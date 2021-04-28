---
description: Revocación de certificados de OPM
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Revocación de certificados de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ebf38a3fa6bd2b61a756d6103453fd0356f693
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092733"
---
# <a name="opm-certificate-revocation"></a><span data-ttu-id="e5017-103">Revocación de certificados de OPM</span><span class="sxs-lookup"><span data-stu-id="e5017-103">OPM Certificate Revocation</span></span>

<span data-ttu-id="e5017-104">Microsoft puede revocar un certificado de administrador de protección de salida (OPM).</span><span class="sxs-lookup"><span data-stu-id="e5017-104">An output protection manager (OPM) certificate can be revoked by Microsoft.</span></span> <span data-ttu-id="e5017-105">La lista de certificados revocados se almacena en una lista de revocación global (GRL).</span><span class="sxs-lookup"><span data-stu-id="e5017-105">The list of revoked certificates is stored in a global revocation list (GRL).</span></span> <span data-ttu-id="e5017-106">La GRL tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="e5017-106">The GRL has the following format:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5017-107">Sección</span><span class="sxs-lookup"><span data-stu-id="e5017-107">Section</span></span></th>
<th><span data-ttu-id="e5017-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5017-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5017-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5017-109">Header</span></span></td>
<td><span data-ttu-id="e5017-110">Estructura <a href="grl-header.md"><strong>GRL_HEADER</strong></a> datos.</span><span class="sxs-lookup"><span data-stu-id="e5017-110">A <a href="grl-header.md"><strong>GRL_HEADER</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5017-111">Core</span><span class="sxs-lookup"><span data-stu-id="e5017-111">Core</span></span></td>
<td><span data-ttu-id="e5017-112">Contiene las siguientes listas de revocación:</span><span class="sxs-lookup"><span data-stu-id="e5017-112">Contains the following revocation lists:</span></span>
<ul>
<li><span data-ttu-id="e5017-113">Revocaciones binarias de kernel</span><span class="sxs-lookup"><span data-stu-id="e5017-113">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="e5017-114">Revocaciones binarias en modo de usuario</span><span class="sxs-lookup"><span data-stu-id="e5017-114">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="e5017-115">Revocaciones de certificados</span><span class="sxs-lookup"><span data-stu-id="e5017-115">Certificate revocations</span></span></li>
<li><span data-ttu-id="e5017-116">Raíces de confianza (reservadas)</span><span class="sxs-lookup"><span data-stu-id="e5017-116">Trusted roots (reserved)</span></span></li>
</ul>
<span data-ttu-id="e5017-117">La lista de raíces de confianza no se usa actualmente y está reservada para su uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e5017-117">The list of trusted roots is currently not used, and is reserved for future use.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5017-118">Entradas extensibles</span><span class="sxs-lookup"><span data-stu-id="e5017-118">Extensible entries</span></span></td>
<td><span data-ttu-id="e5017-119">Contiene información utilizada por otros componentes.</span><span class="sxs-lookup"><span data-stu-id="e5017-119">Contains information used by other components.</span></span> <span data-ttu-id="e5017-120">Esta sección no es relevante para OPM.</span><span class="sxs-lookup"><span data-stu-id="e5017-120">This section is not relevant to OPM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5017-121">Renovaciones:</span><span class="sxs-lookup"><span data-stu-id="e5017-121">Renewals:</span></span></td>
<td><span data-ttu-id="e5017-122">Contiene GUID que definen Windows Update identificadores.</span><span class="sxs-lookup"><span data-stu-id="e5017-122">Contains GUIDs that define Windows Update identifiers.</span></span> <span data-ttu-id="e5017-123">Esta sección contiene identificadores para las listas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e5017-123">This section contains identifiers for the following lists:</span></span>
<ul>
<li><span data-ttu-id="e5017-124">Revocaciones binarias de kernel</span><span class="sxs-lookup"><span data-stu-id="e5017-124">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="e5017-125">Revocaciones binarias en modo de usuario</span><span class="sxs-lookup"><span data-stu-id="e5017-125">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="e5017-126">Revocaciones de certificados</span><span class="sxs-lookup"><span data-stu-id="e5017-126">Certificate revocations</span></span></li>
</ul>
<span data-ttu-id="e5017-127">Una aplicación puede usar estos identificadores para solicitar una versión renovado de un binario revocado, si hay alguno disponible.</span><span class="sxs-lookup"><span data-stu-id="e5017-127">An application can use these identifiers to request a renewed version of a revoked binary, if one is available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5017-128">Firma: sección Principal</span><span class="sxs-lookup"><span data-stu-id="e5017-128">Signature: Core section</span></span></td>
<td><span data-ttu-id="e5017-129">Firma las secciones de encabezado y núcleo.</span><span class="sxs-lookup"><span data-stu-id="e5017-129">Signs the header and core sections.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5017-130">Firma: sección Extensible</span><span class="sxs-lookup"><span data-stu-id="e5017-130">Signature: Extensible section</span></span></td>
<td><span data-ttu-id="e5017-131">Firma el encabezado y las secciones extensibles.</span><span class="sxs-lookup"><span data-stu-id="e5017-131">Signs the header and extensible sections.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e5017-132">El encabezado GRL es una [**estructura GRL \_ HEADER.**](grl-header.md)</span><span class="sxs-lookup"><span data-stu-id="e5017-132">The GRL header is a [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="e5017-133">El **miembro dwSequenceNumber** de la estructura contiene el número de versión grl.</span><span class="sxs-lookup"><span data-stu-id="e5017-133">The **dwSequenceNumber** member of the structure contains the GRL version number.</span></span> <span data-ttu-id="e5017-134">Este número se incrementa cada vez que se actualiza la GRL y se coloca una nueva versión en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e5017-134">This number is incremented whenever the GRL is updated and a new version placed on the user's computer.</span></span>

<span data-ttu-id="e5017-135">Los certificados OPM revocados se enumeran en la lista de revocaciones de certificados de la sección Core.</span><span class="sxs-lookup"><span data-stu-id="e5017-135">Revoked OPM certificates are listed in the certificate revocations list of the Core section.</span></span> <span data-ttu-id="e5017-136">Cada entrada Core de grl es una matriz de 20 bytes que contiene el hash SHA-1 de la clave pública del certificado revocado.</span><span class="sxs-lookup"><span data-stu-id="e5017-136">Each Core entry in the GRL is a 20-byte array that contains the SHA-1 hash of the public key of the revoked certificate.</span></span>

<span data-ttu-id="e5017-137">Las secciones Firma contienen firmas que se pueden usar para comprobar que la GRL no se ha alterado.</span><span class="sxs-lookup"><span data-stu-id="e5017-137">The Signature sections contains signatures that can be used to verify that the GRL has not been tampered with.</span></span> <span data-ttu-id="e5017-138">Cada sección signature contiene una estructura [**MF \_ SIGNATURE.**](mf-signature.md)</span><span class="sxs-lookup"><span data-stu-id="e5017-138">Each Signature sections contains am [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="e5017-139">La primera firma firma el encabezado más la sección Core.</span><span class="sxs-lookup"><span data-stu-id="e5017-139">The first signature signs the header plus the Core section.</span></span> <span data-ttu-id="e5017-140">La segunda firma firma el encabezado más la sección Extensible; esta firma no es relevante para OPM.</span><span class="sxs-lookup"><span data-stu-id="e5017-140">The second signature signs the header plus the Extensible section; this signature is not relevant to OPM.</span></span>

<span data-ttu-id="e5017-141">Para asegurarse de que la GRL no se ha alterado, compruebe la firma como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="e5017-141">To ensure that the GRL itself has not been tampered with, verify the signature as follows:</span></span>

1.  <span data-ttu-id="e5017-142">Busque el inicio de la [**estructura MF \_ SIGNATURE.**](mf-signature.md)</span><span class="sxs-lookup"><span data-stu-id="e5017-142">Find the start of the [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="e5017-143">La ubicación de la **estructura MF \_ SIGNATURE** se da en el **miembro cbSignatureCoreOffset** de la [**estructura GRL \_ HEADER.**](grl-header.md)</span><span class="sxs-lookup"><span data-stu-id="e5017-143">The location of the **MF\_SIGNATURE** structure is given in the **cbSignatureCoreOffset** member of the [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="e5017-144">La ubicación se especifica como un desplazamiento en bytes desde el inicio de grl.</span><span class="sxs-lookup"><span data-stu-id="e5017-144">The location is specified as an offset in bytes from the start of the GRL.</span></span>
2.  <span data-ttu-id="e5017-145">Analice la estructura [**MF \_ SIGNATURE**](mf-signature.md) como una firma PKCS \# 7 con una cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="e5017-145">Parse the [**MF\_SIGNATURE**](mf-signature.md) structure as a PKCS \#7 signature with a certificate chain.</span></span>
3.  <span data-ttu-id="e5017-146">Compruebe la cadena de certificados hasta una raíz de confianza.</span><span class="sxs-lookup"><span data-stu-id="e5017-146">Verify the certificate chain up to a trusted root.</span></span>
4.  <span data-ttu-id="e5017-147">Compruebe que el certificado hoja tiene el siguiente identificador de objeto en el EKU: "1.3.6.1.4.1.311.10.5.4".</span><span class="sxs-lookup"><span data-stu-id="e5017-147">Verify that the leaf certificate has the following object identifier in the EKU: "1.3.6.1.4.1.311.10.5.4".</span></span>
5.  <span data-ttu-id="e5017-148">Calcule un hash de los bytes que incluyen el encabezado y las secciones principales de grl.</span><span class="sxs-lookup"><span data-stu-id="e5017-148">Compute a hash of the bytes that include the header and the core sections of the GRL.</span></span>
6.  <span data-ttu-id="e5017-149">Compruebe que el hash coincide con la firma del certificado hoja.</span><span class="sxs-lookup"><span data-stu-id="e5017-149">Verify that the hash matches the signature in the leaf certificate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5017-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5017-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5017-151">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="e5017-151">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="e5017-152">**ENCABEZADO \_ GRL**</span><span class="sxs-lookup"><span data-stu-id="e5017-152">**GRL\_HEADER**</span></span>](grl-header.md)
</dt> <dt>

[<span data-ttu-id="e5017-153">**MF \_ SIGNATURE**</span><span class="sxs-lookup"><span data-stu-id="e5017-153">**MF\_SIGNATURE**</span></span>](mf-signature.md)
</dt> </dl>

 

 



