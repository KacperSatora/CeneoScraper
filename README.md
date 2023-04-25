# CeneoScraper

## Selektory CSS składowych opinii w serwisie Ceeneo.pl

| Składowa | Nazwa | Selektor |
| --- | --- | --- |
| Opinia | Opinion | div.js\_product-review |
| Identyfikator opinii | Opinion\_Id | ["data-entry-id"] |
| Autora | Author | span.user-post\_\_author-name |
| Rekomendację | Recommendation | span.user-post\_\_author-recommendation \> em |
| Liczbę Gwiazdek | Score | span.user-post\_\_score-count |
| Czy opinia jest potwierdzona zakupem | Purchased | div.review-pz |
| Data wystawienia opinii | Published\_at | span.user-post\_\_published \> time:nth-child(1)["datetime"] |
| Data zakupu produktu | Purchased\_at | span.user-post\_\_published \> time:nth-child(2)["datetime"] |
| Ile osób uznało opinię za przydatną | Thumbs\_up | span[id^=votes-yes]button.vote-yes["data-total-vote"]button.vote-yes \> span |
| Ile osób uznało opinię za nieprzydatną | Thumbs\_down | span[id^=votes-no]button.vote-no["data-total-vote"]button.vote-no \> span |
| Treść opinii | Content | div.user-post\_\_text |
| Listę wad | Cons | div.review-feature\_\_col:has(\> div.review-feature\_\_title--negatives) \> div.review-feature\_\_item |
| Listę zalet | Pros | div.review-feature\_\_col:has(\> div.review-feature\_\_title--positives) \> div.review-feature\_\_item |

## Użyte biblioteki
- Requests
- BeautifulSoup4