
```
/* Digest Algorithms */

var DigestAlgorithms = [
	"MD5",
	"SHA1",
	"SHA224",
	"SHA256",
	"SHA384",
	"SHA512",
];

/* Encryption Schemes */

var EncryptionSchemes = [
	"AES-128-CBC",
	"AES-128-CFB",
];

/* Message Authentication Schemes */

var MessageAuthSchemes = [
	"hmacWithSHA1",
];

/* PKCS #5 */

var KeyDeriveFunctions = [
	"PBKDF1",
	"PBKDF2",
];

var pbes2Params = {
	"keyDeriveFunction": {
		"algorithm": KeyDeriveFunctions[1],
		"parameter": {
			"salt": "0x234208920830492830489234",
			"iterCount": 1024,
			"keyLength": 16
		}
	},
	"encryptionScheme": {
		"algorithm": EncryptionSchemes[0],
		"parameter": { "iv": "0x2902809809809234234"}
	}
};

var pbmac1Params = {
	"keyDeriveFunction": {
		"algorithm": KeyDeriveFunctions[1],
		"parameter": {
			"salt": "0x234208920830492830489234",
			"iterCount": 1024,
			"keyLength": 20
		}
	},
	"messageAuthScheme": {
		"algorithm": MessageAuthSchemes[0],
	}
};

/* PKCS #7 */

var ContentTypes = [
	"data",
	"signedData",
	"envelopedData",
	"signedAndEnvelopedData",
	"digestedData",
	"encryptedData",
];

var dataContentInfo = {
	"contentType": "data",
	"content": "message"
};


/* PKCS #7 SignedData */

var signerInfo = {
	"version": 1,
	"signer": { "serialNumber": "234234234" },
	"digestAlgirthm": "SHA1",
	"signedAttributes": [],
	"signatureScheme": "ecdsa-with-SHA1",
	"unsignedAttributes": []
};

var signedData = {
	"version": 1,
	"digestAlgorithms": [ "SHA1" ],
	"contentInfo": dataContentInfo,
	"certificates": [],
	"crls": [],
	"signerInfos": [ signerInfo ]
};

var signedDataContentInfo = {
	"contentType": "signedData",
	"content": signedData
};

var recipientInfo = {
	"version": 1,
	"recipient": { "emailAddress": "guanzhi@hotmail.com" },
	"keyEncryptionScheme": {
		"algorithm": "AES-128-CBC",
		"parameter": ...
	},
	"encryptedKey": "0x3240298023984203948"
};

var envelpedData = {
	"version": 1,
	"recipientInfos": [ recipientInfo ],
	"encryptedContentInfo": {
		"contentType": ,
		"contentEncryptionScheme": ,
		"encryptedConent": 
	}
};

var signedAndEnvelopedData = {
	"version": 1,
	"recipientInfos": [ recipientInfo ],
	"digestAlgorithms": [ "SHA1" ],
	"encryptionConentInfo": encrptedContentInfo,
	"certificates": [],
	"crls": [],
	"signerInfos": [ signerInfo1 ]	
};

var encryptedData = {
	"version": 1,
	"encryptedContentInfo": encryptedContentInfo
};


	

/* Elliptic Curve Cryptography */

var ECDSAAlgorithms = [
	"ecdsa-with-SHA1",
	"ecdsa-with-Recommended",
	"ecdsa-with-SHA224",
	"ecdsa-with-SHA256",
	"ecdsa-with-SHA384",
	"ecdsa-with-SHA512",
];

var ECDHAlgorithms = [
	"dhSinglePass-stdDH-sha1kdf",
	"dhSinglePass-cofactorDH-sha1kdf",
	"dhSinglePass-cofactorDH-recommendedKDF",
	"dhSinglePass-cofactorDH-specifiedKDF",
];

var ECIESAlgorithms = [
	"ecies-recommendedParameters",
	"ecies-specifiedParameters",
];

var ECCAlgorithms = [
	ECDSAAlgorithmSet,
	ECDHAlgorithmSet,
	ECMQVAlgoirthmSet,
	ECIESAlgorithmSet,
	ECWKTAlgorithmSet,
];

var ECDOMainParameters = [
	"specified",
	"named",
	"implicitCA",
];

var CurveNames = [
	"secp192k1",
	"secp256k1",
];

var FieldTypes = [
	"prime-field",
	"characteristic-two-field",
];

var specifiiedECDomain ::= {
	"version": 1,
	"fieldID": {
		"fieldType": FieldTypes[0],
		"primeP": "0x8909283409283409283402834098"
	},
	"curve": {
		"a": "0x23428902938402983409234802938408",
		"b": "0x982347928374982347982347928347234",
		"seed": "0x234234234234234234234234"
	},
	"base": "0x32490982093402938402834",
	"order": "0x234234234234234234234",
	"cofactor": 1
};
	
var ecPrivateKey1 = {
	"version": 1,
	"privateKey": "0x234298023984203849",
	"parameters": { "specified": specifiiedECDomain }
};

var ecPrivateKey2 = {
	"version": 1,
	"privateKey": "0x234298023984203849",
	"parameters": { "named": CurveNames[0] }
};

var ecdsaSigValue = {
	"r": "0x234098230948023984203849",
	"s": "0x234098230948023984203849",
};

var eciesCiphertextValue = {
	"ephemeralPublicKey": "0x0982309482309482034892348203498029384",
	"symmetricCiphertext": "23409009283049820394208394",
	"macTag": "3920348029834092834",
};


/* PKCS #8 Private Key Info */

var ecPrivateKeyInfo = {
	"version": 0,
	"privateKeyAlgorithm": {
		"algorithm": "EC",
		"parameter": { "named": "secp192k1" }
	},
	"privateKey": "0x3423948029834023",
	"attributes": []
};

```