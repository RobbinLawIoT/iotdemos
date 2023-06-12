# Protocols

## TCP/IP Stack

- [Internet Protocol Suite by Wikipedia](https://en.wikipedia.org/wiki/Internet_protocol_suite)

## Application Layer
- [Evolution of HTTP by mdn](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP)
- [SSL vs TLS](https://aws.amazon.com/compare/the-difference-between-ssl-and-tls)


## Transport Layer

## Internet Layer

## Link Layer 
- OSI Model Equivalent
  - Data Link Layer (layer2)
    - Logical Link Control
    - Media Access Control
  - Physical (layer1)
- includes protocols for communication between all hosts accessible without traversing a router.
- [IEEE 802](https://en.wikipedia.org/wiki/IEEE_802)
  - [802.3 Ethernet]()
  - [802.11 Wireless Local Area Network (WLAN) aka Wireless Fidelity (Wi-Fi)]()
  - [802.15 Wireless Personal Area Network (WPAN)](https://en.wikipedia.org/wiki/IEEE_802.15)
    - 802.15.1 Bluetooth
    - 802.15.4 Low Rate Wireless Personal Area Network (LR-WPAN)
      - low power, low data rates, close proximity
      - 10m range, line-of-sight 250 kbit/s
      - defines physical and media access control of OSI model
      - standard defined in 2003
      - examples
        - [Zigbee](https://en.wikipedia.org/wiki/Zigbee)
          - home automation, medical device data collection
        - [WirelessHART](https://en.wikipedia.org/wiki/WirelessHART)
          - industrial, highway addressable remote transducer Protocol (HART)
          - time synchronized, self organizing, self healing mesh architecture
        - [ISA100.11a](https://en.wikipedia.org/wiki/ISA100.11a)
          - industrial, Honeywell, Yokogawa
        - [IPv6 over Low Power Personal Area Networks (6LoWPAN)](https://en.wikipedia.org/wiki/6LoWPAN)
          - Internet Engineering Task Force (IETF) working group
          - applying IPv6 Protocol over IEEE802.15.4 allowing low power low memory devices to participate in the IoT
          - the Thread protocol is built over 6LoWPAN
