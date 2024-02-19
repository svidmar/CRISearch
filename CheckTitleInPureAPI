(title as text) =>
let
    apiKey = "Pure_APIkey",
    encodedTitle = Uri.EscapeDataString(title),
    url = "https://Pure_unstance_URL/ws/api/524/research-outputs?q=" & encodedTitle & "&apiKey=" & apiKey,
    Source = Json.Document(Web.Contents(url, [Headers=[Accept="application/json"]])),
    Count = try Source[count] otherwise -1
in
    if Count = 0 then "No"
    else if Count > 0 then "Yes"
    else "Error: Invalid or missing count"
