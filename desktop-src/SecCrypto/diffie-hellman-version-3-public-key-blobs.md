---
description: Diffie-Hellman los blobs de clave pública de la versión 3 (tipo PUBLICKEYBLOB) se usan para exportar e importar información acerca de una clave pública DH.
ms.assetid: ba29a71a-7509-49c7-93d2-f0a699532706
title: Blobs de clave pública de Diffie-Hellman versión 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7228e4b4a786dc0eb25d1ba199b5c20923dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667187"
---
# <a name="diffie-hellman-version-3-public-key-blobs"></a>Blobs de clave pública de Diffie-Hellman versión 3

Diffie-Hellman los [*blobs de clave pública*](../secgloss/p-gly.md) de la versión 3 (tipo PUBLICKEYBLOB) se usan para exportar e importar información acerca de una clave pública DH. Tienen el siguiente formato:


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



Este formato de BLOB se exporta cuando \_ \_ se usa la marca ver3 del BLOB de cifrado con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Dado que la versión está en el BLOB, no es necesario especificar una marca cuando se usa este [*BLOB*](../secgloss/b-gly.md) con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Además, este formato de BLOB se usa con la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) cuando el valor de *dwParam* \_ de los \_ parámetros de configuración de PK pub se usa para establecer los parámetros de clave en una clave DH. Esto se hace cuando se ha \_ usado la marca CRYPT PREGEN para generar la clave. Cuando se usa en esta situación, el valor y se omite y, por tanto, no se debe incluir en el BLOB.

En la tabla siguiente se describe cada componente del BLOB de clave.



| Campo        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader   | Estructura [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) . El miembro **bType** debe tener un valor PUBLICKEYBLOB.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| dhpubkeyver3 | Estructura de [**DHPUBKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) . El miembro **mágico** debe establecerse en 0x33484400 para las claves públicas. Observe que el valor hexadecimal es simplemente una codificación [*ASCII*](../secgloss/a-gly.md) de "DH3".                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| P            | El valor P se encuentra directamente después de la estructura [**DHPUBKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) y siempre debe ser la longitud, en bytes, del campo **DHPUBKEY \_ ver3** **bitlenP** (longitud de bit de P) dividido entre ocho (formato [*Little-Endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                                                                                                                                                                                           |
| Q            | El valor Q se encuentra directamente después del valor P y siempre debe ser la longitud en bytes del campo [**DHPUBKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenQ** dividido entre ocho (formato [*Little-Endian*](../secgloss/l-gly.md) ). Si el valor de bitlenQ es 0, el valor no está presente en el BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| G            | El valor G se encuentra directamente después del valor Q y siempre debe ser la longitud, en bytes, del campo [**DHPUBKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenP** (longitud de bit de P) dividido entre ocho. Si la longitud de los datos es uno o varios bytes más cortos que P dividido entre 8, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato [*Little-Endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                              |
| J            | El valor J se encuentra directamente después del valor G y siempre debe ser la longitud en bytes del campo [**DHPUBKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenJ** dividido entre ocho (formato [*Little-Endian*](../secgloss/l-gly.md) ). Si el valor de bitlenQ es 0, el valor no está presente en el BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| Y            | El valor Y, (G ^ X) mod P, se encuentra directamente después del valor J y siempre debe ser la longitud en bytes del campo [**DHPUBKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenP** (longitud de bit de P) dividido entre ocho. Si la longitud de los datos resultante del cálculo de (G ^ X) mod P es uno o más bytes más cortos que P dividido entre 8, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato [*Little-Endian*](../secgloss/l-gly.md) ). Cuando esta estructura se usa con [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con el valor *DWPARAM* de los parámetros de KP \_ pub \_ , este valor no se incluye en el BLOB. |



 

> [!Note]  
> Los blobs de clave pública no están cifrados, pero contienen claves públicas en formato de texto simple.

 

 

 
