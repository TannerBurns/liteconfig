# LiteConfig

    Simple config parser in golang
    Ini style config parser


# Example

    settings.conf

        [default]
        name=LiteConfig
        version=0.1
        author=Tanner Burns

        [section2]
        example=This is an example

    main.go

        package main

        import (
            "fmt"
            "log"

            "github.com/tannerburns/liteconfig"
        )

        func main() {
            path := "settings.conf"
            lc, err := liteconfig.NewConfig(path)
            if err != nil {
                log.Fatal(err)
            }
            fmt.Println(lc.Config["default"]["name"])
        }



