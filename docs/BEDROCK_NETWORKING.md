# Bedrock Networking (Proxmox)

- Use **bridged** networking (vmbr0) so the guest gets a LAN IP.
- Open/forward **UDP 19132** to the guest.
- In LXC set features: `keyctl=1,nesting=1`.
- LAN discovery can fail across virtualization; add the server manually via `IP:19132`.
- UFW example inside guest:
  ```bash
  ufw allow 19132/udp
  ```

- OpenID **Connect** is an interoperable authentication protocol based on the **OAuth 2.0** framework of specifications 
  (IETF RFC 6749 and 6750). It simplifies the way to verify the identity of users based on the authentication performed 
  by an Authorization Server and to obtain user profile information in an interoperable and REST-like manner.

- OpenID Connect enables application and website developers to launch sign-in flows and receive verifiable assertions
  about users across Web-based, mobile, and JavaScript clients. And the specification suite is extensible to support a
  range of optional features such as encryption of identity data, discovery of OpenID Providers, and session logout.

- For developers, it provides a secure and verifiable answer to the question “What is the identity of the person currently
  using the browser or mobile app that is connected?” Best of all, it removes the responsibility of setting, storing, and
  managing passwords which is frequently associated with credential-based data breaches.
