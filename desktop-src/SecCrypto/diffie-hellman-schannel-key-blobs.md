---
description: Los blobs se utilizan con el proveedor de Diffie-Hellman/Schannel para exportar claves desde el proveedor de servicios criptográficos (CSP) e importarlas en él.
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: Blobs de clave Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813739"
---
# <a name="diffie-hellmanschannel-key-blobs"></a>Blobs de clave Diffie-Hellman/Schannel

Los [*blobs*](../secgloss/b-gly.md) se utilizan con el proveedor de de [*Diffie-Hellman*](../secgloss/d-gly.md) / [*Schannel*](../secgloss/s-gly.md) para exportar claves desde el proveedor de [*servicios de cifrado*](../secgloss/c-gly.md) (CSP), e importarlas en él.

-   [Blobs de clave pública](#public-key-blobs)
-   [Blobs de clave privada](#private-key-blobs)

## <a name="public-key-blobs"></a>Blobs de clave pública

Diffie-Hellman los [*blobs de clave pública*](../secgloss/p-gly.md), tipo **PUBLICKEYBLOB**, se usan para intercambiar el valor de mod P (G ^ X) en un intercambio de claves Diffie-Hellman. Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

En la tabla siguiente se describe cada componente del [*BLOB de clave*](../secgloss/k-gly.md).



| Campo          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . El miembro **mágico** debe establecerse en 0x31484400. Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de DH1.                                                                                                                                                                                                                                                                                                                                                      |
| publickeystruc | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| y              | Secuencia de **bytes** . El valor y, (G ^ X) mod P, se encuentra directamente después de la estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . La longitud, en bytes, de la secuencia es el miembro **bitlen** de **DHPUBKEY** dividido por ocho. Si la longitud de los datos resultante del cálculo de (G ^ X) mod P es uno o varios bytes más cortos que P divididos por ocho, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato [*Little-Endian*](../secgloss/l-gly.md) ). |



 

## <a name="private-key-blobs"></a>Blobs de clave privada

Los [*blobs de clave privada*](../secgloss/p-gly.md)d-h, tipo **PRIVATEKEYBLOB**, se usan para exportar e importar información privada de una clave D-H. Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente del BLOB de clave.



| Campo          | Descripción                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . El miembro **mágico** debe establecerse en 0x32484400. Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de DH2. |
| generador      | Secuencia de **bytes** . El generador G.                                                                                                                                                                      |
| publickeystruc | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                      |
| principal          | Secuencia de **bytes** . El módulo primo, P. Estos datos siempre deben tener el bit más significativo establecido en uno.                                                                    |
| secret         | Secuencia de **bytes** . El exponente secreto X.                                                                                                                                                                |



 

> [!Note]  
> Los valores primo, generator y secreto siempre deben tener la misma longitud, en bytes. Si un valor es de un byte o más corto que el resto, debe rellenarse con el número de cero bytes necesario para que sean iguales. El primo, el generador y el secreto están en formato [*Little-Endian*](../secgloss/l-gly.md) .

 

 

 
