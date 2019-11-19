rakuten-client-go
==================
forked from github.com/ken-io/rakuten-client-go
## Installation

```go
go get -u github.com/suisun2015/rakuten-client-go
```

## Usage

```go
import rakuten "github.com/suisun2015/rakuten-client-go"
```

```go
c := rakuten.NewIchiba("<put your appid>")

param := &rakuten.IchibaItemSearchParam{
        Keyword: "pokemon",
        Sort:    "+itemPrice",
}
resp, _ := c.IchibaItemSearch(param)
fmt.Printf("resp = %+v\n", resp)

param := &rakuten.IchibaRankingParam{
        GenreID: "562354",
        Page:    "2",
}
resp, err := c.IchibaItemRanking(param)
fmt.Printf("resp = %+v\n", resp)
```
