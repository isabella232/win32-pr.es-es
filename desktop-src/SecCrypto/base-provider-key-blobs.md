---
description: El proveedor base y el proveedor extendido usan los mismos blobs de clave.
ms.assetid: b4592036-0fa3-4b7e-beed-78cf1d2f39a9
title: Blobs de clave del proveedor base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d95eaeaa1b6438045ebba55d2bb45785e4068154ff51818e937bc434dff7fb29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773047"
---
# <a name="base-provider-key-blobs"></a>Blobs de clave del proveedor base

El proveedor base y el proveedor extendido usan los mismos [*blobs de clave.*](../secgloss/k-gly.md)

-   [Blobs de clave pública](#public-key-blobs)
-   [Blobs de clave privada](#private-key-blobs)
-   [Blobs de clave simples](#simple-key-blobs)

## <a name="public-key-blobs"></a>Blobs de clave pública

[*Los BLOB de clave pública*](../secgloss/p-gly.md), tipo **PUBLICKEYBLOB,** se usan para almacenar claves públicas fuera de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP). [](../secgloss/p-gly.md) Los blobs de clave pública del proveedor base tienen el formato siguiente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente de clave pública. Todos los valores están en [*formato little-endian.*](../secgloss/l-gly.md)



| Campo          | Descripción                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulus        | Los datos de módulo de clave pública se encuentran directamente después de [**la estructura RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) El tamaño de estos datos variará en función del tamaño de la clave pública. El número de bytes se puede determinar dividiendo el valor del campo **bitlen RSAPUBKEY** entre ocho. |
| publickeystruc | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                 |
| rsapubkey      | Estructura [**RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) El **miembro** mágico debe establecerse en 0x31415352. Este valor hexadecimal es la [*codificación ASCII*](../secgloss/a-gly.md) de RSA1.                                                                         |



 

> [!Note]  
> Los blobs de clave pública no están cifrados. Contienen claves públicas en [*formato de texto*](../secgloss/p-gly.md) no cifrado.

 

## <a name="private-key-blobs"></a>Blobs de clave privada

[*Los blobs de clave privada*](../secgloss/p-gly.md), tipo **PRIVATEKEYBLOB,** se usan para almacenar [*claves privadas*](../secgloss/p-gly.md) fuera de un CSP. Los blobs de clave privada del proveedor base tienen el formato siguiente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

En la tabla siguiente se describe el componente BLOB de clave privada.

> [!Note]  
> Estos campos corresponden a los campos descritos en la sección 7.2 de [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1 con pequeñas diferencias.

 



| Campo           | Descripción                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coeficiente     | Coeficiente. Tiene un valor numérico de (inverso de q) mod p.                                                                                                                                                |
| exponent1       | Exponente 1. Tiene un valor numérico de d mod (p – 1).                                                                                                                                                        |
| exponent2       | Exponente 2. Tiene un valor numérico de d mod (q – 1).                                                                                                                                                        |
| Modulus         | Módulo. Tiene un valor de *Prime1 ×**Prime2* y a menudo se conoce como n.                                                                                                                                   |
| prime1          | Número primo 1, conocido a menudo como p.                                                                                                                                                                             |
| prime2          | Número primo 2, a menudo conocido como q.                                                                                                                                                                             |
| privateExponent | Exponente privado, conocido a menudo como d.                                                                                                                                                                           |
| publickeystruc  | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                         |
| rsapubkey       | Estructura [**RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) El **miembro** mágico debe establecerse en 0x32415352. Este valor hexadecimal es la [*codificación ASCII*](../secgloss/a-gly.md) de RSA2. |



 

> [!Note]  
> Los blobs de clave privada no están cifrados. Contienen claves privadas en formato de texto no cifrado.

 

Al llamar [**a CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)el desarrollador puede elegir si cifrar la clave. **PrivateKEYBLOB se** cifra si el *parámetro hExpKey* contiene un identificador válido para una clave de sesión. Todo menos la [**parte PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrada.

> [!Note]  
> El algoritmo de cifrado y los parámetros de clave de cifrado no se almacenan junto con el blob de clave privada. La aplicación debe administrar y almacenar esta información. Si se pasa cero para *hExpKey*, la clave privada se exportará sin cifrado.

 

> [!Caution]  
> Es peligroso exportar claves privadas sin cifrado porque, a continuación, son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.

 

## <a name="simple-key-blobs"></a>Blobs de clave simples

[*Los blobs de clave simples*](../secgloss/s-gly.md), tipo **SIMPLEBLOB,** se usan para almacenar y transportar claves de sesión fuera de un CSP. Los blobs de clave simple del proveedor base siempre se cifran con una [*clave pública de intercambio de claves*](../secgloss/k-gly.md). El **miembro pbData** de **SIMPLEBLOB** es una secuencia de bytes en el formato siguiente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente del **miembro pbData** de **SIMPLEBLOB.**



| Campo          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Estructura [**de identificador \_ de ALG**](alg-id.md) que especifica el algoritmo de cifrado utilizado para cifrar los datos de clave de sesión. Normalmente, tiene un valor de CALG \_ RSA KEYX, que indica que los datos de la clave de sesión se cifraron con una clave pública de intercambio de claves mediante el algoritmo \_ de clave pública [*RSA*](../secgloss/r-gly.md).                                                                                                                           |
| encryptedkey   | Secuencia **BYTE** que representa los datos de clave de sesión cifrados en forma de un bloque de cifrado PKCS \# 1, tipo 2. Para obtener información sobre este formato de datos, vea Public Key Cryptography Standards (PKCS) \# 1, publicado por RSA Data Security, Inc. Estos datos siempre tienen el mismo tamaño que el módulo de la clave pública. Por ejemplo, las claves públicas generadas por el proveedor base RSA de Microsoft pueden tener una longitud de 512 bits (64 bytes), por lo que los datos de la clave de sesión cifrada también tienen siempre 512 bits (64 bytes).<br/> |
| publickeystruc | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

 

 
