---
description: Describe el formato de una clave privada exportada de DSS versión 3.
ms.assetid: 650532fd-919b-495a-9fb9-981790447d3d
title: Blobs de clave privada de la versión 3 de DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6706f8cbfccb8c836efefb99a30086dc459619c8477b773a557f503ebbb2243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767260"
---
# <a name="dss-version-3-private-key-blobs"></a>Blobs de clave privada de la versión 3 de DSS

Cuando se exporta una clave [*privada DSS*](../secgloss/d-gly.md) [](../secgloss/p-gly.md) de la versión 3, se encuentra en un formato como se muestra a continuación:


```C++
BLOBHEADER        blobheader; 
DSSPRIVKEY_VER3   dssprivkeyver3;
BYTE p[dssprivkeyver3.bitlenP/8]; 
                    // Where P is the prime modulus
BYTE q[dssprivkeyver3.bitlenQ/8]; 
                    // Where Q is a large factor of P-1
BYTE g[dssprivkeyver3.bitlenP/8]; 
                    // Where G is the generator parameter
BYTE j[dssprivkeyver3.bitlenJ/8]; 
                    // Where J is (P-1)/Q
BYTE y[dssprivkeyver3.bitlenP/8]; 
                    // Where Y is (G^X) mod P
BYTE x[dssprivkeyver3.bitlenX/8]; 
                    // Where X is the private exponent
```



Este [*formato BLOB*](../secgloss/b-gly.md) se exporta cuando se usa la marca \_ CRYPT BLOB \_ VER3 con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Dado que la versión está en el BLOB, no es necesario especificar una marca al usar este BLOB con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

En la tabla siguiente se describe cada componente de la [*clave BLOB*](../secgloss/k-gly.md).



| Campo          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blobheader     | Estructura [**BLOBHEADER.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) El **miembro bType** debe tener un valor de PUBLICKEYBLOB.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dssprivkeyver3 | Estructura **DSSPRIVKEY \_ VER3.** El **miembro** mágico debe establecerse en "DSS4" (0x34535344) para las claves privadas. Observe que el valor hexadecimal es simplemente una [*codificación ASCII*](../secgloss/a-gly.md) de "DSS4".<br/>                                                                                                                                                                                                                                                                     |
| P              | El valor P se encuentra directamente después de la estructura **DSSPRIVKEY \_ VER3** y siempre debe ser la longitud, en bytes, del campo **\_ bitlenP DSSPRIVKEY VER3** (longitud de bits de P) dividido entre ocho (formato [*little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                           |
| Q              | El valor Q se encuentra directamente después del valor P y siempre debe ser la longitud, en bytes, del campo **\_ bitlenQ DSSPRIVKEY VER3** dividido entre ocho (formato [*little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                                                                     |
| G              | El valor G se encuentra directamente después del valor Q y siempre debe ser la longitud, en bytes, del campo **\_ bitlenP DSSPRIVKEY VER3** (longitud de bits de P) dividida entre ocho. Si la longitud de los datos es uno o varios bytes más cortos que P divididos entre 8, los datos se deben agregar con los bytes necesarios (de valor cero) para que los datos sean la longitud deseada (formato [*little-endian).*](../secgloss/l-gly.md)                                                                 |
| J              | El valor J se encuentra directamente después del valor G y siempre debe ser la longitud, en bytes, del campo **\_ bitlenJ DSSPRIVKEY VER3** dividido entre ocho (formato [*little-endian).*](../secgloss/l-gly.md) Si el valor de bitlenJ es 0, el valor no está presente en blob.                                                                                                                                                                                                   |
| Y              | El valor Y,(G^X) mod P, se encuentra directamente después del valor J y siempre debe ser la longitud, en bytes, del campo **\_ bitlenP DSSPRIVKEY VER3** (longitud de bits de P) dividida entre ocho. Si la longitud de los datos que resulta del cálculo de (G^X) mod P es uno o más bytes más cortos que P divididos entre 8, los datos se deben agregar con los bytes necesarios (de valor cero) para que los datos sean la longitud deseada (formato [*little-endian).*](../secgloss/l-gly.md) |
| X              | El valor X es un entero grande aleatorio, de modo que la parte pública del par de claves DH, Y, es igual a: Y = (G^X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                               |



 

Al llamar [**a CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)el desarrollador puede elegir si cifrar la clave. La clave se cifra si el *parámetro hExpKey* contiene un identificador válido para una clave de sesión. Todo menos la [**parte BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrada. Tenga en cuenta que el algoritmo de cifrado y los parámetros de clave de cifrado no se almacenan junto con [*el blob de clave privada*](../secgloss/p-gly.md). La aplicación debe administrar y almacenar esta información. Si se pasa cero para *hExpKey*, la clave privada se exportará sin cifrado.

> [!IMPORTANT]
> Es peligroso exportar claves privadas sin cifrado porque, a continuación, son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.

 

 

 
