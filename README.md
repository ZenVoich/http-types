# Canister HTTP interface types

More https://internetcomputer.org/docs/current/references/http-gateway-protocol-spec/

## Install
```
mops add http-types
```

## Usage
```motoko
import HttpTypes "mo:http-types";
import Text "mo:base/Text";

public query func http_request(request : HttpTypes.Request) : async HttpTypes.Response {
  return {
    status_code = 200;
    headers = [
      ("Content-Type", "text/html; charset=utf-8"),
    ];
    body = Text.encodeUtf8("Hello, <b>World!</b>");
    streaming_strategy = null;
    upgrade = null;
  };
}
```