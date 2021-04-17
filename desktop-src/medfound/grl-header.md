---
description: Contiene el encabezado de la lista de revocación global (GRL).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: Estructura de GRL_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659779"
---
# <a name="grl_header-structure"></a><span data-ttu-id="df40e-103">La \_ estructura del encabezado GRL</span><span class="sxs-lookup"><span data-stu-id="df40e-103">GRL\_HEADER structure</span></span>

<span data-ttu-id="df40e-104">Contiene el encabezado de la lista de revocación global (GRL).</span><span class="sxs-lookup"><span data-stu-id="df40e-104">Contains the global revocation list (GRL) header.</span></span>

## <a name="syntax"></a><span data-ttu-id="df40e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df40e-105">Syntax</span></span>


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a><span data-ttu-id="df40e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="df40e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="df40e-107">**wszIdentifier**</span><span class="sxs-lookup"><span data-stu-id="df40e-107">**wszIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-108">El identificador GRL.</span><span class="sxs-lookup"><span data-stu-id="df40e-108">The GRL identifier.</span></span> <span data-ttu-id="df40e-109">El valor siempre es L "MSGRL".</span><span class="sxs-lookup"><span data-stu-id="df40e-109">The value is always L"MSGRL".</span></span>

</dd> <dt>

<span data-ttu-id="df40e-110">**wFormatMajor**</span><span class="sxs-lookup"><span data-stu-id="df40e-110">**wFormatMajor**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-111">Número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="df40e-111">The major version number.</span></span> <span data-ttu-id="df40e-112">Actualmente, el valor debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="df40e-112">Currently the value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-113">**wFormatMinor**</span><span class="sxs-lookup"><span data-stu-id="df40e-113">**wFormatMinor**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-114">Número de versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="df40e-114">The minor version number.</span></span> <span data-ttu-id="df40e-115">Actualmente, el valor debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="df40e-115">Currently the value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-116">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="df40e-116">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-117">Un valor de **FILETIME** que especifica cuándo se creó el archivo.</span><span class="sxs-lookup"><span data-stu-id="df40e-117">A **FILETIME** value that specifies when the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-118">**dwSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="df40e-118">**dwSequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-119">Número de versión de GRL.</span><span class="sxs-lookup"><span data-stu-id="df40e-119">The GRL version number.</span></span> <span data-ttu-id="df40e-120">Actualmente, el valor debe ser al menos 3.</span><span class="sxs-lookup"><span data-stu-id="df40e-120">Currently the value must be at least 3</span></span>

</dd> <dt>

<span data-ttu-id="df40e-121">**dwForceRebootVersion**</span><span class="sxs-lookup"><span data-stu-id="df40e-121">**dwForceRebootVersion**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="df40e-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-123">**dwForceProcessRestartVersion**</span><span class="sxs-lookup"><span data-stu-id="df40e-123">**dwForceProcessRestartVersion**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-124">Reservado.</span><span class="sxs-lookup"><span data-stu-id="df40e-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-125">**cbRevocationSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="df40e-125">**cbRevocationSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-126">Desplazamiento, en bytes, desde el inicio del GRL hasta la sección principal.</span><span class="sxs-lookup"><span data-stu-id="df40e-126">The offset, in bytes, from the start of the GRL to the Core section.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-127">**cRevokedKernelBinaries**</span><span class="sxs-lookup"><span data-stu-id="df40e-127">**cRevokedKernelBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-128">El número de archivos binarios de kernel revocados que aparecen en el GRL.</span><span class="sxs-lookup"><span data-stu-id="df40e-128">The number of revoked kernel binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-129">**cRevokedUserBinaries**</span><span class="sxs-lookup"><span data-stu-id="df40e-129">**cRevokedUserBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-130">El número de archivos binarios de modo de usuario revocados que aparecen en el GRL.</span><span class="sxs-lookup"><span data-stu-id="df40e-130">The number of revoked user-mode binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-131">**cRevokedCertificates**</span><span class="sxs-lookup"><span data-stu-id="df40e-131">**cRevokedCertificates**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-132">El número de certificados revocados que aparecen en el GRL.</span><span class="sxs-lookup"><span data-stu-id="df40e-132">The number of revoked certificates listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-133">**cTrustedRoots**</span><span class="sxs-lookup"><span data-stu-id="df40e-133">**cTrustedRoots**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-134">El número de raíces de confianza enumeradas en el GRL.</span><span class="sxs-lookup"><span data-stu-id="df40e-134">The number of trusted roots listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-135">**cbExtensibleSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="df40e-135">**cbExtensibleSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-136">Desplazamiento, en bytes, desde el inicio del GRL hasta la sección extensible.</span><span class="sxs-lookup"><span data-stu-id="df40e-136">The offset, in bytes, from the start of the GRL to the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-137">**cExtensibleEntries**</span><span class="sxs-lookup"><span data-stu-id="df40e-137">**cExtensibleEntries**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-138">El número de entradas en la sección extensible.</span><span class="sxs-lookup"><span data-stu-id="df40e-138">The number of entries in the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-139">**cbRenewalSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="df40e-139">**cbRenewalSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-140">Desplazamiento, en bytes, desde el inicio del GRL hasta la sección de renovación.</span><span class="sxs-lookup"><span data-stu-id="df40e-140">The offset, in bytes, from the start of the GRL to the Renewals section.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-141">**cRevokedKernelBinaryRenewals**</span><span class="sxs-lookup"><span data-stu-id="df40e-141">**cRevokedKernelBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-142">El número de renovaciones binarias del kernel enumeradas en el GRL.</span><span class="sxs-lookup"><span data-stu-id="df40e-142">The number of kernel binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-143">**cRevokedUserBinaryRenewals**</span><span class="sxs-lookup"><span data-stu-id="df40e-143">**cRevokedUserBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-144">El número de renovaciones binarias de modo de usuario enumeradas en el GRL.</span><span class="sxs-lookup"><span data-stu-id="df40e-144">The number of user-mode binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-145">**cRevokedCertificateRenewals**</span><span class="sxs-lookup"><span data-stu-id="df40e-145">**cRevokedCertificateRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-146">El número de renovaciones de certificado enumeradas en el GRL.</span><span class="sxs-lookup"><span data-stu-id="df40e-146">The number of certificate renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-147">**cbSignatureCoreOffset**</span><span class="sxs-lookup"><span data-stu-id="df40e-147">**cbSignatureCoreOffset**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-148">Desplazamiento, en bytes, desde el inicio del GRL hasta la firma de la sección principal.</span><span class="sxs-lookup"><span data-stu-id="df40e-148">The offset, in bytes, from the start of the GRL to the Core section signature.</span></span>

</dd> <dt>

<span data-ttu-id="df40e-149">**cbSignatureExtOffset**</span><span class="sxs-lookup"><span data-stu-id="df40e-149">**cbSignatureExtOffset**</span></span>
</dt> <dd>

<span data-ttu-id="df40e-150">Desplazamiento, en bytes, desde el inicio del GRL hasta la firma de la sección extensible.</span><span class="sxs-lookup"><span data-stu-id="df40e-150">The offset, in bytes, from the start of the GRL to the Extensible section signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df40e-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df40e-151">Remarks</span></span>

<span data-ttu-id="df40e-152">Todos los enteros del GRL tienen un orden de bytes Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="df40e-152">All integers in the GRL have little-endian byte ordering.</span></span> <span data-ttu-id="df40e-153">Todas las estructuras se alinean con límites de 1 byte.</span><span class="sxs-lookup"><span data-stu-id="df40e-153">All structures are aligned to 1-byte boundaries.</span></span>

<span data-ttu-id="df40e-154">Esta estructura no se declara en un encabezado de SDK.</span><span class="sxs-lookup"><span data-stu-id="df40e-154">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="df40e-155">Para usar esta estructura, agregue la declaración que se muestra aquí al código fuente.</span><span class="sxs-lookup"><span data-stu-id="df40e-155">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="df40e-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df40e-156">Requirements</span></span>



| <span data-ttu-id="df40e-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="df40e-157">Requirement</span></span> | <span data-ttu-id="df40e-158">Value</span><span class="sxs-lookup"><span data-stu-id="df40e-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="df40e-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df40e-159">Minimum supported client</span></span><br/> | <span data-ttu-id="df40e-160">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="df40e-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="df40e-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df40e-161">Minimum supported server</span></span><br/> | <span data-ttu-id="df40e-162">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="df40e-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df40e-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="df40e-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df40e-164">Revocación de certificados OPM</span><span class="sxs-lookup"><span data-stu-id="df40e-164">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="df40e-165">Estructuras OPM</span><span class="sxs-lookup"><span data-stu-id="df40e-165">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




