## Module Apiary.Types

#### `Request`

``` purescript
type Request = { body :: String, headers :: Headers, method :: Method, url :: URL }
```

#### `emptyRequest`

``` purescript
emptyRequest :: Request
```

#### `Response`

``` purescript
type Response = { body :: String, headers :: Headers, status :: Int }
```

#### `Error`

``` purescript
data Error
  = RuntimeError Error
  | DecodeError Response MultipleErrors
  | UnexpectedResponse Response
```

##### Instances
``` purescript
Semigroup Error
```

#### `Apiary`

``` purescript
type Apiary = Except Error
```

