---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: El \_ atributo CopyToSDMIDevice de DRM ActionAllowed \_ indica si se permite copiar el contenido en un dispositivo de SDMI.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420216"
---
# <a name="drm_actionallowed_copytosdmidevice"></a><span data-ttu-id="7532a-104">\_CopyToSDMIDevice ACTIONALLOWED \_ DRM</span><span class="sxs-lookup"><span data-stu-id="7532a-104">DRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

<span data-ttu-id="7532a-105">El **atributo \_ \_ CopyToSDMIDevice de DRM ActionAllowed** indica si se permite copiar el contenido en un dispositivo de SDMI.</span><span class="sxs-lookup"><span data-stu-id="7532a-105">The **DRM\_ActionAllowed\_CopyToSDMIDevice** attribute indicates whether the content is allowed to be copied to an SDMI device.</span></span>

## <a name="global-constant"></a><span data-ttu-id="7532a-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="7532a-106">Global Constant</span></span>

<span data-ttu-id="7532a-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="7532a-107">g\_wszWMDRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="7532a-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7532a-108">Data Type</span></span>

<span data-ttu-id="7532a-109">**tipo de WMT \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="7532a-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="7532a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7532a-110">Remarks</span></span>

<span data-ttu-id="7532a-111">Las licencias de Windows Media DRM 10 usan la acción de copia para restringir la copia a los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7532a-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="7532a-112">Debe comprobar la propiedad [**de \_ \_ copia de ActionAllowed de DRM**](drm-actionallowed-copy.md) para determinar si se permite la copia.</span><span class="sxs-lookup"><span data-stu-id="7532a-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="7532a-113">Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="7532a-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="7532a-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="7532a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7532a-115">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="7532a-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




