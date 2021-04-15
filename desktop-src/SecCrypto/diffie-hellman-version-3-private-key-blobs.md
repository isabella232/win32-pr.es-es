---
description: Describe el formato de un BLOB de clave privada Diffie-Hellman versión 3 exportado.
ms.assetid: c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1
title: Blobs de clave privada de Diffie-Hellman versión 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb35a6db0cfd75d34ba30d26be816a64c1b04205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497200"
---
# <a name="diffie-hellman-version-3-private-key-blobs"></a>Blobs de clave privada de Diffie-Hellman versión 3

Cuando se exporta un BLOB de [*clave privada*](../secgloss/p-gly.md) Diffie-Hellman versión 3, tiene un formato como el siguiente:


```C++
BLOBHEADER        blobheader;
DHPRIVKEY_VER3   dhprivkeyver3;
BYTE p[dhprivkeyver3.bitlenP/8]; 
            // Where P is the prime modulus
BYTE q[dhprivkeyver3.bitlenQ/8]; 
            // Where Q is a large factor of P-1
BYTE g[dhprivkeyver3.bitlenP/8]; 
            // Where G is the generator parameter
BYTE j[dhprivkeyver3.bitlenJ/8]; 
            // Where J is (P-1)/Q
BYTE y[dhprivkeyver3.bitlenP/8]; 
            // Where Y is (G^X) mod P
BYTE x[dhprivkeyver3.bitlenX/8]; 
            // Where X is the private exponent
```



Este formato de [*BLOB*](../secgloss/b-gly.md) se exporta cuando \_ se usa la marca ver3 del BLOB de cifrado \_ con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Dado que la versión está en el BLOB, no es necesario especificar una marca cuando se usa este BLOB con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

En la tabla siguiente se describe cada componente del [*BLOB de clave*](../secgloss/k-gly.md).



| Campo         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader    | Estructura [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| dhprivkeyver3 | Estructura de [**DHPRIVKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) . El miembro **mágico** debe establecerse en 0x34484400 para las claves privadas. Observe que el valor hexadecimal es simplemente una codificación [*ASCII*](../secgloss/a-gly.md) de "DH4".                                                                                                                                                                                                                                                                                            |
| P             | El valor P se encuentra directamente después de la estructura [**DHPRIVKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) y siempre debe ser la longitud en bytes del campo **DHPRIVKEY \_ ver3** **bitlenP** (longitud de bit de P) dividido entre ocho (formato [*Little-Endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                            |
| Q             | El valor Q se encuentra directamente después del valor P y siempre debe ser la longitud en bytes del campo [**DHPRIVKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenQ** dividido entre ocho (formato [*Little-Endian*](../secgloss/l-gly.md) ). Si el valor de bitlenQ es 0, el valor no está presente en el BLOB.                                                                                                                                                                                                  |
| G             | El valor G se encuentra directamente después del valor Q y siempre debe ser la longitud en bytes del campo [**DHPRIVKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenP** (longitud de bit de P) dividido entre ocho. Si la longitud de los datos es uno o varios bytes más cortos que P dividido entre 8, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato [*Little-Endian*](../secgloss/l-gly.md) ).                                                                 |
| J             | El valor J se encuentra directamente después del valor G y siempre debe ser la longitud en bytes del campo [**DHPRIVKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenJ** dividido entre ocho (formato [*Little-Endian*](../secgloss/l-gly.md) ). Si el valor de bitlenJ es 0, el valor no está presente en el BLOB.                                                                                                                                                                                                  |
| Y             | El valor Y, (G ^ X) mod P, se encuentra directamente después del valor J y siempre debe ser la longitud en bytes del campo [**DHPRIVKEY \_ ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenP** (longitud de bit de P) dividido entre ocho. Si la longitud de los datos resultante del cálculo de (G ^ X) mod P es uno o más bytes más cortos que P dividido entre 8, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato [*Little-Endian*](../secgloss/l-gly.md) ). |
| X             | El valor X es un entero aleatorio grande, de modo que la parte pública del par de claves DH, Y, sea igual a: Y = (G ^ X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Al llamar a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), el desarrollador puede elegir si desea cifrar la clave. La clave se cifra si el parámetro *hExpKey* contiene un identificador válido para una clave de sesión. Todo excepto la parte [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrado. Tenga en cuenta que el algoritmo de cifrado y los parámetros de clave de cifrado no se almacenan junto con el [*BLOB de clave privada*](../secgloss/p-gly.md). La aplicación debe administrar y almacenar esta información. Si se pasa cero para *hExpKey*, la clave privada se exportará sin cifrado.

> [!Note]  
> Es peligroso exportar las claves privadas sin cifrado, ya que son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.

 

 

 
