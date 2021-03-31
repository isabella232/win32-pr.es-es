---
title: Constantes de WINBIO_BIOMETRIC_SUBTYPE (Winbio \_ Types. h)
description: Proporcionar información sobre una medida biométrica.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996614"
---
# <a name="winbio_biometric_subtype-constants"></a><span data-ttu-id="7100e-103">WINBIO \_ constantes de \_ subtipo de biométrico</span><span class="sxs-lookup"><span data-stu-id="7100e-103">WINBIO\_BIOMETRIC\_SUBTYPE Constants</span></span>

<span data-ttu-id="7100e-104">**WINBIO \_ Las constantes de \_ SUBtipo biométrico** se usan en el plataforma de biometría de Windows para proporcionar información adicional sobre una medida biométrica.</span><span class="sxs-lookup"><span data-stu-id="7100e-104">**WINBIO\_BIOMETRIC\_SUBTYPE** constants are used throughout the Windows Biometric Framework to provide additional information about a biometric measurement.</span></span> <span data-ttu-id="7100e-105">Se pueden usar las siguientes constantes cuando no se requiere ningún subtipo o cuando se requiere un subtipo.</span><span class="sxs-lookup"><span data-stu-id="7100e-105">The following constants can be used when no subtype is required or when any subtype is required.</span></span>



| <span data-ttu-id="7100e-106">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="7100e-106">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="7100e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7100e-107">Description</span></span>                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <span data-ttu-id="7100e-108"><dt>**WINBIO \_ \_No \_ información de subtipos**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="7100e-108"><dt>**WINBIO\_SUBTYPE\_NO\_INFORMATION**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="7100e-109">No hay información de subtipos.</span><span class="sxs-lookup"><span data-stu-id="7100e-109">No subtype information.</span></span><br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <span data-ttu-id="7100e-110"><dt>**WINBIO \_ Subtipo \_**</dt> de <dt>0xFF</dt></span><span class="sxs-lookup"><span data-stu-id="7100e-110"><dt>**WINBIO\_SUBTYPE\_ANY**</dt> <dt>0xFF</dt></span></span> </dl>                                   | <span data-ttu-id="7100e-111">Cualquier subtipo.</span><span class="sxs-lookup"><span data-stu-id="7100e-111">Any subtype.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="7100e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7100e-112">Remarks</span></span>

<span data-ttu-id="7100e-113">Para buscar los subtipos biométricos disponibles para un tipo de biométrico determinado, use la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="7100e-113">To find the available biometric subtypes for a particular biometric type, use the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7100e-114"><strong>WINBIO_BIOMETRIC_TYPE</strong> valor</span><span class="sxs-lookup"><span data-stu-id="7100e-114"><strong>WINBIO_BIOMETRIC_TYPE</strong> value</span></span></th>
<th><span data-ttu-id="7100e-115">Temas para buscar valores de <strong>WINBIO_BIOMETRIC_SUBTYPE</strong></span><span class="sxs-lookup"><span data-stu-id="7100e-115">Topic(s) to find <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7100e-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span><span class="sxs-lookup"><span data-stu-id="7100e-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span></span></td>
<td><span data-ttu-id="7100e-117"><a href="winbio-ansi-385-face-constants.md"><strong>Constantes de WINBIO_ANSI_385_FACE</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="7100e-117"><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="7100e-118">Estos valores solo se aplican a Windows 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7100e-118">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7100e-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span><span class="sxs-lookup"><span data-stu-id="7100e-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span></span></td>
<td><span data-ttu-id="7100e-120">Uno de los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="7100e-120">One of the following topics:</span></span>
<ul>
<li><span data-ttu-id="7100e-121"><a href="winbio-ansi-381-format-constants.md"><strong>Constantes de WINBIO_ANSI_381_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="7100e-121"><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT Constants</strong></a></span></span></li>
<li><span data-ttu-id="7100e-122"><a href="winbio-ansi-381-img-constants.md"><strong>Constantes de WINBIO_ANSI_381_IMG</strong></a></span><span class="sxs-lookup"><span data-stu-id="7100e-122"><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG Constants</strong></a></span></span></li>
<li><span data-ttu-id="7100e-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>Constantes de WINBIO_ANSI_381_IMG_ACQ</strong></a></span><span class="sxs-lookup"><span data-stu-id="7100e-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ Constants</strong></a></span></span></li>
<li><span data-ttu-id="7100e-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>Constantes de WINBIO_ANSI_381_IMP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7100e-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE Constants</strong></a></span></span></li>
<li><span data-ttu-id="7100e-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>Constantes de WINBIO_ANSI_381_PIXELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="7100e-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS Constants</strong></a></span></span></li>
<li><span data-ttu-id="7100e-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>Constantes de huella digital WINBIO_ANSI_381_POS</strong></a></span><span class="sxs-lookup"><span data-stu-id="7100e-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS Fingerprint Constants</strong></a></span></span></li>
<li><span data-ttu-id="7100e-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>Constantes de WINBIO_ANSI_381_POS_Palm</strong></a></span><span class="sxs-lookup"><span data-stu-id="7100e-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm Constants</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7100e-128"><strong>WINBIO_TYPE_IRIS</strong></span><span class="sxs-lookup"><span data-stu-id="7100e-128"><strong>WINBIO_TYPE_IRIS</strong></span></span></td>
<td><span data-ttu-id="7100e-129"><a href="winbio-iris-constants.md"><strong>Constantes de WINBIO_IRIS</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="7100e-129"><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="7100e-130">Estos valores solo se aplican a Windows 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7100e-130">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7100e-131"><strong>WINBIO_TYPE_VOICE</strong></span><span class="sxs-lookup"><span data-stu-id="7100e-131"><strong>WINBIO_TYPE_VOICE</strong></span></span></td>
<td><span data-ttu-id="7100e-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>Constantes de WINBIO_VOICE</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="7100e-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="7100e-133">Estos valores solo se aplican a Windows 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7100e-133">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7100e-134">Para obtener más información, consulte [constantes de aplicación cliente](client-application-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7100e-134">For more information, see [Client Application Constants](client-application-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7100e-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7100e-135">Requirements</span></span>



| <span data-ttu-id="7100e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7100e-136">Requirement</span></span> | <span data-ttu-id="7100e-137">Value</span><span class="sxs-lookup"><span data-stu-id="7100e-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7100e-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7100e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7100e-139">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7100e-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="7100e-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7100e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7100e-141">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7100e-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7100e-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7100e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7100e-143"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7100e-143"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





