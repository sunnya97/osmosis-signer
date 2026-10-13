# Keplr Tx Signer
Static page: pre-built tx cards (Simulate / Sign & Broadcast via Keplr) + advanced raw-message panel.

Run (Keplr does not inject into file:// pages):
    cd keplr-signer && python3 -m http.server 8787
    open http://localhost:8787

Edit `TRANSACTIONS` at the top of the script in index.html, or drop a sibling `transactions.json`
(same array shape; static entries only — `live` builders must exist in index.html's LIVE object).
Card msg format: {type:"execute", contract, msg:{...}, funds:[]} or {typeUrl, value}.
RPC defaults to https://rpc.osmosis.zone (alternates in dropdown). No keys stored, no analytics.
