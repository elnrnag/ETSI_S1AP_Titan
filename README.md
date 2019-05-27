# ETSI_S1AP_Titan
Titan-compilable version of ETSI's S1AP Conformance tests

## Prerequisites

### ASN.1 PER encoder/decoder

!!! The project will not compile as-is, since it needs an ASN.1 UPER encoder-decoder. To make it compile the following functions in module S1AP_Types have to be implemented (e.g. by generating a PER encoder with a proprietary tool, like OSS Nokalva's ASN.1 C++ compiler):

external function enc_S1AP_PDU(in S1AP_PDU pdu) return octetstring;

external function dec_S1AP_PDU(in octetstring stream) return S1AP_PDU;

## Titan IPL4 testport, SocketAPI, TCCUsefulFunctions
The following Titan extensions will also be needed:

https://github.com/eclipse/titan.TestPorts.IPL4asp

https://github.com/eclipse/titan.TestPorts.Common_Components.Socket-API

https://github.com/eclipse/titan.Libraries.TCCUsefulFunctions

