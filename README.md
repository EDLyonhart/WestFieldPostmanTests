# WestFieldPostmanTests


End points touched through:

User Flow / Acceptance Tests:
  -Parking
  -Partial Accounts / Newsletters
  -Staff Access Flow / User Update
  - Wishlists / Favorites

Integration Tests : /accounts:
  - User Accounts
  - Credit Cards
  - Interests
  - Kids
  - Newsletters
  - Parking
Integration Tests : Garages / Operators
Integration Tests : Gateways / Merchants  **** Potentially problematic. Destructively interact with sensitive routes and database entries.





integration tests | acceptance tests | verb | route

ACCOUNTS

|----|----| POST   | /account |

|----|----| GET    | /account |

|----|----| PATCH  | /account |

|----|----| PATCH  | /account/password |

|----|----| DELETE | /account |

|----|----| POST   | /account/upgrade |

|----|----| GET    | /account/status |

|----|----| POST   | /account/credit_cards |

|----|----| GET    |	/account/credit_cards |

|----|----| PATCH  |	/account/credit_cards/<payment_method_token> |

|----|----| DELETE | /account/credit_cards/<payment_method_token> |

|----|----| POST   | /account/interests |

|----|----| GET    | /account/interests |

|----|----| PUT    | /account/interests |

|----|----| POST   | /account/kids |

|----|----| GET    | /account/newsletters |

|----|----| PATCH  | /account/newsletters/subscribe |

|----|----| POST   | /account/newsletters/subscribe |

|    |----| POST   | /account/parking/email_invoice |

|----|----| GET    | /account/parking/history |

|----|----| GET    | /account/parking/sessions/summary |

|----|----| POST   | /account/parking/signup |

|----|----| GET    | /account/vehicles |

|----|----| POST   | /account/vehicles |

|----|----| PATCH  | /account/vehicles/<license_plate> |

|----|----| DELETE | /account/vehicles/<license_plate> |

|    |    | PUT    | /account/apps/<app_id> |

|    |    | PUT    | /account/apps/<app_id>/devices/<device_token> |

|    |    | DELETE | /account/apps/<app_id>/devices/<device_token> |


PEOPLE

|----|    | GET    | /people |

|    |----| GET    | /people/{person_id} |

|    |----| PATCH  | /people/{person_id} |

|----|    | GET    | /people/{person_id}/credit_cards |

|----|    | GET    | /people/{person_id}/food/history |

|----|    | GET    | /people/{person_id}/food/orders/{food_order_id} |

|----|    | POST   | /people/{person_id}/food/orders/{food_order_id}/receipt |

|    |----| GET    | /people/{person_id}/interests |

|    |----| POST   | /people/{person_id}/interests |

|----|----| PUT    | /people/{person_id}/kids |

|----|----| GET    | /people/{person_id}/kids |

|    |----| GET    | /people/{person_id}/parking/history |

|    |----| POST   | /people/{person_id}/parking/invoice |

|    |----| POST   | /people/{person_id}/parking/receipt |

|    |----| GET    | /people/{person_id}/vehicles |

|    |----| POST   | /people/{person_id}/vehicles |

|    |----| DELETE | /people/{person_id}/vehicles/{license_plate} |

|    |    | GET    | /people/analytics |

|    |    | GET    | /people/integrations/edna/accounts |

|    |    | POST   | /people/notification |

|    |    | POST   | /people/notifications/email |

|    |    | POST   | /people/notifications/push |

|    |    | POST   | /people/notifications/sms |

|    |    | POST   | /people/oauth/revoke |

|----|----| POST   | /people/oauth/token |

|    |----| GET    | /people/oauth/token/info |

|    |    | GET    | /people/parking |

|    |    | POST   | /people/password_resets |

|    |    | PUT    | /people/password_resets/{token} |

|    |    | POST   | /people/tickets/feedback |

|    |    | POST   | /people/tickets/support |


PARKING

|    |----| POST   | /parking/activities |

|----|    | GET    | /parking/garages |

|----|    | POST   | /parking/garages |

|----|    | GET    | /parking/garages/{centre_id}/summary |

|----|    | GET    | /parking/garages/{garage_id} |

|----|    | PATCH  | /parking/garages/{garage_id} |

|    |    | POST   | /parking/integrations/swarco/{centre_id}/garages |

|----|    | POST   | /parking/operators |

|----|    | GET    | /parking/operators |

|----|    | GET    | /parking/operators/{centre_id} |

|----|    | DELETE | /parking/operators/{centre_id} |

|----|    | PATCH  | /parking/operators/{centre_id} |

|    |----| GET    | /parking/sessions |

|    |----| GET    | /parking/sessions/{parking_session_id} |

|    |----| POST   | /parking/sessions/{parking_session_id}/charge |

|    |----| POST   | /parking/sessions/{parking_session_id}/refund |

|    |----| GET    | /parking/sessions/invoice |

|    |----| GET    | /parking/sessions/open |

|    |----| GET    | /parking/sessions/summary |


PAYMENTS

|****|    | GET    | /payments/gateways |

|****|    | POST   | /payments/gateways |

|****|    | DELETE | /payments/gateways/{gateway_id} |

|****|    | GET    | /payments/gateways/{gateway_id} |

|****|    | PATCH  | /payments/gateways/{gateway_id} |

|****|    | GET    | /payments/merchants |

|****|    | POST   | /payments/merchants |

|****|    | DELETE | /payments/merchants/{merchant_id} |

|****|    | GET    | /payments/merchants/{merchant_id} |

|****|    | PATCH  | /payments/merchants/{merchant_id} |

|****|----| DELETE | /payments/payment_methods/{payment_method_token} |

|****|----| GET    | /payments/payment_methods/{payment_method_token} |

|****|    | PATCH  | /payments/payment_methods/{payment_method_token} |

|****|    | POST   | /payments/payment_methods/{payment_method_token}/verify |

|    |    | POST   | /payments/stripe_events |

|    |    | GET    | /payments/transactions/{transaction_id} |

|    |    | POST   | /payments/transactions/{transaction_id}/capture |

|    |    | POST   | /payments/transactions/{transaction_id}/refund |

|    |    | POST   | /payments/transactions/{transaction_id}/void |

|****|    | POST   | /payments/transactions/authorize |

|****|    | POST   | /payments/transactions/purchase |


STAFF

|    |    | GET    | /staff |

|    |    | POST   | /staff |

|    |    | GET    | /staff/{uuid} |

|    |    | POST   | /staff/revoke |

|----|----| POST   | /staff/token |

|    |----| GET    | /staff/token/info |


WISHLISTS

|    |----| GET    | /favorites |

|    |----| DELETE | /favorites/{person_id} |

|    |----| POST   | /favorites/items |

|    |----| DELETE | /favorites/items/{kind}/{resource_id} |

|    |----| POST   | /favorites/items/bulk |


WFAPI

|    |----| GET    | /stores |

|    |----| GET    | /events |

|    |----| GET    | /deals |
