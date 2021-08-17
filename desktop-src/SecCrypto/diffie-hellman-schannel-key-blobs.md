---
description: Los blobs se usan con el proveedor Diffie-Hellman/Schannel para exportar claves del proveedor de servicios criptográficos (CSP) e importar claves en él.
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: Blobs de clave Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c653e26f53611e8b00a1dae4e49df7084e6dc655d67f11550a430860fab12d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767699"
---
# <a name="diffie-hellmanschannel-key-blobs"></a>Blobs de clave Diffie-Hellman/Schannel

[*Los blobs se*](../secgloss/b-gly.md) usan con el proveedor [*Diffie-Hellman*](../secgloss/d-gly.md)Schannel para exportar claves del proveedor de servicios criptográficos (CSP) e importar claves en / [](../secgloss/s-gly.md) él. [](../secgloss/c-gly.md)

-   [Blobs de clave pública](#public-key-blobs)
-   [Blobs de clave privada](#private-key-blobs)

## <a name="public-key-blobs"></a>Blobs de clave pública

Diffie-Hellman [*blobs*](../secgloss/p-gly.md)de clave pública , tipo **PUBLICKEYBLOB,** se usan para intercambiar el valor de mod P (G^X) en un intercambio de Diffie-Hellman clave. Estas claves se exportan e importan como una secuencia de bytes con el formato siguiente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

En la tabla siguiente se describe cada componente de la [*clave BLOB*](../secgloss/k-gly.md).



| Campo          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Estructura [**DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) El **miembro** mágico debe establecerse en 0x31484400. Este valor hexadecimal es la [*codificación ASCII*](../secgloss/a-gly.md) de DH1.                                                                                                                                                                                                                                                                                                                                                      |
| publickeystruc | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| y              | Secuencia **BYTE.** El valor y, (G^X) mod P, se encuentra directamente después de la [**estructura DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) La longitud, en bytes, de la secuencia es el **miembro bitlen** de **DHPUBKEY** dividido entre ocho. Si la longitud de los datos que resulta del cálculo de (G^X) mod P es uno o más bytes más cortos que P divididos entre ocho, los datos se deben agregar con los bytes necesarios (de valor cero) para que los datos sean la longitud deseada (formato [*little-endian).*](../secgloss/l-gly.md) |



 

## <a name="private-key-blobs"></a>Blobs de clave privada

Los [*blobs de clave*](../secgloss/p-gly.md)privada D-H, tipo **PRIVATEKEYBLOB,** se usan para exportar e importar información privada de una clave D-H. Estas claves se exportan e importan como una secuencia de bytes con el formato siguiente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente del blob de clave.



| Campo          | Descripción                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Estructura [**DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) El **miembro** mágico debe establecerse en 0x32484400. Este valor hexadecimal es la [*codificación ASCII*](../secgloss/a-gly.md) de DH2. |
| generador      | Secuencia **BYTE.** Generador G.                                                                                                                                                                      |
| publickeystruc | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                      |
| Primer          | Secuencia **BYTE.** Módulo primo, P. Estos datos siempre deben tener el bit más significativo del byte más significativo establecido en uno.                                                                    |
| secret         | Secuencia **BYTE.** Exponente del secreto X.                                                                                                                                                                |



 

> [!Note]  
> Los valores primo, generador y secreto siempre deben tener la misma longitud, en bytes. Si algún valor es un byte o más corto que los demás, se debe agregar con el número necesario de cero bytes para que sean iguales. El primo, el generador y el secreto están en [*formato little-endian.*](../secgloss/l-gly.md)

 

 

 
