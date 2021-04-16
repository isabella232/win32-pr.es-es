---
description: Especifica un identificador de algoritmo.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669899"
---
# <a name="alg_id"></a>ALG_ID

El tipo de datos **ALG_ID** especifica un identificador de algoritmo. Los parámetros de este tipo de datos se pasan a la mayoría de las funciones de CryptoAPI.


```C++
typedef unsigned int ALG_ID;
```



En la tabla siguiente se enumeran los identificadores de algoritmo que están definidos actualmente. Los autores de [*proveedores de servicios criptográficos*](../secgloss/c-gly.md) (CSP) personalizados pueden definir nuevos valores. Además, la **ALG_ID** que usan los CSP personalizados para las especificaciones clave **AT_KEYEXCHANGE** y **AT_SIGNATURE** dependen del proveedor. Las asignaciones actuales siguen a la tabla.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificador</th>
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CALG_3DES</td>
<td>0x00006603</td>
<td>Algoritmo de cifrado <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> .</td>
</tr>
<tr class="even">
<td>CALG_3DES_112</td>
<td>0x00006609</td>
<td>Cifrado <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> de dos claves con una longitud de clave efectiva igual a 112 bits.</td>
</tr>
<tr class="odd">
<td>CALG_AES</td>
<td>0x00006611</td>
<td>Estándar de cifrado avanzado (AES). Este algoritmo es compatible con el <a href="microsoft-aes-cryptographic-provider.md">proveedor de servicios criptográficos AES de Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_AES_128</td>
<td>0x0000660e</td>
<td>AES de 128 bits. Este algoritmo es compatible con el <a href="microsoft-aes-cryptographic-provider.md">proveedor de servicios criptográficos AES de Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_AES_192</td>
<td>0x0000660f</td>
<td>AES de 192 bits. Este algoritmo es compatible con el <a href="microsoft-aes-cryptographic-provider.md">proveedor de servicios criptográficos AES de Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_AES_256</td>
<td>0x00006610</td>
<td>AES de 256 bits. Este algoritmo es compatible con el <a href="microsoft-aes-cryptographic-provider.md">proveedor de servicios criptográficos AES de Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_AGREEDKEY_ANY</td>
<td>0x0000aa03</td>
<td>Identificador de algoritmo temporal para los identificadores de Diffie-Hellman: claves acordadas.</td>
</tr>
<tr class="even">
<td>CALG_CYLINK_MEK</td>
<td>0x0000660c</td>
<td>Un algoritmo para crear una clave DES de 40 bits con bits de paridad y bits de clave con ceros para que la longitud de la clave sea 64 bits. Este algoritmo es compatible con el <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_DES</td>
<td>0x00006601</td>
<td>Algoritmo de cifrado DES.</td>
</tr>
<tr class="even">
<td>CALG_DESX</td>
<td>0x00006604</td>
<td>Algoritmo de cifrado DESX.</td>
</tr>
<tr class="odd">
<td>CALG_DH_EPHEM</td>
<td>0x0000aa02</td>
<td>Algoritmo de intercambio de claves efímeras Diffie-Hellman.</td>
</tr>
<tr class="even">
<td>CALG_DH_SF</td>
<td>0x0000aa01</td>
<td>Diffie-Hellman el algoritmo de intercambio de claves de almacenamiento y reenvío.</td>
</tr>
<tr class="odd">
<td>CALG_DSS_SIGN</td>
<td>0x00002200</td>
<td>Algoritmo de firma de <a href="/windows/desktop/SecGloss/p-gly"><em>clave pública</em></a> DSA.</td>
</tr>
<tr class="even">
<td>CALG_ECDH</td>
<td>0x0000aa05</td>
<td>Algoritmo de intercambio de claves de curva elíptica Diffie-Hellman.
<blockquote>
[!Note]<br />
Este algoritmo solo se admite a través de <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.
</blockquote>
<br/> <strong>Windows Server 2003 y Windows XP:</strong> Este algoritmo no es compatible.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECDH_EPHEM</td>
<td>0x0000ae06</td>
<td>Curva elíptica efímera Diffie-Hellman algoritmo de intercambio de claves.
<blockquote>
[!Note]<br />
Este algoritmo solo se admite a través de <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.
</blockquote>
<br/> <strong>Windows Server 2003 y Windows XP:</strong> Este algoritmo no es compatible.<br/></td>
</tr>
<tr class="even">
<td>CALG_ECDSA</td>
<td>0x00002203</td>
<td>Algoritmo de firma digital de curva elíptica.
<blockquote>
[!Note]<br />
Este algoritmo solo se admite a través de <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.
</blockquote>
<br/> <strong>Windows Server 2003 y Windows XP:</strong> Este algoritmo no es compatible.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECMQV</td>
<td>0x0000a001</td>
<td>Algoritmo de intercambio de claves de curva elíptica Menezes, qu y Vanstone (MQV). Este algoritmo no es compatible.</td>
</tr>
<tr class="even">
<td>CALG_HASH_REPLACE_OWF</td>
<td>0x0000800b</td>
<td>Algoritmo hash de función unidireccional.</td>
</tr>
<tr class="odd">
<td>CALG_HUGHES_MD5</td>
<td>0x0000a003</td>
<td>Algoritmo hash de Hughes MD5.</td>
</tr>
<tr class="even">
<td>CALG_HMAC</td>
<td>0x00008009</td>
<td>Algoritmo hash con clave HMAC. Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_KEA_KEYX</td>
<td>0x0000aa04</td>
<td>Algoritmo de intercambio de claves de KEA (FORTEZZA). Este algoritmo no es compatible.</td>
</tr>
<tr class="even">
<td>CALG_MAC</td>
<td>0x00008005</td>
<td>Algoritmo hash con clave de <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> . Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_MD2</td>
<td>0x00008001</td>
<td>Algoritmo de hash MD2. Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_MD4</td>
<td>0x00008002</td>
<td>Algoritmo de hash MD4.</td>
</tr>
<tr class="odd">
<td>CALG_MD5</td>
<td>0x00008003</td>
<td>Algoritmo de hash MD5. Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_NO_SIGN</td>
<td>0x00002000</td>
<td>No hay ningún algoritmo de firma.</td>
</tr>
<tr class="odd">
<td>CALG_OID_INFO_CNG_ONLY</td>
<td>0xFFFFFFFF</td>
<td>El algoritmo solo se implementa en CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, se puede usar para determinar si un algoritmo de criptografía solo se admite mediante las funciones de CNG.</td>
</tr>
<tr class="even">
<td>CALG_OID_INFO_PARAMETERS</td>
<td>0xfffffffe</td>
<td>El algoritmo se define en los parámetros codificados. El algoritmo solo se admite mediante CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, se puede usar para determinar si un algoritmo de criptografía solo se admite mediante las funciones de CNG.</td>
</tr>
<tr class="odd">
<td>CALG_PCT1_MASTER</td>
<td>0x00004c04</td>
<td>Lo usa el sistema de operaciones de Schannel.dll. Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</td>
</tr>
<tr class="even">
<td>CALG_RC2</td>
<td>0x00006602</td>
<td>Algoritmo de cifrado de bloques RC2. Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_RC4</td>
<td>0x00006801</td>
<td>Algoritmo de cifrado de flujo RC4. Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_RC5</td>
<td>0x0000660d</td>
<td>Algoritmo de cifrado de bloque RC5.</td>
</tr>
<tr class="odd">
<td>CALG_RSA_KEYX</td>
<td>0x0000a400</td>
<td>Algoritmo de intercambio de claves públicas RSA. Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_RSA_SIGN</td>
<td>0x00002400</td>
<td>Algoritmo de firma de clave pública RSA. Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_ENC_KEY</td>
<td>0x00004c07</td>
<td>Lo usa el sistema de operaciones de Schannel.dll. Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</td>
</tr>
<tr class="even">
<td>CALG_SCHANNEL_MAC_KEY</td>
<td>0x00004c03</td>
<td>Lo usa el sistema de operaciones de Schannel.dll. Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_MASTER_HASH</td>
<td>0x00004c02</td>
<td>Lo usa el sistema de operaciones de Schannel.dll. Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</td>
</tr>
<tr class="even">
<td>CALG_SEAL</td>
<td>0x00006802</td>
<td>El algoritmo de cifrado de sellado. Este algoritmo no es compatible.</td>
</tr>
<tr class="odd">
<td>CALG_SHA</td>
<td>0x00008004</td>
<td>Algoritmo de hash SHA. Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_SHA1</td>
<td>0x00008004</td>
<td>Igual que <strong>CALG_SHA</strong>. Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_SHA_256</td>
<td>0x0000800c</td>
<td>algoritmo hash SHA 256 bits. Este algoritmo es compatible con el proveedor de servicios criptográficos RSA y AES mejorado de Microsoft. <strong>Windows XP con SP3:</strong> Este algoritmo es compatible con el proveedor de servicios criptográficos (Prototype) de AES y RSA mejorado de Microsoft.<br/> <strong>Windows XP con SP2, Windows XP con SP1 y Windows XP:</strong> Este algoritmo no es compatible.<br/></td>
</tr>
<tr class="even">
<td>CALG_SHA_384</td>
<td>0x0000800d</td>
<td>algoritmo hash SHA 384 bits. Este algoritmo es compatible con el proveedor de servicios criptográficos RSA y AES mejorado de Microsoft. <strong>Windows XP con SP3:</strong> Este algoritmo es compatible con el proveedor de servicios criptográficos (Prototype) de AES y RSA mejorado de Microsoft.<br/> <strong>Windows XP con SP2, Windows XP con SP1 y Windows XP:</strong> Este algoritmo no es compatible.<br/></td>
</tr>
<tr class="odd">
<td>CALG_SHA_512</td>
<td>0x0000800e</td>
<td>algoritmo hash SHA 512 bits. Este algoritmo es compatible con el proveedor de servicios criptográficos RSA y AES mejorado de Microsoft. <strong>Windows XP con SP3:</strong> Este algoritmo es compatible con el proveedor de servicios criptográficos (Prototype) de AES y RSA mejorado de Microsoft.<br/> <strong>Windows XP con SP2, Windows XP con SP1 y Windows XP:</strong> Este algoritmo no es compatible.<br/></td>
</tr>
<tr class="even">
<td>CALG_SKIPJACK</td>
<td>0x0000660a</td>
<td>Algoritmo de cifrado de bloque Skipjack (FORTEZZA). Este algoritmo no es compatible.</td>
</tr>
<tr class="odd">
<td>CALG_SSL2_MASTER</td>
<td>0x00004c05</td>
<td>Lo usa el sistema de operaciones de Schannel.dll. Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</td>
</tr>
<tr class="even">
<td>CALG_SSL3_MASTER</td>
<td>0x00004c01</td>
<td>Lo usa el sistema de operaciones de Schannel.dll. Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</td>
</tr>
<tr class="odd">
<td>CALG_SSL3_SHAMD5</td>
<td>0x00008008</td>
<td>Lo usa el sistema de operaciones de Schannel.dll. Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</td>
</tr>
<tr class="even">
<td>CALG_TEK</td>
<td>0x0000660b</td>
<td>TEK (FORTEZZA). Este algoritmo no es compatible.</td>
</tr>
<tr class="odd">
<td>CALG_TLS1_MASTER</td>
<td>0x00004c06</td>
<td>Lo usa el sistema de operaciones de Schannel.dll. Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</td>
</tr>
<tr class="even">
<td>CALG_TLS1PRF</td>
<td>0x0000800a</td>
<td>Lo usa el sistema de operaciones de Schannel.dll. Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</td>
</tr>
</tbody>
</table>



 

Para el proveedor de servicios criptográficos [básicos](microsoft-base-cryptographic-provider.md)de Microsoft, el [proveedor de servicios](microsoft-strong-cryptographic-provider.md)criptográficos seguros de Microsoft y el [proveedor de servicios criptográficos mejorados de Microsoft](microsoft-enhanced-cryptographic-provider.md), los **ALG_IDs** que se usan para las especificaciones clave **AT_KEYEXCHANGE** y **AT_SIGNATURE** son los siguientes:

-   **CALG_RSA_KEYX** se utiliza para **AT_KEYEXCHANGE**.
-   **CALG_RSA_SIGN** se utiliza para **AT_SIGNATURE**.

En el caso de [Microsoft base DSS y Diffie-Hellman proveedor de servicios criptográficos](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), el **ALG_IDs** que se usa para las especificaciones clave **AT_KEYEXCHANGE** y **AT_SIGNATURE** son los siguientes:

-   **CALG_DH_SF** se utiliza para **AT_KEYEXCHANGE**.
-   **CALG_DSS_SIGN** se utiliza para **AT_SIGNATURE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de criptografía](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
