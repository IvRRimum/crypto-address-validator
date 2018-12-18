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
    // version - most used:
    // 0 - Ex. address: 1AWxjnBTBZBXnV3pGiDmEThousaeQ83K61
    // 5 - Ex. address: 3FAwA6gSAmuVcVcW9Mf5s4b79KHQm27JEq
    // Full list, including testnet prefixes(see Decimal prefix) - https://en.bitcoin.it/wiki/List_of_address_prefixes
    ok, version, err := CryptoAddressValidator.ValidateBTCAddress([]byte(address))
    if !ok || err != nil {
      fmt.Println("Address is invalid")
      return
    }

    fmt.Println("Address ", address, " is a valid BTC address! Version: ", version)
  }
```
