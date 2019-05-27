# ETSI_S1AP_Titan
Titan-compilable version of ETSI's S1AP Conformance tests

!!! The project will not compile as-is, since it needs an ASN.1 UPER encoder-decoder. To make it compile the following functions in module S1AP_Types have to be implemented:

external function enc_S1AP_PDU(in S1AP_PDU pdu) return octetstring;

external function dec_S1AP_PDU(in octetstring stream) return S1AP_PDU;
