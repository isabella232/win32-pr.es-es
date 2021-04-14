---
title: DRM_LicenseAcqURL
description: El \_ atributo LicenseAcqURL de DRM contiene la dirección de una página web a la que la aplicación cliente puede desplazarse para obtener una licencia de contenido para el contenido de la versión 7 de DRM.
ms.assetid: bee29e39-ded8-439d-9164-fc318cb535c0
keywords:
- DRM_LicenseAcqURL formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231efc4334a4d893b4bdd1e7545bd50b1bed2a5c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104533004"
---
# <a name="drm_licenseacqurl"></a><span data-ttu-id="61d53-104">\_LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="61d53-104">DRM\_LicenseAcqURL</span></span>

<span data-ttu-id="61d53-105">El **atributo \_ LicenseAcqURL de DRM** contiene la dirección de una página web a la que la aplicación cliente puede desplazarse para obtener una licencia de contenido para el contenido de la versión 7 de DRM.</span><span class="sxs-lookup"><span data-stu-id="61d53-105">The **DRM\_LicenseAcqURL** attribute contains the address of a Web page that the client application can navigate to in order to obtain a content license for DRM version 7 content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="61d53-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="61d53-106">Global Constant</span></span>

<span data-ttu-id="61d53-107">g \_ wszWMDRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="61d53-107">g\_wszWMDRM\_LicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="61d53-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="61d53-108">Data Type</span></span>

<span data-ttu-id="61d53-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="61d53-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="61d53-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61d53-110">Remarks</span></span>

<span data-ttu-id="61d53-111">Este atributo se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="61d53-111">This attribute can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="61d53-112">Se puede recuperar el mismo atributo de archivo mediante [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md).</span><span class="sxs-lookup"><span data-stu-id="61d53-112">The same file attribute can be retrieved using [**DRM\_DRMHeader\_LicenseAcqURL**](drm-drmheader-licenseacqurl.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="61d53-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="61d53-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d53-114">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="61d53-114">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




