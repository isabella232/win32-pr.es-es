---
description: Los blobs se usan con el proveedor RSA/Schannel para exportar claves del proveedor de servicios criptográficos (CSP) e importar claves en él.
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: BLOB de clave RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be8bfa8b87ee901317e220583ff7b08ea110e342a2d9dd9abb477053ffdf05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900540"
---
# <a name="rsaschannel-key-blobs"></a>BLOB de clave RSA/Schannel

[*Los blobs se*](../secgloss/b-gly.md) usan con el proveedor [*rsa*](../secgloss/r-gly.md)Schannel para exportar claves desde el proveedor de servicios / [](../secgloss/s-gly.md) [*criptográficos*](../secgloss/c-gly.md) (CSP) e importar claves en él.

-   [Blobs de clave pública](#public-key-blobs)
-   [Blobs de clave privada](#private-key-blobs)
-   [Blobs de clave simple](#simple-key-blobs)

## <a name="public-key-blobs"></a>Blobs de clave pública

[*Los BLOB de clave pública,*](../secgloss/p-gly.md)tipo **PUBLICKEYBLOB,** se usan para almacenar [*claves públicas.*](../secgloss/p-gly.md) Estas claves se exportan e importan como una secuencia de bytes con el formato siguiente.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente de clave pública. Todos los valores están en [*formato little-endian.*](../secgloss/l-gly.md)



| Campo          | Descripción                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulus        | Secuencia **BYTE.** Los datos del módulo de clave pública se encuentran directamente después de la **estructura RSAPUBKEY.** La longitud de estos datos varía en función de la longitud de la clave pública. El número de bytes se puede determinar dividiendo el valor del miembro **bitlen** de **RSAPUBKEY** entre ocho. |
| publickeystruc | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                              |
| rsapubkey      | Estructura [**RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) El **miembro** mágico debe establecerse en 0x31415352. Este valor hexadecimal es la [*codificación ASCII*](../secgloss/a-gly.md) de RSA1.                                                                                      |



 

> [!Note]  
> Los BLOB de clave pública no están cifrados. Contienen claves públicas en [*formato de texto*](../secgloss/p-gly.md) no cifrado.

 

## <a name="private-key-blobs"></a>Blobs de clave privada

[*Los BLOB de clave privada,*](../secgloss/p-gly.md)tipo **PRIVATEKEYBLOB,** se usan para almacenar pares de claves pública [*y privada.*](../secgloss/p-gly.md) Estas claves se exportan e importan como una secuencia de bytes con el formato siguiente.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

Si el [*blob de clave*](../secgloss/k-gly.md) está cifrado, se cifran todos los elementos, menos la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB.

> [!Note]  
> El algoritmo de cifrado y los parámetros de clave de cifrado no se almacenan junto con el blob de clave privada. Es responsabilidad de la aplicación administrar esta información.

 

En la tabla siguiente se describe cada componente BLOB de clave privada.

> [!Note]  
> Estos campos corresponden a los campos descritos en la sección 7.2 de [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1 con pequeñas diferencias.

 



| Campo           | Descripción                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| exponent1       | Secuencia **BYTE.** Primer exponente. Tiene un valor numérico de d mod (p – 1).                                                                                                                           |
| exponent2       | Secuencia **BYTE.** Segundo exponente. Tiene un valor numérico de d mod (q – 1).                                                                                                                          |
| Coeficiente     | Secuencia **BYTE.** Coeficiente. Tiene un valor numérico de (inverso de q) mod p.                                                                                                                           |
| Modulus         | Secuencia **BYTE.** Módulo. Tiene una cadena que contiene *Prime1* \* *Prime2.* A menudo se conoce como n.                                                                                               |
| prime1          | Secuencia **BYTE.** Número primo 1, conocido a menudo como p.                                                                                                                                                        |
| prime2          | Secuencia **BYTE.** Número primo 2, conocido a menudo como q.                                                                                                                                                        |
| publickeystruc  | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                         |
| privateExponent | Secuencia **BYTE.** Exponente privado, conocido a menudo como d.                                                                                                                                                  |
| rsapubkey       | Estructura [**RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) El **miembro** mágico debe establecerse en 0x32415352. Este valor hexadecimal es la [*codificación ASCII*](../secgloss/a-gly.md) de RSA2. |



 

> [!Note]  
> Los BLOB de clave privada no están cifrados. Contienen claves privadas en formato de texto no cifrado.

 

Al llamar [**a CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)el desarrollador puede elegir si cifrar la clave. **PrivateKEYBLOB se** cifra si el *parámetro hExpKey* contiene un identificador válido para una clave de sesión. Todo menos [**la parte PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrada.

> [!Note]  
> El algoritmo de cifrado y los parámetros de clave de cifrado no se almacenan junto con el blob de clave privada. La aplicación debe administrar y almacenar esta información. Si se pasa cero para *hExpKey,* la clave privada se exportará sin cifrado.

 

> [!Caution]  
> Es peligroso exportar claves privadas sin cifrado porque, a continuación, son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.

 

## <a name="simple-key-blobs"></a>Blobs de clave simple

[*Los BLOB de clave simple,*](../secgloss/s-gly.md)tipo **SIMPLEBLOB,** se usan para almacenar y transportar claves de sesión. Siempre se cifran con una [*clave pública de intercambio de claves*](../secgloss/k-gly.md). Estas claves se exportan e importan como una secuencia de bytes con el formato siguiente.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente BLOB simple.



| Campo          | Descripción                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Estructura [**de id. \_ de ALG.**](alg-id.md) Normalmente, especifica el algoritmo CALG RSA KEYX, que indica que los datos de clave de sesión se cifraron con una clave pública de intercambio de claves, mediante el algoritmo de clave pública \_ \_ [*RSA*](../secgloss/r-gly.md). |
| encryptedkey   | Secuencia **BYTE.** Los datos de clave de sesión cifrados tienen el formato de un bloque de cifrado PKCS \# 1, tipo 2. Para obtener información sobre este formato de datos, consulte Public Key Cryptography Standards (PKCS), publicado por RSA Data Security, Inc.                                                                                     |
| publickeystruc | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                         |



 

Estos datos siempre tienen el mismo tamaño que el módulo de la clave pública. Por ejemplo, las claves públicas generadas por el proveedor criptográfico base de Microsoft siempre tienen una longitud de 512 bits (64 bytes), por lo que los datos de la clave de sesión cifrada también tienen siempre 64 bytes.

 

 
