---
description: Los blobs se utilizan con el proveedor de Diffie-Hellman para exportar las claves del proveedor de servicios de cifrado (CSP) e importarlas en él.
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Diffie-Hellman blobs de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667190"
---
# <a name="diffie-hellman-key-blobs"></a>Diffie-Hellman blobs de clave

Los [*blobs*](../secgloss/b-gly.md) se utilizan con el proveedor de [*Diffie-Hellman*](../secgloss/d-gly.md) para exportar claves desde el [*proveedor de servicios de cifrado*](../secgloss/c-gly.md) (CSP) e importarlas en él.

-   [Blobs de clave pública](#public-key-blobs)
-   [Blobs de clave privada](#private-key-blobs)

## <a name="public-key-blobs"></a>Blobs de clave pública

Diffie-Hellman los [*blobs de clave pública*](../secgloss/p-gly.md), tipo **PUBLICKEYBLOB**, se usan para intercambiar el valor de mod P (G ^ X) en un intercambio de claves Diffie-Hellman. Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

En la tabla siguiente se describe cada componente del [*BLOB de clave*](../secgloss/k-gly.md).



| Campo          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . El miembro **mágico** debe establecerse en 0x31484400. Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de "DH1".                                                                                                                                                                                                                                                                                                                                                                 |
| publickeystruc | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| y              | Secuencia de **bytes** . El valor Y, (G ^ X) mod P, se encuentra directamente después de la estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) y siempre debe ser la longitud, en bytes, del campo **DHPUBKEY bitlen** (longitud de bit de P) dividido entre ocho. Si la longitud de los datos resultante del cálculo de (G ^ X) mod P es uno o varios bytes más cortos que P divididos por ocho, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato [*Little-Endian*](../secgloss/l-gly.md) ). |



 

## <a name="private-key-blobs"></a>Blobs de clave privada

Diffie-Hellman los [*blobs de clave privada*](../secgloss/p-gly.md), escriba **PRIVATEKEYBLOB**, se usan para almacenar la información pública o privada de una clave de Diffie-Hellman. Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente del BLOB de clave.



| Campo          | Descripción                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . El miembro **mágico** debe establecerse en 0x32484400. Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de "DH2". |
| generador      | Secuencia de **bytes** . El generador, G.                                                                                                                                                                       |
| publickeystruc | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                        |
| principal          | Secuencia de **bytes** . El módulo primo, P. Estos datos siempre deben tener el bit más significativo establecido en uno.                                                                      |
| secret         | Secuencia de **bytes** . El exponente secreto, X.                                                                                                                                                                 |



 

> [!Note]  
> El generador y el secreto deben tener siempre la misma longitud, en bytes. Si es un byte o más corto que el otro, se debe rellenar con el número necesario de bytes de valor cero para que sean iguales. Tanto el generador como el secreto están en formato [*Little-Endian*](../secgloss/l-gly.md) .

 

 

 
