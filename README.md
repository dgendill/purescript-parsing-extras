# purescript-parsing-extras

Extra parsing functions to be used with [purescript-parsing](https://github.com/purescript-contrib/purescript-parsing). Pull requests welcome.

## Module Text.Parsing.Extras

#### `fromCharList`

``` purescript
fromCharList :: forall f. Foldable f => f Char -> String
```

#### `alphaNumString`

``` purescript
alphaNumString :: forall m. Monad m => ParserT String m String
```

Parse a single alphanumeric string

#### `betweenQuotes`

``` purescript
betweenQuotes :: forall s m. StringLike s => Monad m => ParserT s m String
```

Parse all characters between single or double quotes

#### `betweenDoubleQuotes`

``` purescript
betweenDoubleQuotes :: forall s m. StringLike s => Monad m => ParserT s m String
```

Parse all characters between double quotes

#### `betweenSingleQuotes`

``` purescript
betweenSingleQuotes :: forall s m. StringLike s => Monad m => ParserT s m String
```

Parse all characters between single quotes

#### `parseArray`

``` purescript
parseArray :: forall s m a. StringLike s => Monad m => ParserT s m a -> ParserT s m (Array a)
```

Parse an array of items embed within braces and
seperated by commas. Whitespace is allowed between braces, items, and commas, e.g.
[ whitespace (item) whitespace , whitespace (item) whitespace ]


