---
description: Los blobs de clave pública de la versión 3 de DSS de tipo PUBLICKEYBLOB se usan para exportar e importar información sobre una clave pública DH.
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: Blobs de clave pública de la versión 3 de DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077aa9bb10569fac60d965ee6d5938984f3d579c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476474"
---
# <a name="dss-version-3-public-key-blobs"></a>Blobs de clave pública de la versión 3 de DSS

Los [*blobs*](../secgloss/p-gly.md) de clave pública de la versión 3 de DSS de tipo PUBLICKEYBLOB se usan para exportar e importar información sobre una clave pública DH. Tienen el formato siguiente:


```C++
BLOBHEADER blobheader; 
        // As explained under "Data Structures"
DSSPUBKEY_VER3 dsspubkeyver3;
BYTE p[dsspubkeyver3.bitlenP/8]; 
       // Where P is the prime modulus
BYTE q[dsspubkeyver3.bitlenQ/8]; 
       // Where Q is a large factor of P-1
BYTE g[dsspubkeyver3.bitlenP/8]; 
       // Where G is the generator parameter
BYTE j[dsspubkeyver3.bitlenJ/8]; 
       // Where J is (P-1)/Q
BYTE y[dsspubkeyver3.bitlenP/8]; 
       // Where Y is (G^X) mod P
```



Este [*formato BLOB*](../secgloss/b-gly.md) se exporta cuando se usa la marca \_ CRYPT BLOB \_ VER3 con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Dado que la versión está en el BLOB, no es necesario especificar una marca al usar este BLOB con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Además, este formato BLOB se usa con la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) cuando se usa el valor *dwParam* KP PUB PARAMS para establecer parámetros clave en una clave \_ \_ DSS. Esto se hace cuando se ha usado la \_ marca CRYPT PREGEN para generar la clave. Cuando se usa en esta situación, el valor y se omite y, por lo tanto, no debe incluirse en el BLOB.

En la tabla siguiente se describe cada componente del blob de clave.




| Campo | Descripción | 
|-------|-------------|
| Blobheader | Estructura <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER.</strong></a> El <strong>miembro bType</strong> debe tener un valor de PUBLICKEYBLOB. | 
| Dsspubkeyver3 | Una <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> estructura. El <strong>miembro</strong> mágico debe establecerse en "DSS3" (0x33535344) para las claves públicas. Observe que el valor hexadecimal es simplemente una <a href="/windows/desktop/SecGloss/a-gly"><em>codificación ASCII</em></a> de "DSS3".<br /> | 
| P | El valor P se encuentra directamente después de la estructura <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> y siempre debe ser la longitud, en bytes, del campo <strong>bitlenP</strong> de DSSPUBKEY_VER3 (longitud de bits de P) dividido entre ocho (formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian).</em></a> | 
| Q | El valor Q se encuentra directamente después del valor P y siempre debe ser la longitud en bytes del miembro<strong>bitlenQ</strong> de <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a>dividido entre ocho (formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian).</em></a> | 
| G | El valor G se encuentra directamente después del valor Q y <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong></strong></a>siempre debe ser la longitud, en bytes, del miembro<strong>DSSPUBKEY_VER3 bitlenP</strong> (longitud de bits de P) dividido entre ocho. Si la longitud de los datos es uno o varios bytes más cortos que P divididos entre 8, los datos se deben agregar con los bytes necesarios (de valor cero) para que los datos sean la longitud deseada (formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian).</em></a> | 
| J | El valor J se encuentra directamente después del valor G y siempre debe ser la longitud en bytes del miembro<strong>bitlenJ</strong> de <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a>dividido entre ocho (formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian).</em></a> Si el valor de bitlenQ es 0, el valor no está presente en blob. | 
| Y | El valor Y,(G^X) mod P, se encuentra directamente después del valor J y siempre debe ser la longitud, en bytes, del miembro<strong>bitlenP</strong> de <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a>(longitud de bits de P) dividido entre ocho. Si la longitud de los datos que resulta del cálculo de (G^X) mod P es uno o más bytes más cortos que P divididos entre 8, los datos se deben agregar con los bytes necesarios (de valor cero) para que los datos sean la longitud deseada (formato<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian).</em></a><blockquote>[!Note]<br />Cuando esta estructura se usa con <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> con el valor <em>dwParam</em> KP_PUB_PARAMS, este valor no se incluye en blob.</blockquote><br /><br /> | 




 

> [!Note]  
> Los BLOB de clave pública no están cifrados, pero contienen claves públicas en formato de texto no cifrado.

 

 

 
