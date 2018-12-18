# crypto-address-validator
Validates crypto currency addresses. Currently BTC, ETH

### BTC usage
```
  import (
    "fmt"

    CryptoAddressValidator "github.com/IvRRimum/crypto-address-validator"
  )

  func main() {
    address := "1AGNa15ZQXAZUgFiqJ2i7Z2DPU2J6hW62i"
    ok, err := CryptoAddressValidator.ValidA58([]byte(os.Args[1]))
    if !ok || err != nil {
      fmt.Println("Address is invalid")
      return
    }

    fmt.Println("Address ", address, " is a valid BTC address!")
  }
```
