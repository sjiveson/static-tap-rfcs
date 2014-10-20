# API Reference Documentation

See [RFC 011][1] to comment on the API Reference Documentation,
including issues such as "Should the version be in the path or in
a header?" and "Should the path include /api or should that be part of
the hostname?"

## Responses

All API endpoints currently return "the kitchen sink".  You cannot
filter or search using the API at this time.

## Versioned

The API is versioned, and it begins with a base path of `/api`.  The
version follows in the current path, so the base path for any resource
is `/api/vx`, where `x` is the version number.  As of now, that path
will be `/api/v0`.

## Interfaces

#### Endpoint

```bash
/api/v0/interfaces
```

#### Response

| Attribute                   | Contents                              |
|-----------------------------|---------------------------------------|
| `created_at`                | Timestamp when record was created     |
| `updated_at`                | Timestamp when record was updated     |
| `device`                    | Device to which this belongs          |
| `name`                      | Interface name                        |
| `interface_flapped`         | Last time interface was down          |
| `admin_status`              | Administrative status                 |
| `oper_status`               | Operational status                    |
| `input_bps`                 | Input rate in bps - Input             |
| `output_bps`                | Number of bits per second - Output    |
| `input_pps`                 | Number of packets per second - Input  |
| `output_pps`                | Number of packets per second - Output |
| `hardware_physical_address` | Physical address                      |
| `mtu`                       | Maximum Transmission Unit             |
| `speed`                     | Maximum rate                          |
| `id`                        | Record number                         |

## OSPF

#### API Endpoint

```bash
/api/v0/protocols/ospf
```

#### Response

| Attribute             | Contents                                  |
|-----------------------|-------------------------------------------|
| `created_at`          | Timestamp when record was created         |
| `updated_at`          | Timestamp when record was updated         |
| `device`              | Device to which this belongs              |
| `neighbor_id`         | Neighbor ID of the OSPF Neighbor          |
| `neighbor_address`    | Address of the neighbor's interface       |
| `interface_name`      | Interface through which neighbor is known |
| `ospf_neighbor_state` | OSPF State                                |
| `neighbor_priority`   | Neighbor's OSPF Priority                  |
| `activity_timer`      | OSPF Dead Timer                           |

[1]: ../../../issues/11 "RFC 011: API Route Structure"
