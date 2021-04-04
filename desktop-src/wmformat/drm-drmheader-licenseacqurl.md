---
title: DRM_DRMHeader_LicenseAcqURL
description: El \_ atributo DRMHeader de DRM \_ LicenseAcqURL contiene la dirección URL de adquisición de licencias para una licencia de DRM versión 7.
ms.assetid: 00c788b4-b291-4df5-9926-0badc7357faf
keywords:
- DRM_DRMHeader_LicenseAcqURL formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c394df01703befbb17c61b340b8ea4239740ac3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077312"
---
# <a name="drm_drmheader_licenseacqurl"></a><span data-ttu-id="a4cc1-104">\_LicenseAcqURL DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="a4cc1-104">DRM\_DRMHeader\_LicenseAcqURL</span></span>

<span data-ttu-id="a4cc1-105">El **atributo \_ DRMHeader \_ de DRM LicenseAcqURL** contiene la dirección URL de adquisición de licencias para una licencia de DRM versión 7.</span><span class="sxs-lookup"><span data-stu-id="a4cc1-105">The **DRM\_DRMHeader\_LicenseAcqURL** attribute contains the license acquisition URL for a DRM version 7 license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a4cc1-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="a4cc1-106">Global Constant</span></span>

<span data-ttu-id="a4cc1-107">g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="a4cc1-107">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="a4cc1-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a4cc1-108">Data Type</span></span>

<span data-ttu-id="a4cc1-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="a4cc1-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="a4cc1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4cc1-110">Remarks</span></span>

<span data-ttu-id="a4cc1-111">Este atributo solo está presente con el contenido de la versión 7 de DRM.</span><span class="sxs-lookup"><span data-stu-id="a4cc1-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="a4cc1-112">Se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="a4cc1-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="a4cc1-113">Para establecer la dirección URL de adquisición de licencias en el archivo mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , debe usar la propiedad [**\_ LicenseAcqURL de DRM**](drm-licenseacqurl.md) .</span><span class="sxs-lookup"><span data-stu-id="a4cc1-113">To set the license acquisition URL on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_LicenseAcqURL**](drm-licenseacqurl.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4cc1-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4cc1-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4cc1-115">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="a4cc1-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




