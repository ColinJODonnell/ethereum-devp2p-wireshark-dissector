These patch files modify the GETH client to add in key export functionality. These happen in the folling files and functions.

p2p/rlpx/rlpx.go
function makeAuthMsg
function makeAuthResp

crypto/crypto.go
function LoadECDSA

crypto_crypto_key_save_to_file - modifies the crypto/crypto.go file to save the key in plain text when loaded into memory
p2p_rlpx_key_save_to_local - modifies the p2p/rlpx/rlpx.go file to save information about the RLPx messages to file
p2p_rlpx_key_in_header - modifies the p2p/rlpx/rlpx.go file to save the RLPx ephimeral key information in the headers of the packets. This includes modifications to the struct for packets as well. This is for compatability with Kemp's model for dissecting packets. 

