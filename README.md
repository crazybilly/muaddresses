# muaddresses -  Tools to standardize and compare addresses

A set of tools in R for standardizing and comparing mailing addresses, built for Millikin University's Alumni & Development Office. Originally forked from [Hans Thompson's rusps package](https://github.com/hansthompson/rusps).

```
devtools::install_github("crazybilly/muaddresses")
library(muaddresses)
username <- 'XXXYYYYYZZZZ' # get this quickly and freely by signing up at https://registration.shippingapis.com/ (not commercial).
street1 <- '333 W raspberry road'
street2 <- '333  raspberry rd'
city   <- 'anchorage'
state  <- 'ak'

usps_validate(username, street1, city, state)

#  Address.Address2       Address.City      Address.State       Address.Zip5       Address.Zip4  Address..attrs.ID 
# "333 RASPBERRY RD"        "ANCHORAGE"               "AK"            "99518"             "1565"                "0" 

# Check if two diffent Addresses resolve to the same address
#   need a new function to do this
# all(validate_address_usps(username, street1, city, state)  == validate_address_usps(username, street2, city, state))
# TRUE
```

## Documentation
- [USPS tools](https://www.usps.com/business/web-tools-apis/address-information-api.htm#_Toc410982986)
- [libpostal](https://github.com/openvenues/libpostal)
- [libpostal docker image with REST](https://github.com/johnlonganecker/libpostal-rest-docker)
- [libpostal-rest on Docker Hub](https://hub.docker.com/r/clicksend/libpostal-rest/)

