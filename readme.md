# [BZDACS](https://github.com/hardstylez72/bzdacs) - golang client


Easy to use:
```go
...
import acsmw "github.com/hardstylez72/bzdacs-go"

func extractAuthorizationParams(req *http.Request) *acsmw.InputParams {
	return &acsmw.InputParams{
		Login:       "<Your user login>",
		Route:       req.RequestURI,
		Namespace:   "<Your namespace>",
		System:      "<Your system>",
		RouteMethod: req.Method,
	}
}

func main (
	router := NewYourFavoriteRouter()
	router.Use(acsmw.AccessCheck("http(s)://<your-domain>", extractAuthorizationParams))
	server.Serve(router)
)
...
```
