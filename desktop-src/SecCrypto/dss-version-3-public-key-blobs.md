---
description: Los blobs de clave pública de DSS versión 3 del tipo PUBLICKEYBLOB se usan para exportar e importar información acerca de una clave pública DH.
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: Blobs de clave pública de DSS versión 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593ac69025ff046a9a8d014286c2464788c07b02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666403"
---
# <a name="dss-version-3-public-key-blobs"></a>Blobs de clave pública de DSS versión 3

Los [*blobs de clave pública*](../secgloss/p-gly.md) de DSS versión 3 del tipo PUBLICKEYBLOB se usan para exportar e importar información acerca de una clave pública DH. Tienen el siguiente formato:


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



Este formato de [*BLOB*](../secgloss/b-gly.md) se exporta cuando \_ se usa la marca ver3 del BLOB de cifrado \_ con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Dado que la versión está en el BLOB, no es necesario especificar una marca cuando se usa este BLOB con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Además, este formato de BLOB se usa con la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) cuando el valor de *dwParam* \_ de los \_ parámetros de configuración de PK pub se usa para establecer parámetros de clave en una clave DSS. Esto se hace cuando se ha \_ usado la marca CRYPT PREGEN para generar la clave. Cuando se usa en esta situación, el valor y se omite y, por tanto, no se debe incluir en el BLOB.

En la tabla siguiente se describe cada componente del BLOB de clave.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Blobheader</td>
<td>Estructura <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> . El miembro <strong>bType</strong> debe tener un valor PUBLICKEYBLOB.</td>
</tr>
<tr class="even">
<td>Dsspubkeyver3</td>
<td>Estructura de <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> . El miembro <strong>mágico</strong> debe establecerse en &quot; DSS3 &quot; (0x33535344) para las claves públicas. Observe que el valor hexadecimal es solo una codificación <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> de &quot; DSS3.&quot;<br/></td>
</tr>
<tr class="odd">
<td>P</td>
<td>El valor P se encuentra directamente después de la estructura <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> , y siempre debe ser la longitud, en bytes, del campo DSSPUBKEY_VER3 <strong>bitlenP</strong> (longitud de bit de P) dividido entre ocho (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian</em></a> ).</td>
</tr>
<tr class="even">
<td>Q</td>
<td>El valor Q se encuentra directamente después del valor P y siempre debe ser la longitud en bytes del miembro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> dividido entre ocho (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian</em></a> ).</td>
</tr>
<tr class="odd">
<td>G</td>
<td>El valor G se encuentra directamente después del valor Q y siempre debe ser la longitud, en bytes, del miembro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (longitud de bit de P) dividido entre ocho. Si la longitud de los datos es uno o varios bytes más cortos que P dividido entre 8, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian</em></a> ).</td>
</tr>
<tr class="even">
<td>J</td>
<td>El valor J se encuentra directamente después del valor G y siempre debe ser la longitud en bytes del miembro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> dividido entre ocho (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian</em></a> ). Si el valor de bitlenQ es 0, el valor no está presente en el BLOB.</td>
</tr>
<tr class="odd">
<td>Y</td>
<td>El valor Y, (G ^ X) mod P, se encuentra directamente después del valor J y siempre debe ser la longitud, en bytes, del miembro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (longitud de bit de P) dividido entre ocho. Si la longitud de los datos resultante del cálculo de (G ^ X) mod P es uno o más bytes más cortos que P dividido entre 8, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian</em></a> ).
<blockquote>
[!Note]<br />
Cuando esta estructura se usa con <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> con el valor de <em>dwParam</em> KP_PUB_PARAMS, este valor no se incluye en el BLOB.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Los blobs de clave pública no están cifrados, pero contienen claves públicas en formato de texto simple.

 

 

 
