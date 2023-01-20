# Basics
**HTTP** = HyperText Transfer Protocol   
* _HyperText_ = content with reference to other content (text, images, videos, or any other digital content)  
  * references between hypertexts recourses are called hyperlinks or just links.
* _Transfer Protocol_ = a set of guidelines/process of exchanging data, but doesn't define what that data might be.

HTTP (HyperText Transfer Protocol) is a request/response protocol. An HTTP exchange is more like a series of distinct   questions and answers than a conversation between two systems. 

**The ability to link pages/massive collections together for interactivity is what makes everything possible!**

---

HTTP defines the process of exchanging hypertext between systems and works between clients and servers. 
* _Clients_ or user agent = the data consumer (your browser)
* _Servers_ or origin = the data provider, often where an application is running

In a typical exchange, the client sends a request to the server for a particular resource - a webpage, image, or application data - and the server provides a response containing either the resource that the client requested or an explanation of why it can't provide the resource. 

You ask the server a simple yes/no question and it responds accordingly. 

# Properties 

### Reliable Connections
Messages passed between clients and servers sacrifice a little speef for the sake of trust. 

HTTP doesn't work well if messages aren't received in the correct order, so it's critical that the connection your hypertext is crossing is reliable. 

### Stateless Transfer
As a _stateless_ protocol, HTTP doesn't store any information. Each request you send across an HTTP connection should contain all its own context (unlike a _stateful_ protocol, which might include specifications of storing data between requests). Therefore, you only ever need to read a single HTTP request to understand its intent - this is different for maintaining login statuses or the contents of a shopping cart. 

HTTP supports _cookies_, bits of data that a client sends in with their request. The server can examine this data/loop up a _session_ for your account, or it can act on the information in the cookie directly. 

### Intermediaries
The Internet is a big place. Your request will pass through a series of intermediaries, other servers or devices that pass along your request. These include 3 types
- proxies: may modify your request so it appears to come from a different source
- gateways: pretend to be the resource server you requested
- tunnels: simply pass your request along

#### Example

1. Client
- Your Computer  
Also known as the "User Agent," initiates the HTTP reqest and renders the response. 
2. Proxy
- Your Router  
Hides your computer's details behind a shared IP address. May add request headers. 
3. Tunnel
- Intermediate Servers  
There might be a LOT of these! Clients and servers internet providers, routers, etc. Passes requests and responses directly through.
4. Gateway
- Their Router  
Hides the server's details behind a shared IP address. This is as far as the client can "see".
5. Server
- Their Data Center  
Also known as the "origin," the receiving server, likely part of much later network of servers. Generates the response and sends it back down the line. 

**Note:** These are interchangeable depending on the flow of data! This is an important part of HTTP: a single server may act as any of the intermediary types, depending on the needs of the HTTP message it's transmitting. 

The key takeaway is that HTTP isn't limited to  your browser and application servers. Lots of devices support HTTP in their own way!

---

[The HTTP Spec](https://tools.ietf.org/html/rfc2616#section-1.4) describes the protocol in great detail. 

