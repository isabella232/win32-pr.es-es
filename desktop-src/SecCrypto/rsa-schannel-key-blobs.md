---
description: Los blobs se utilizan con el proveedor de RSA/Schannel para exportar claves del proveedor de servicios criptográficos (CSP) e importarlas en él.
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: Blobs de clave RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea26a98e9c2925442166eb28245ebc471b1749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908081"
---
# <a name="rsaschannel-key-blobs"></a>Blobs de clave RSA/Schannel

Los [*blobs*](../secgloss/b-gly.md) se utilizan con el proveedor de Schannel de [*RSA*](../secgloss/r-gly.md) / [](../secgloss/s-gly.md) para exportar claves desde el proveedor de [*servicios de cifrado*](../secgloss/c-gly.md) (CSP) e importarlas en él.

-   [Blobs de clave pública](#public-key-blobs)
-   [Blobs de clave privada](#private-key-blobs)
-   [Blobs de clave simple](#simple-key-blobs)

## <a name="public-key-blobs"></a>Blobs de clave pública

Los [*blobs de clave pública*](../secgloss/p-gly.md), tipo **PUBLICKEYBLOB**, se usan para almacenar [*claves públicas*](../secgloss/p-gly.md). Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente de clave pública. Todos los valores están en formato [*Little-Endian*](../secgloss/l-gly.md) .



| Campo          | Descripción                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulus        | Secuencia de **bytes** . Los datos del módulo de clave pública se encuentran directamente después de la estructura **RSAPUBKEY** . La longitud de estos datos varía en función de la longitud de la clave pública. El número de bytes se puede determinar dividiendo el valor del miembro **bitlen** de **RSAPUBKEY** por ocho. |
| publickeystruc | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                              |
| rsapubkey      | Estructura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . El miembro **mágico** debe establecerse en 0x31415352. Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de rsa1.                                                                                      |



 

> [!Note]  
> No se cifran los blobs de clave pública. Contienen claves públicas en formato de [*texto simple*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>Blobs de clave privada

Los [*blobs de clave privada*](../secgloss/p-gly.md), tipo **PRIVATEKEYBLOB**, se usan para almacenar [*pares de claves pública y privada*](../secgloss/p-gly.md). Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.

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

Si el [*BLOB de clave*](../secgloss/k-gly.md) está cifrado, se cifra todo excepto la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB.

> [!Note]  
> Los parámetros de algoritmo de cifrado y clave de cifrado no se almacenan junto con el BLOB de clave privada. Es responsabilidad de la aplicación administrar esta información.

 

En la tabla siguiente se describe cada componente de BLOB de clave privada.

> [!Note]  
> Estos campos se corresponden con los campos que se describen en la sección 7,2 de [*estándares de criptografía de clave pública*](../secgloss/p-gly.md) (PKCS) \# 1 con pequeñas diferencias.

 



| Campo           | Descripción                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| exponent1       | Secuencia de **bytes** . Primer exponente. Este tiene un valor numérico de d mod (p – 1).                                                                                                                           |
| exponent2       | Secuencia de **bytes** . Segundo exponente. Este tiene un valor numérico de d mod (q – 1).                                                                                                                          |
| coeficiente     | Secuencia de **bytes** . Coeficiente. Esto tiene un valor numérico de (inverso de q) mod p.                                                                                                                           |
| Modulus         | Secuencia de **bytes** . El módulo. Tiene una cadena que contiene *Prime1* \* *Prime2*. A menudo se conoce como n.                                                                                               |
| prime1          | Secuencia de **bytes** . Número primo 1, que a menudo se conoce como p.                                                                                                                                                        |
| prime2          | Secuencia de **bytes** . Número primo 2, que a menudo se conoce como q.                                                                                                                                                        |
| publickeystruc  | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                         |
| privateExponent | Secuencia de **bytes** . Exponente privado, que a menudo se conoce como d.                                                                                                                                                  |
| rsapubkey       | Estructura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . El miembro **mágico** debe establecerse en 0x32415352. Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de RSA2. |



 

> [!Note]  
> No se cifran los blobs de clave privada. Contienen claves privadas en formato de texto simple.

 

Al llamar a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), el desarrollador puede elegir si desea cifrar la clave. El **PRIVATEKEYBLOB** se cifra si el parámetro *hExpKey* contiene un identificador válido para una clave de sesión. Todo excepto la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrado.

> [!Note]  
> Los parámetros de algoritmo de cifrado y clave de cifrado no se almacenan junto con el BLOB de clave privada. La aplicación debe administrar y almacenar esta información. Si se pasa cero para *hExpKey*, la clave privada se exportará sin cifrado.

 

> [!Caution]  
> Es peligroso exportar las claves privadas sin cifrado, ya que son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.

 

## <a name="simple-key-blobs"></a>Blobs de clave simple

Los [*blobs de clave simple*](../secgloss/s-gly.md), Type **SIMPLEBLOB**, se usan para almacenar y transportar claves de sesión. Siempre se cifran con una [*clave pública de intercambio de claves*](../secgloss/k-gly.md). Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente de BLOB simple.



| Campo          | Descripción                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Una estructura de [**\_ identificador de alg**](alg-id.md) . Normalmente, esto especifica el \_ algoritmo CALG RSA \_ KEYX, que indica que los datos de la clave de sesión se cifraron con una clave pública de intercambio de claves, mediante el [*algoritmo de clave pública RSA*](../secgloss/r-gly.md). |
| EncryptedKey   | Secuencia de **bytes** . Los datos de la clave de sesión cifrada tienen el formato de un \# bloque de cifrado PKCS 1, tipo 2. Para obtener información sobre este formato de datos, consulte los estándares de criptografía de clave pública (PKCS) publicados por RSA Data Security, Inc.                                                                                     |
| publickeystruc | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                         |



 

Estos datos tienen siempre el mismo tamaño que el módulo de la clave pública. Por ejemplo, las claves públicas generadas por el proveedor de servicios criptográficos de base de Microsoft son siempre de 512 bits (64 bytes) de longitud, por lo que los datos de clave de sesión cifrada también tienen siempre 64 bytes.

 

 
