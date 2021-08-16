---
description: Los blobs se usan con el proveedor Diffie-Hellman para exportar claves del proveedor de servicios criptográficos (CSP) e importar claves en él.
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Diffie-Hellman blobs de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e993daf5b9ec0509ae6fa01df4edc06bafec733bb80f7b014921026fbc35ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767719"
---
# <a name="diffie-hellman-key-blobs"></a>Diffie-Hellman blobs de claves

[*Los blobs se*](../secgloss/b-gly.md) usan con el proveedor [*Diffie-Hellman*](../secgloss/d-gly.md) para exportar claves del proveedor de servicios criptográficos [*(CSP)*](../secgloss/c-gly.md) e importar claves en él.

-   [Blobs de clave pública](#public-key-blobs)
-   [Blobs de clave privada](#private-key-blobs)

## <a name="public-key-blobs"></a>Blobs de clave pública

Diffie-Hellman [*blobs*](../secgloss/p-gly.md)de clave pública, tipo **PUBLICKEYBLOB,** se usan para intercambiar el valor mod P (G^X) en un intercambio de Diffie-Hellman clave. Estas claves se exportan e importan como una secuencia de bytes con el formato siguiente.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

En la tabla siguiente se describe cada componente de la [*clave BLOB*](../secgloss/k-gly.md).



| Campo          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Estructura [**DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) El **miembro** mágico debe establecerse en 0x31484400. Este valor hexadecimal es la [*codificación ASCII*](../secgloss/a-gly.md) de "DH1".                                                                                                                                                                                                                                                                                                                                                                 |
| publickeystruc | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| y              | Secuencia **BYTE.** El valor Y,(G^X) mod P, se encuentra directamente después de la estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) y siempre debe ser la longitud, en bytes, del campo **bitlen DHPUBKEY** (longitud de bits de P) dividida entre ocho. Si la longitud de los datos que resulta del cálculo de (G^X) mod P es uno o varios bytes más corto que P dividido entre ocho, los datos se deben agregar con los bytes necesarios (de valor cero) para que los datos sean la longitud deseada (formato [*little-endian).*](../secgloss/l-gly.md) |



 

## <a name="private-key-blobs"></a>Blobs de clave privada

Diffie-Hellman [*blobs de*](../secgloss/p-gly.md)clave privada, tipo **PRIVATEKEYBLOB,** se usan para almacenar la información pública y privada de una Diffie-Hellman privada. Estas claves se exportan e importan como una secuencia de bytes con el formato siguiente.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

En la tabla siguiente se describe cada componente del blob de clave.



| Campo          | Descripción                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Estructura [**DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) El **miembro** mágico debe establecerse en 0x32484400. Este valor hexadecimal es la [*codificación ASCII*](../secgloss/a-gly.md) de "DH2". |
| generador      | Secuencia **BYTE.** El generador, G.                                                                                                                                                                       |
| publickeystruc | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                        |
| Primer          | Secuencia **BYTE.** Módulo primo, P. Estos datos siempre deben tener el bit más significativo del byte más significativo establecido en uno.                                                                      |
| secret         | Secuencia **BYTE.** Exponente del secreto, X.                                                                                                                                                                 |



 

> [!Note]  
> El generador y el secreto siempre deben tener la misma longitud, en bytes. Si es un byte o más corto que el otro, se debe agregar con el número necesario de bytes de valor cero para que sean iguales. Tanto el generador como el secreto están en [*formato little-endian.*](../secgloss/l-gly.md)

 

 

 
