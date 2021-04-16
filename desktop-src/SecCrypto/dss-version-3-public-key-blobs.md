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
# <a name="dss-version-3-public-key-blobs"></a><span data-ttu-id="18a46-103">Blobs de clave pública de DSS versión 3</span><span class="sxs-lookup"><span data-stu-id="18a46-103">DSS Version 3 Public Key BLOBs</span></span>

<span data-ttu-id="18a46-104">Los [*blobs de clave pública*](../secgloss/p-gly.md) de DSS versión 3 del tipo PUBLICKEYBLOB se usan para exportar e importar información acerca de una clave pública DH.</span><span class="sxs-lookup"><span data-stu-id="18a46-104">DSS version 3 [*Public Key BLOBs*](../secgloss/p-gly.md) of type PUBLICKEYBLOB are used to export and import information about a DH public key.</span></span> <span data-ttu-id="18a46-105">Tienen el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="18a46-105">They have the following format:</span></span>


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



<span data-ttu-id="18a46-106">Este formato de [*BLOB*](../secgloss/b-gly.md) se exporta cuando \_ se usa la marca ver3 del BLOB de cifrado \_ con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="18a46-106">This [*BLOB*](../secgloss/b-gly.md) format is exported when the CRYPT\_BLOB\_VER3 flag is used with [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span> <span data-ttu-id="18a46-107">Dado que la versión está en el BLOB, no es necesario especificar una marca cuando se usa este BLOB con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="18a46-107">Because the version is in the BLOB, there is no need to specify a flag when using this BLOB with [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span>

<span data-ttu-id="18a46-108">Además, este formato de BLOB se usa con la función [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) cuando el valor de *dwParam* \_ de los \_ parámetros de configuración de PK pub se usa para establecer parámetros de clave en una clave DSS.</span><span class="sxs-lookup"><span data-stu-id="18a46-108">In addition, this BLOB format is used with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function when the *dwParam* value KP\_PUB\_PARAMS is used to set key parameters on a DSS key.</span></span> <span data-ttu-id="18a46-109">Esto se hace cuando se ha \_ usado la marca CRYPT PREGEN para generar la clave.</span><span class="sxs-lookup"><span data-stu-id="18a46-109">This is done when the CRYPT\_PREGEN flag has been used to generate the key.</span></span> <span data-ttu-id="18a46-110">Cuando se usa en esta situación, el valor y se omite y, por tanto, no se debe incluir en el BLOB.</span><span class="sxs-lookup"><span data-stu-id="18a46-110">When used in this situation, the y value is ignored and therefore should not be included in the BLOB.</span></span>

<span data-ttu-id="18a46-111">En la tabla siguiente se describe cada componente del BLOB de clave.</span><span class="sxs-lookup"><span data-stu-id="18a46-111">The following table describes each component of the key BLOB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18a46-112">Campo</span><span class="sxs-lookup"><span data-stu-id="18a46-112">Field</span></span></th>
<th><span data-ttu-id="18a46-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="18a46-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18a46-114">Blobheader</span><span class="sxs-lookup"><span data-stu-id="18a46-114">Blobheader</span></span></td>
<td><span data-ttu-id="18a46-115">Estructura <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="18a46-115">A <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> structure.</span></span> <span data-ttu-id="18a46-116">El miembro <strong>bType</strong> debe tener un valor PUBLICKEYBLOB.</span><span class="sxs-lookup"><span data-stu-id="18a46-116">The <strong>bType</strong> member must have a value of PUBLICKEYBLOB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18a46-117">Dsspubkeyver3</span><span class="sxs-lookup"><span data-stu-id="18a46-117">Dsspubkeyver3</span></span></td>
<td><span data-ttu-id="18a46-118">Estructura de <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="18a46-118">A <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure.</span></span> <span data-ttu-id="18a46-119">El miembro <strong>mágico</strong> debe establecerse en &quot; DSS3 &quot; (0x33535344) para las claves públicas.</span><span class="sxs-lookup"><span data-stu-id="18a46-119">The <strong>magic</strong> member should be set to &quot;DSS3&quot; (0x33535344) for public keys.</span></span> <span data-ttu-id="18a46-120">Observe que el valor hexadecimal es solo una codificación <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> de &quot; DSS3.&quot;</span><span class="sxs-lookup"><span data-stu-id="18a46-120">Notice that the hexadecimal value is just an <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> encoding of &quot;DSS3.&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18a46-121">P</span><span class="sxs-lookup"><span data-stu-id="18a46-121">P</span></span></td>
<td><span data-ttu-id="18a46-122">El valor P se encuentra directamente después de la estructura <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> , y siempre debe ser la longitud, en bytes, del campo DSSPUBKEY_VER3 <strong>bitlenP</strong> (longitud de bit de P) dividido entre ocho (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="18a46-122">The P value is located directly after the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure, and should always be the length, in bytes, of the DSSPUBKEY_VER3 <strong>bitlenP</strong> field (bit length of P) divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18a46-123">Q</span><span class="sxs-lookup"><span data-stu-id="18a46-123">Q</span></span></td>
<td><span data-ttu-id="18a46-124">El valor Q se encuentra directamente después del valor P y siempre debe ser la longitud en bytes del miembro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> dividido entre ocho (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="18a46-124">The Q value is located directly after the P value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18a46-125">G</span><span class="sxs-lookup"><span data-stu-id="18a46-125">G</span></span></td>
<td><span data-ttu-id="18a46-126">El valor G se encuentra directamente después del valor Q y siempre debe ser la longitud, en bytes, del miembro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (longitud de bit de P) dividido entre ocho.</span><span class="sxs-lookup"><span data-stu-id="18a46-126">The G value is located directly after the Q value and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="18a46-127">Si la longitud de los datos es uno o varios bytes más cortos que P dividido entre 8, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="18a46-127">If the length of the data is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18a46-128">J</span><span class="sxs-lookup"><span data-stu-id="18a46-128">J</span></span></td>
<td><span data-ttu-id="18a46-129">El valor J se encuentra directamente después del valor G y siempre debe ser la longitud en bytes del miembro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> dividido entre ocho (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="18a46-129">The J value is located directly after the G value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span> <span data-ttu-id="18a46-130">Si el valor de bitlenQ es 0, el valor no está presente en el BLOB.</span><span class="sxs-lookup"><span data-stu-id="18a46-130">If the bitlenQ value is 0, then the value is absent from the BLOB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18a46-131">Y</span><span class="sxs-lookup"><span data-stu-id="18a46-131">Y</span></span></td>
<td><span data-ttu-id="18a46-132">El valor Y, (G ^ X) mod P, se encuentra directamente después del valor J y siempre debe ser la longitud, en bytes, del miembro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (longitud de bit de P) dividido entre ocho.</span><span class="sxs-lookup"><span data-stu-id="18a46-132">The Y value, (G^X) mod P, is located directly after the J value, and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="18a46-133">Si la longitud de los datos resultante del cálculo de (G ^ X) mod P es uno o más bytes más cortos que P dividido entre 8, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little-Endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="18a46-133">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="18a46-134">Cuando esta estructura se usa con <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> con el valor de <em>dwParam</em> KP_PUB_PARAMS, este valor no se incluye en el BLOB.</span><span class="sxs-lookup"><span data-stu-id="18a46-134">When this structure is used with <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> with the <em>dwParam</em> value KP_PUB_PARAMS, then this value is not included in the BLOB.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="18a46-135">Los blobs de clave pública no están cifrados, pero contienen claves públicas en formato de texto simple.</span><span class="sxs-lookup"><span data-stu-id="18a46-135">Public key BLOBs are not encrypted, but contain public keys in plaintext form.</span></span>

 

 

 
