---
description: Describe el formato de un blob de clave privada Diffie-Hellman versión 3 exportada.
ms.assetid: c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1
title: Diffie-Hellman blobs de clave privada de la versión 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb35a6db0cfd75d34ba30d26be816a64c1b04205
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265407"
---
# <a name="diffie-hellman-version-3-private-key-blobs"></a>Diffie-Hellman blobs de clave privada de la versión 3

Cuando se exporta Diffie-Hellman blob de clave privada de la versión [*3,*](../secgloss/p-gly.md) se encuentra en un formato como el siguiente:


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



Este [*formato BLOB*](../secgloss/b-gly.md) se exporta cuando se usa la marca \_ CRYPT BLOB \_ VER3 con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Dado que la versión está en el BLOB, no es necesario especificar una marca al usar este BLOB [**con CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

En la tabla siguiente se describe cada componente de la [*clave BLOB*](../secgloss/k-gly.md).



| Campo         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader    | Estructura [**BLOBHEADER.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| dhprivkeyver3 | Estructura [**DHPRIVKEY \_ VER3.**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) El **miembro** mágico debe establecerse en 0x34484400 claves privadas. Observe que el valor hexadecimal es simplemente una [*codificación ASCII*](../secgloss/a-gly.md) de "DH4".                                                                                                                                                                                                                                                                                            |
| P             | El valor P se encuentra directamente después de la estructura [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) y siempre debe ser la longitud en bytes del campo **bitlenP** **DHPRIVKEY \_ VER3** (longitud de bits de P) dividido entre ocho (formato [*little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                            |
| Q             | El valor Q se encuentra directamente después del valor P y siempre debe ser la longitud en bytes del campo **bitlenQ** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) dividido entre ocho (formato [*little-endian).*](../secgloss/l-gly.md) Si el valor de bitlenQ es 0, el valor no está presente en blob.                                                                                                                                                                                                  |
| G             | El valor G se encuentra directamente después del valor Q y siempre debe ser la longitud en bytes del campo **bitlenP** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) (longitud de bits de P) dividido entre ocho. Si la longitud de los datos es uno o varios bytes más cortos que P dividido entre 8, los datos se deben agregar con los bytes necesarios (de valor cero) para que los datos sean la longitud deseada (formato [*little-endian).*](../secgloss/l-gly.md)                                                                 |
| J             | El valor J se encuentra directamente después del valor G y siempre debe ser la longitud en bytes del campo **bitlenJ** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) dividido entre ocho (formato [*little-endian).*](../secgloss/l-gly.md) Si el valor de bitlenJ es 0, el valor no está presente en blob.                                                                                                                                                                                                  |
| Y             | El valor Y,(G^X) mod P, se encuentra directamente después del valor J y siempre debe ser la longitud en bytes del campo **bitlenP** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) (longitud de bits de P) dividido entre ocho. Si la longitud de los datos que resulta del cálculo de (G^X) mod P es uno o varios bytes más corto que P dividido entre 8, los datos se deben agregar con los bytes necesarios (de valor cero) para que los datos sean la longitud deseada (formato [*little-endian).*](../secgloss/l-gly.md) |
| X             | El valor X es un entero grande aleatorio, de modo que la parte pública del par de claves DH, Y, es igual a: Y = (G^X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Al llamar [**a CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)el desarrollador puede elegir si cifrar la clave. La clave se cifra si el *parámetro hExpKey* contiene un identificador válido para una clave de sesión. Todo menos [**la parte BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrada. Tenga en cuenta que el algoritmo de cifrado y los parámetros de clave de cifrado no se almacenan junto con la [*clave privada BLOB*](../secgloss/p-gly.md). La aplicación debe administrar y almacenar esta información. Si se pasa cero para *hExpKey,* la clave privada se exportará sin cifrado.

> [!Note]  
> Es peligroso exportar claves privadas sin cifrado porque, a continuación, son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.

 

 

 
