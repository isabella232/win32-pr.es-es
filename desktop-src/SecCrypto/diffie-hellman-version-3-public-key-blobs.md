---
description: Diffie-Hellman blobs de clave pública de la versión 3 (tipo PUBLICKEYBLOB) se usan para exportar e importar información sobre una clave pública DH.
ms.assetid: ba29a71a-7509-49c7-93d2-f0a699532706
title: Diffie-Hellman blobs de clave pública de la versión 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21515e370fba1c63ab3d852a88ad45b974683a3ca5ba3c3ad258733593fb6e5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767422"
---
# <a name="diffie-hellman-version-3-public-key-blobs"></a>Diffie-Hellman blobs de clave pública de la versión 3

Diffie-Hellman [*blobs*](../secgloss/p-gly.md) de clave pública de la versión 3 (tipo PUBLICKEYBLOB) se usan para exportar e importar información sobre una clave pública DH. Tienen el formato siguiente:


```C++
BLOBHEADER blobheader; 
                 // As explained under "Data Structures"
DHPUBKEY_VER3 dhpubkeyver3;
BYTE p[dhpubkeyver3.bitlenP/8]; 
                 // Where P is the prime modulus
BYTE q[dhpubkeyver3.bitlenQ/8]; 
                 // Where Q is a large factor of P-1
BYTE g[dhpubkeyver3.bitlenP/8]; 
                 // Where G is the generator parameter
BYTE j[dhpubkeyver3.bitlenJ/8]; 
                 // Where J is (P-1)/Q
BYTE y[dhpubkeyver3.bitlenP/8]; 
                 // Where Y is (G^X) mod P
```



Este formato BLOB se exporta cuando se usa la marca \_ CRYPT BLOB \_ VER3 con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Dado que la versión está en el BLOB, no es necesario especificar una marca al usar este [*BLOB*](../secgloss/b-gly.md) con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Además, este formato BLOB se usa con la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) cuando se usa el valor *dwParam* KP PUB PARAMS para establecer parámetros clave en una \_ clave \_ DH. Esto se hace cuando se ha usado la \_ marca CRYPT PREGEN para generar la clave. Cuando se usa en esta situación, el valor y se omite y, por lo tanto, no debe incluirse en blob.

En la tabla siguiente se describe cada componente del blob de clave.



| Campo        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader   | Estructura [**BLOBHEADER.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) El **miembro bType** debe tener un valor de PUBLICKEYBLOB.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| dhpubkeyver3 | Estructura [**DHPUBKEY \_ VER3.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) El **miembro** mágico debe establecerse en 0x33484400 claves públicas. Observe que el valor hexadecimal es simplemente una [*codificación ASCII*](../secgloss/a-gly.md) de "DH3".                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| P            | El valor P se encuentra directamente después de la estructura [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) y siempre debe ser la longitud, en bytes, del campo **bitlenP** **DHPUBKEY \_ VER3** (longitud de bits de P) dividido entre ocho (formato [*little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                                                                                                                                                                                           |
| Q            | El valor Q se encuentra directamente después del valor P y siempre debe ser la longitud en bytes del campo **bitlenQ** [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) dividido entre ocho (formato [*little-endian).*](../secgloss/l-gly.md) Si el valor de bitlenQ es 0, el valor no está presente en blob.                                                                                                                                                                                                                                                                                                                                                                 |
| G            | El valor G se encuentra directamente después del valor Q y siempre debe ser la longitud, en bytes, del campo **bitlenP** [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) (longitud de bits de P) dividida entre ocho. Si la longitud de los datos es uno o varios bytes más cortos que P divididos entre 8, los datos se deben agregar con los bytes necesarios (de valor cero) para que los datos sean la longitud deseada (formato [*little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                              |
| J            | El valor J se encuentra directamente después del valor G y siempre debe ser la longitud en bytes del campo **bitlenJ** [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) dividido entre ocho (formato [*little-endian).*](../secgloss/l-gly.md) Si el valor de bitlenQ es 0, el valor no está presente en blob.                                                                                                                                                                                                                                                                                                                                                                 |
| Y            | El valor Y,(G^X) mod P, se encuentra directamente después del valor J y siempre debe ser la longitud en bytes del campo **bitlenP** [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) (longitud de bits de P) dividido entre ocho. Si la longitud de los datos que resulta del cálculo de (G^X) mod P es uno o más bytes más cortos que P divididos entre 8, los datos se deben agregar con los bytes necesarios (de valor cero) para que los datos sean la longitud deseada (formato [*little-endian).*](../secgloss/l-gly.md) Cuando esta estructura se usa con [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con el valor *dwParam* KP PUB PARAMS, este valor no \_ \_ se incluye en blob. |



 

> [!Note]  
> Los BLOB de clave pública no están cifrados, pero contienen claves públicas en formato de texto no cifrado.

 

 

 
