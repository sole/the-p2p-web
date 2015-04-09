# the-p2p-web

## APIs

* NetworkStats - methods and properties to monitor data usage. e.g. type of network which is providing internet to us now (data or wifi)
  * available via [mozNetworkStatsManager](https://developer.mozilla.org/en-US/docs/Web/API/window/navigator/mozNetworkStats)
* NFC - not strictly network based but can transmit data!
* TCPSocket. [TCP](http://en.wikipedia.org/wiki/Transmission_Control_Protocol) transmissions are *reliable, ordered and error-checked*.
  * Accessible via `mozTCPSocket`
  * [API docs](https://developer.mozilla.org/en-US/docs/Web/API/TCPSocket)
* UDPSocket. UDP transmissions emphasise reduced latency over reliability so no error-checking, in contrast with TCP.
  * Accessible via `UDPSocket`, but totally undocumented :-(
  * [WebIDL](http://mxr.mozilla.org/mozilla-central/source/dom/webidl/UDPSocket.webidl)
  * Related bugs
    * [745283 - Expose a client UDP datagram socket API to web applications](https://bugzilla.mozilla.org/show_bug.cgi?id=745283) -- all attachments with test cases are somewhat hidden [here](https://bugzilla.mozilla.org/attachment.cgi?bugid=745283&action=viewall)
    * [1152283 - Repeated use of UDPSocket without calling close() end up restarting Gaia](https://bugzilla.mozilla.org/show_bug.cgi?id=1152283)
* WebSockets: send messages to a server and receive event-driven responses without having to poll the server for a reply.
  * [API docs](https://developer.mozilla.org/en-US/docs/Web/API/WebSocket)
  * [Documentation](https://developer.mozilla.org/en-US/docs/WebSockets)
* WiFi information via the `navigator.mozWifiManager` object
  * [API docs](https://developer.mozilla.org/en-US/docs/Web/API/WiFi_Information_API)
* Wifi Direct via the `WifiP2pManager` object
  * [WiFi Direct](https://en.wikipedia.org/wiki/Wi-Fi_Direct) wikipedia article, good overview.
  * Bug [811635 - B2G Wifi: Support Wifi Direct](https://bugzilla.mozilla.org/show_bug.cgi?id=811635)
  * [WebIDL](https://dxr.mozilla.org/mozilla-central/source/dom/wifi/WifiP2pManager.jsm)
  * (incomplete) [API docs](https://developer.mozilla.org/en-US/docs/Web/API/MozWifiP2pManager)
  * [Blog post](https://hacks.mozilla.org/2015/01/the-p2p-web-wi-fi-direct-in-firefox-os/)
  * Examples
    * [firedrop](https://github.com/justindarc/firedrop) - share files with devices nearby
	* [Who is around?](https://github.com/gmarty/who-is-around) - Discover devices and services around you in a fun way
	* [Wifi Columns](https://github.com/gmarty/wifi-columns) - emulator running Columns game, p2p players without internet connection

## Libraries

* [dns-sd.js](https://github.com/justindarc/dns-sd.js) - announcing and discovering services via multicast DNS. Firefox OS only (?)
* [p2p-helper.js](https://github.com/justindarc/p2p-helper.js) - utility for simplifying peer-to-peer connections in Firefox OS
* [fxos-web-server](https://github.com/justindarc/fxos-web-server)
  * [blog post](https://hacks.mozilla.org/2015/02/embedding-an-http-web-server-in-firefox-os/)

## Usual examples

* [Echo protocol](http://en.wikipedia.org/wiki/Echo_Protocol)

## Sample / demo apps

* [networkInfo](https://github.com/sole/networkInfo) - show currently connected wi-fi network plus IP address and network security scheme
