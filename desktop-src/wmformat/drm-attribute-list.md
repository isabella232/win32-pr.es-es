---
title: Lista de atributos de DRM
description: Lista de atributos de DRM
ms.assetid: 222ef91c-b776-4de8-b1ad-88c2beca05aa
keywords:
- SDK de Windows Media Format, atributos
- Advanced Systems Format (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- atributos, administración de derechos digitales (DRM)
- Administración de derechos digitales (DRM), atributos
- DRM (administración de derechos digitales), atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3beccc33a48f57015040f06c140a55f5f9691daa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714251"
---
# <a name="drm-attribute-list"></a><span data-ttu-id="ddc90-109">Lista de atributos de DRM</span><span class="sxs-lookup"><span data-stu-id="ddc90-109">DRM Attribute List</span></span>

<span data-ttu-id="ddc90-110">Para mayor comodidad, en la tabla siguiente se enumeran todos los atributos de archivo relacionados con DRM.</span><span class="sxs-lookup"><span data-stu-id="ddc90-110">For convenience, the following table lists all the DRM-related file attributes.</span></span> <span data-ttu-id="ddc90-111">(Estos atributos también se enumeran en la tabla de todos los atributos de la [lista de atributos](attribute-list.md)).</span><span class="sxs-lookup"><span data-stu-id="ddc90-111">(These attributes are also listed in the table of all attributes under [Attribute List](attribute-list.md).)</span></span>

<span data-ttu-id="ddc90-112">Las aplicaciones pueden establecer estos valores cuando se escriben archivos DRM y se pueden recuperar cuando se leen.</span><span class="sxs-lookup"><span data-stu-id="ddc90-112">Applications can set these values when writing DRM files and can retrieve them when reading.</span></span>



| <span data-ttu-id="ddc90-113">Atributo de archivo DRM</span><span class="sxs-lookup"><span data-stu-id="ddc90-113">DRM file attribute</span></span>                                                                   | <span data-ttu-id="ddc90-114">Identificador global</span><span class="sxs-lookup"><span data-stu-id="ddc90-114">Global identifier</span></span>                             | <span data-ttu-id="ddc90-115">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ddc90-115">Data type</span></span>             |
|--------------------------------------------------------------------------------------|-----------------------------------------------|-----------------------|
| [<span data-ttu-id="ddc90-116">**ContentID de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-116">**DRM\_ContentID**</span></span>](drm-contentid.md)                                              | <span data-ttu-id="ddc90-117">g \_ wszWMDRM \_ contentid</span><span class="sxs-lookup"><span data-stu-id="ddc90-117">g\_wszWMDRM\_ContentID</span></span>                        | <span data-ttu-id="ddc90-118">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-118">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-119">**\_ContentDistributor DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-119">**DRM\_DRMHeader\_ContentDistributor**</span></span>](drm-drmheader-contentdistributor.md)       | <span data-ttu-id="ddc90-120">g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="ddc90-120">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>    | <span data-ttu-id="ddc90-121">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-121">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-122">**DRMHeader de de DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-122">**DRM\_DRMHeader\_ContentID**</span></span>](drm-drmheader-contentid.md)                         | <span data-ttu-id="ddc90-123">g \_ wszWMDRM \_ DRMHeader \_ contentid</span><span class="sxs-lookup"><span data-stu-id="ddc90-123">g\_wszWMDRM\_DRMHeader\_ContentID</span></span>             | <span data-ttu-id="ddc90-124">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-124">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-125">**\_IndividualizedVersion DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-125">**DRM\_DRMHeader\_IndividualizedVersion**</span></span>](drm-drmheader-individualizedversion.md) | <span data-ttu-id="ddc90-126">g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="ddc90-126">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span> | <span data-ttu-id="ddc90-127">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-127">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-128">**ID. de DRMHeader de DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-128">**DRM\_DRMHeader\_KeyID**</span></span>](drm-drmheader-keyid.md)                                 | <span data-ttu-id="ddc90-129">\_wszWMDRM \_ DRMHeader ID. de cuenta \_</span><span class="sxs-lookup"><span data-stu-id="ddc90-129">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>                 | <span data-ttu-id="ddc90-130">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-130">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-131">**\_LicenseAcqURL DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-131">**DRM\_DRMHeader\_LicenseAcqURL**</span></span>](drm-drmheader-licenseacqurl.md)                 | <span data-ttu-id="ddc90-132">g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="ddc90-132">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>         | <span data-ttu-id="ddc90-133">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-133">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-134">**\_SubscriptionContentID DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-134">**DRM\_DRMHeader\_SubscriptionContentID**</span></span>](drm-drmheader-subscriptioncontentid.md) | <span data-ttu-id="ddc90-135">g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="ddc90-135">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span> | <span data-ttu-id="ddc90-136">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-136">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-137">**\_DRMHEADER DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-137">**DRM\_DRMHeader**</span></span>](drm-drmheader.md)                                              | <span data-ttu-id="ddc90-138">g \_ wszWMDRM \_ DRMHeader</span><span class="sxs-lookup"><span data-stu-id="ddc90-138">g\_wszWMDRM\_DRMHeader</span></span>                        | <span data-ttu-id="ddc90-139">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-139">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-140">**\_INDIVIDUALIZEDVERSION DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-140">**DRM\_IndividualizedVersion**</span></span>](drm-individualizedversion.md)                      | <span data-ttu-id="ddc90-141">g \_ wszWMDRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="ddc90-141">g\_wszWMDRM\_IndividualizedVersion</span></span>            | <span data-ttu-id="ddc90-142">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-142">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-143">**ID. de ID \_ de DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-143">**DRM\_KeyID**</span></span>](drm-keyid.md)                                                      | <span data-ttu-id="ddc90-144">ID. de \_ wszWMDRM g \_</span><span class="sxs-lookup"><span data-stu-id="ddc90-144">g\_wszWMDRM\_KeyID</span></span>                            | <span data-ttu-id="ddc90-145">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-145">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-146">**\_LASIGNATURECERT DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-146">**DRM\_LASignatureCert**</span></span>](drm-lasignaturecert.md)                                  | <span data-ttu-id="ddc90-147">g \_ wszWMDRM \_ LASignatureCert</span><span class="sxs-lookup"><span data-stu-id="ddc90-147">g\_wszWMDRM\_LASignatureCert</span></span>                  | <span data-ttu-id="ddc90-148">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-148">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-149">**\_LASIGNATURELICSRVCERT DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-149">**DRM\_LASignatureLicSrvCert**</span></span>](drm-lasignaturelicsrvcert.md)                      | <span data-ttu-id="ddc90-150">g \_ wszWMDRM \_ LASignatureLicSrvCert</span><span class="sxs-lookup"><span data-stu-id="ddc90-150">g\_wszWMDRM\_LASignatureLicSrvCert</span></span>            | <span data-ttu-id="ddc90-151">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-151">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-152">**\_LASIGNATUREPRIVKEY DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-152">**DRM\_LASignaturePrivKey**</span></span>](drm-lasignatureprivkey.md)                            | <span data-ttu-id="ddc90-153">g \_ wszWMDRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="ddc90-153">g\_wszWMDRM\_LASignaturePrivKey</span></span>               | <span data-ttu-id="ddc90-154">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-154">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-155">**\_LASIGNATUREROOTCERT DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-155">**DRM\_LASignatureRootCert**</span></span>](drm-lasignaturerootcert.md)                          | <span data-ttu-id="ddc90-156">g \_ wszWMDRM \_ LASignatureRootCert</span><span class="sxs-lookup"><span data-stu-id="ddc90-156">g\_wszWMDRM\_LASignatureRootCert</span></span>              | <span data-ttu-id="ddc90-157">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-157">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-158">**\_LICENSEACQURL DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-158">**DRM\_LicenseAcqURL**</span></span>](drm-licenseacqurl.md)                                      | <span data-ttu-id="ddc90-159">g \_ wszWMDRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="ddc90-159">g\_wszWMDRM\_LicenseAcqURL</span></span>                    | <span data-ttu-id="ddc90-160">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-160">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="ddc90-161">**\_V1LICENSEACQURL DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-161">**DRM\_V1LicenseAcqURL**</span></span>](drm-v1licenseacqurl.md)                                  | <span data-ttu-id="ddc90-162">g \_ wszWMDRM \_ V1LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="ddc90-162">g\_wszWMDRM\_V1LicenseAcqURL</span></span>                  | <span data-ttu-id="ddc90-163">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ddc90-163">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ddc90-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ddc90-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddc90-165">**Atributos por tipo**</span><span class="sxs-lookup"><span data-stu-id="ddc90-165">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="ddc90-166">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="ddc90-166">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




