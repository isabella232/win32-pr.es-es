---
description: Especifica un identificador de algoritmo.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f4b6c476a8ea6e61785a096abf33c357d9b024
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482401"
---
# <a name="alg_id"></a>ALG_ID

El **ALG_ID** de datos especifica un identificador de algoritmo. Los parámetros de este tipo de datos se pasan a la mayoría de las funciones de CryptoAPI.


```C++
typedef unsigned int ALG_ID;
```



En la tabla siguiente se enumeran los identificadores de algoritmo que están definidos actualmente. Los autores de proveedores [*de servicios criptográficos*](../secgloss/c-gly.md) personalizados (CSP) pueden definir nuevos valores. Además, los **ALG_ID** usan los CSP personalizados  para las especificaciones clave AT_KEYEXCHANGE y **AT_SIGNATURE** dependen del proveedor. Las asignaciones actuales siguen a la tabla.




| Identificador | Valor | Descripción | 
|------------|-------|-------------|
| CALG_3DES | 0x00006603 | <a href="/windows/desktop/SecGloss/t-gly"><em>Algoritmo de cifrado triple de DES.</em></a> | 
| CALG_3DES_112 | 0x00006609 | Cifrado <a href="/windows/desktop/SecGloss/t-gly"><em>DES triple de</em></a> dos claves con una longitud de clave efectiva igual a 112 bits. | 
| CALG_AES | 0x00006611 | Estándar de cifrado avanzado (AES). Este algoritmo es compatible con el proveedor <a href="microsoft-aes-cryptographic-provider.md">criptográfico AES de Microsoft</a>. | 
| CALG_AES_128 | 0x0000660e | AES de 128 bits. Este algoritmo es compatible con el proveedor <a href="microsoft-aes-cryptographic-provider.md">criptográfico AES de Microsoft</a>. | 
| CALG_AES_192 | 0x0000660f | AES de 192 bits. Este algoritmo es compatible con el proveedor <a href="microsoft-aes-cryptographic-provider.md">criptográfico AES de Microsoft</a>. | 
| CALG_AES_256 | 0x00006610 | AES de 256 bits. Este algoritmo es compatible con el proveedor <a href="microsoft-aes-cryptographic-provider.md">criptográfico AES de Microsoft</a>. | 
| CALG_AGREEDKEY_ANY | 0x0000aa03 | Identificador de algoritmo temporal para identificadores de claves diffie-Hellman acordados. | 
| CALG_CYLINK_MEK | 0x0000660c | Algoritmo para crear una clave DES de 40 bits que tenga bits de paridad y bits de clave con cero para que su longitud de clave sea de 64 bits. Este algoritmo es compatible con el proveedor <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">criptográfico base de Microsoft</a>. | 
| CALG_DES | 0x00006601 | Algoritmo de cifrado DES. | 
| CALG_DESX | 0x00006604 | Algoritmo de cifrado DESX. | 
| CALG_DH_EPHEM | 0x0000aa02 | Diffie-Hellman algoritmo de intercambio de claves efímero. | 
| CALG_DH_SF | 0x0000aa01 | Diffie-Hellman el algoritmo de intercambio de claves de almacenamiento y reenvío. | 
| CALG_DSS_SIGN | 0x00002200 | Algoritmo de firma <a href="/windows/desktop/SecGloss/p-gly"><em>de clave pública</em></a> DSA. | 
| CALG_ECDH | 0x0000aa05 | Curva elíptica Diffie-Hellman algoritmo de intercambio de claves.<blockquote>[!Note]<br />Este algoritmo solo se admite a través <a href="/windows/desktop/SecCNG/cng-portal">de Cryptography API: Next Generation</a>.</blockquote><br /><strong>Windows Server 2003 y Windows XP:</strong> Este algoritmo no se admite.<br /> | 
| CALG_ECDH_EPHEM | 0x0000ae06 | Curva elíptica efímera Diffie-Hellman algoritmo de intercambio de claves.<blockquote>[!Note]<br />Este algoritmo solo se admite a través <a href="/windows/desktop/SecCNG/cng-portal">de Cryptography API: Next Generation</a>.</blockquote><br /><strong>Windows Server 2003 y Windows XP:</strong> Este algoritmo no se admite.<br /> | 
| CALG_ECDSA | 0x00002203 | Algoritmo de firma digital de curva elíptica.<blockquote>[!Note]<br />Este algoritmo solo se admite a través <a href="/windows/desktop/SecCNG/cng-portal">de Cryptography API: Next Generation</a>.</blockquote><br /><strong>Windows Server 2003 y Windows XP:</strong> Este algoritmo no se admite.<br /> | 
| CALG_ECMQV | 0x0000a001 | Algoritmo de intercambio de claves Menezes, Qu y Vanstone (MQV) de curva elíptica. Este algoritmo no se admite. | 
| CALG_HASH_REPLACE_OWF | 0x0000800b | Algoritmo hash de función un solo sentido. | 
| CALG_HUGHES_MD5 | 0x0000a003 | Algoritmo hash MD5 de Md5. | 
| CALG_HMAC | 0x00008009 | Algoritmo hash con clave HMAC. Este algoritmo es compatible con el proveedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base de Microsoft</a>. | 
| CALG_KEA_KEYX | 0x0000aa04 | Algoritmo de intercambio de claves KEA (FORTEZZA). Este algoritmo no se admite. | 
| CALG_MAC | 0x00008005 | Algoritmo hash con clave <a href="/windows/desktop/SecGloss/m-gly"><em>MAC.</em></a> Este algoritmo es compatible con el proveedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base de Microsoft</a>. | 
| CALG_MD2 | 0x00008001 | Algoritmo de hash MD2. Este algoritmo es compatible con el proveedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base de Microsoft</a>. | 
| CALG_MD4 | 0x00008002 | Algoritmo de hash MD4. | 
| CALG_MD5 | 0x00008003 | Algoritmo de hash MD5. Este algoritmo es compatible con el proveedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base de Microsoft</a>. | 
| CALG_NO_SIGN | 0x00002000 | Ningún algoritmo de firma. | 
| CALG_OID_INFO_CNG_ONLY | 0xffffffff | El algoritmo solo se implementa en CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, se puede usar para determinar si un algoritmo criptográfico solo se admite mediante el uso de las funciones CNG. | 
| CALG_OID_INFO_PARAMETERS | 0xfffffffe | El algoritmo se define en los parámetros codificados. El algoritmo solo se admite mediante CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, se puede usar para determinar si un algoritmo criptográfico solo se admite mediante el uso de las funciones CNG. | 
| CALG_PCT1_MASTER | 0x00004c04 | Usado por el sistema Schannel.dll operaciones. Las <strong>ALG_ID</strong> no deben usar este tipo de datos. | 
| CALG_RC2 | 0x00006602 | Algoritmo de cifrado de bloque RC2. Este algoritmo es compatible con el proveedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base de Microsoft</a>. | 
| CALG_RC4 | 0x00006801 | Algoritmo de cifrado de secuencia RC4. Este algoritmo es compatible con el proveedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base de Microsoft</a>. | 
| CALG_RC5 | 0x0000660d | Algoritmo de cifrado de bloques RC5. | 
| CALG_RSA_KEYX | 0x0000a400 | Algoritmo de intercambio de claves públicas RSA. Este algoritmo es compatible con el proveedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base de Microsoft</a>. | 
| CALG_RSA_SIGN | 0x00002400 | Algoritmo de firma de clave pública RSA. Este algoritmo es compatible con el proveedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base de Microsoft</a>. | 
| CALG_SCHANNEL_ENC_KEY | 0x00004c07 | Usado por el sistema Schannel.dll operaciones. Las <strong>ALG_ID</strong> no deben usar este tipo de datos. | 
| CALG_SCHANNEL_MAC_KEY | 0x00004c03 | Usado por el sistema Schannel.dll operaciones. Las <strong>ALG_ID</strong> no deben usar este tipo de datos. | 
| CALG_SCHANNEL_MASTER_HASH | 0x00004c02 | Usado por el sistema Schannel.dll operaciones. Las <strong>ALG_ID</strong> no deben usar este tipo de datos. | 
| CALG_SEAL | 0x00006802 | Algoritmo de cifrado SEAL. Este algoritmo no se admite. | 
| CALG_SHA | 0x00008004 | Algoritmo de hash SHA. Este algoritmo es compatible con el proveedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base de Microsoft</a>. | 
| CALG_SHA1 | 0x00008004 | Igual que <strong>CALG_SHA</strong>. Este algoritmo es compatible con el proveedor <a href="microsoft-base-cryptographic-provider.md">criptográfico base de Microsoft</a>. | 
| CALG_SHA_256 | 0x0000800c | Algoritmo hash SHA de 256 bits. Este algoritmo es compatible con el proveedor criptográfico AES y RSA mejorado de Microsoft. <strong>Windows XP con SP3:</strong> Este algoritmo es compatible con el proveedor criptográfico AES y RSA mejorado de Microsoft (prototipo).<br /><strong>Windows XP con SP2, Windows XP con SP1 y Windows XP:</strong> Este algoritmo no se admite.<br /> | 
| CALG_SHA_384 | 0x0000800d | Algoritmo hash SHA de 384 bits. Este algoritmo es compatible con el proveedor criptográfico AES y RSA mejorado de Microsoft. <strong>Windows XP con SP3:</strong> Este algoritmo es compatible con el proveedor criptográfico AES y RSA mejorado de Microsoft (prototipo).<br /><strong>Windows XP con SP2, Windows XP con SP1 y Windows XP:</strong> Este algoritmo no se admite.<br /> | 
| CALG_SHA_512 | 0x0000800e | Algoritmo hash SHA de 512 bits. Este algoritmo es compatible con el proveedor criptográfico AES y RSA mejorado de Microsoft. <strong>Windows XP con SP3:</strong> Este algoritmo es compatible con el proveedor criptográfico AES y RSA mejorado de Microsoft (prototipo).<br /><strong>Windows XP con SP2, Windows XP con SP1 y Windows XP:</strong> Este algoritmo no se admite.<br /> | 
| CALG_SKIPJACK | 0x0000660a | Algoritmo de cifrado de bloque Skipjack (FORTEZZA). Este algoritmo no se admite. | 
| CALG_SSL2_MASTER | 0x00004c05 | Usado por el sistema Schannel.dll operaciones. Las <strong>ALG_ID</strong> no deben usar este tipo de datos. | 
| CALG_SSL3_MASTER | 0x00004c01 | Usado por el sistema Schannel.dll operaciones. Las <strong>ALG_ID</strong> no deben usar este tipo de datos. | 
| CALG_SSL3_SHAMD5 | 0x00008008 | Usado por el sistema Schannel.dll operaciones. Las <strong>ALG_ID</strong> no deben usar este tipo de datos. | 
| CALG_TEK | 0x0000660b | TEK (FORTEZZA). Este algoritmo no se admite. | 
| CALG_TLS1_MASTER | 0x00004c06 | Usado por el sistema Schannel.dll operaciones. Esta <strong>ALG_ID</strong> no debe usarse en las aplicaciones. | 
| CALG_TLS1PRF | 0x0000800a | Usado por el sistema Schannel.dll operaciones. Esta <strong>ALG_ID</strong> no debe usarse en las aplicaciones. | 




 

Para el proveedor criptográfico base de Microsoft , el proveedor  de servicios criptográficos fuerte de [Microsoft](microsoft-strong-cryptographic-provider.md)y el proveedor de servicios criptográficos mejorado de [Microsoft](microsoft-base-cryptographic-provider.md), el ALG_IDs usado para las especificaciones clave **AT_KEYEXCHANGE** **y AT_SIGNATURE** son los siguientes: [](microsoft-enhanced-cryptographic-provider.md)

-   **CALG_RSA_KEYX** se usa para **AT_KEYEXCHANGE**.
-   **CALG_RSA_SIGN** se usa para **AT_SIGNATURE**.

Para [DSS base](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)de Microsoft y Diffie-Hellman  proveedor criptográfico , los  ALG_IDs que se usan para las especificaciones clave AT_KEYEXCHANGE y **AT_SIGNATURE** son los siguientes:

-   **CALG_DH_SF** se usa para **AT_KEYEXCHANGE**.
-   **CALG_DSS_SIGN** se usa para **AT_SIGNATURE**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de criptografía](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
