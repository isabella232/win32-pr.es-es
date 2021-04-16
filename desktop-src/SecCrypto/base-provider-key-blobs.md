---
description: El proveedor base y el proveedor extendido utilizan los mismos blobs de clave.
ms.assetid: b4592036-0fa3-4b7e-beed-78cf1d2f39a9
title: Blobs de clave de proveedor base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c763f97fe6e7868246e0bce30ee2a741e8bd212f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666534"
---
# <a name="base-provider-key-blobs"></a>Blobs de clave de proveedor base

El proveedor base y el proveedor extendido utilizan los mismos [*blobs de clave*](../secgloss/k-gly.md).

-   [Blobs de clave pública](#public-key-blobs)
-   [Blobs de clave privada](#private-key-blobs)
-   [Blobs de clave simple](#simple-key-blobs)

## <a name="public-key-blobs"></a>Blobs de clave pública

Los [*blobs de clave pública*](../secgloss/p-gly.md), tipo **PUBLICKEYBLOB**, se usan para almacenar [*claves públicas*](../secgloss/p-gly.md) fuera de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP). Los blobs de clave pública del proveedor base tienen el siguiente formato.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente de clave pública. Todos los valores están en formato [*Little-Endian*](../secgloss/l-gly.md) .



| Campo          | Descripción                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulus        | Los datos del módulo de clave pública se encuentran directamente después de la estructura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . El tamaño de estos datos variará en función del tamaño de la clave pública. El número de bytes se puede determinar dividiendo el valor del campo **bitlen de RSAPUBKEY** por ocho. |
| publickeystruc | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                 |
| rsapubkey      | Estructura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . El miembro **mágico** debe establecerse en 0x31415352. Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de rsa1.                                                                         |



 

> [!Note]  
> No se cifran los blobs de clave pública. Contienen claves públicas en formato de [*texto simple*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>Blobs de clave privada

Los [*blobs de clave privada*](../secgloss/p-gly.md), tipo **PRIVATEKEYBLOB**, se usan para almacenar [*claves privadas*](../secgloss/p-gly.md) fuera de un CSP. Los blobs de clave privada del proveedor base tienen el siguiente formato.

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
> Estos campos se corresponden con los campos que se describen en la sección 7,2 de [*estándares de criptografía de clave pública*](../secgloss/p-gly.md) (PKCS) \# 1 con pequeñas diferencias.

 



| Campo           | Descripción                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| coeficiente     | Coeficiente. Esto tiene un valor numérico de (inverso de q) mod p.                                                                                                                                                |
| exponent1       | Exponente 1. Este tiene un valor numérico de d mod (p – 1).                                                                                                                                                        |
| exponent2       | Exponente 2. Este tiene un valor numérico de d mod (q – 1).                                                                                                                                                        |
| Modulus         | El módulo. Esto tiene un valor de *Prime1*×*Prime2* y a menudo se conoce como n.                                                                                                                                   |
| prime1          | Número primo 1, que a menudo se conoce como p.                                                                                                                                                                             |
| prime2          | Número primo 2, que a menudo se conoce como q.                                                                                                                                                                             |
| privateExponent | Exponente privado, que a menudo se conoce como d.                                                                                                                                                                           |
| publickeystruc  | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                         |
| rsapubkey       | Estructura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . El miembro **mágico** debe establecerse en 0x32415352. Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de RSA2. |



 

> [!Note]  
> No se cifran los blobs de clave privada. Contienen claves privadas en formato de texto simple.

 

Al llamar a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), el desarrollador puede elegir si desea cifrar la clave. El **PRIVATEKEYBLOB** se cifra si el parámetro *hExpKey* contiene un identificador válido para una clave de sesión. Todo excepto la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrado.

> [!Note]  
> Los parámetros de algoritmo de cifrado y clave de cifrado no se almacenan junto con el BLOB de clave privada. La aplicación debe administrar y almacenar esta información. Si se pasa cero para *hExpKey*, la clave privada se exportará sin cifrado.

 

> [!Caution]  
> Es peligroso exportar las claves privadas sin cifrado, ya que son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.

 

## <a name="simple-key-blobs"></a>Blobs de clave simple

Los [*blobs de clave simple*](../secgloss/s-gly.md), Type **SIMPLEBLOB**, se usan para almacenar y transportar claves de sesión fuera de un CSP. Los blobs de clave simple del proveedor base siempre se cifran con una [*clave pública de intercambio de claves*](../secgloss/k-gly.md). El miembro **pbData** de **SIMPLEBLOB** es una secuencia de bytes con el siguiente formato.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente del miembro **pbData** de **SIMPLEBLOB**.



| Campo          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Una estructura de [**\_ identificador de alg**](alg-id.md) que especifica el algoritmo de cifrado que se usa para cifrar los datos de la clave de sesión. Normalmente, tiene un valor de CALG \_ RSA \_ KEYX, que indica que los datos de la clave de sesión se cifraron con una clave pública de intercambio de claves mediante el [*algoritmo de clave pública RSA*](../secgloss/r-gly.md).                                                                                                                           |
| EncryptedKey   | Secuencia de **bytes** que representa los datos de clave de sesión cifrada con el formato de un \# bloque de cifrado PKCS 1, tipo 2. Para obtener información acerca de este formato de datos, consulte los estándares de criptografía de clave pública (PKCS) \# 1, publicados por RSA Data Security, Inc. Estos datos tienen siempre el mismo tamaño que el módulo de la clave pública. Por ejemplo, las claves públicas generadas por el proveedor base de RSA de Microsoft pueden tener una longitud de 512 bits (64 bytes), por lo que los datos de la clave de sesión cifrada también tienen siempre 512 bits (64 bytes).<br/> |
| publickeystruc | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

 

 
