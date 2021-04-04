---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: El \_ atributo CopyToNonSDMIDevice de DRM ActionAllowed \_ indica si se permite copiar el contenido en un dispositivo que no es de SDMI.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077344"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a><span data-ttu-id="968f9-104">\_CopyToNonSDMIDevice ACTIONALLOWED \_ DRM</span><span class="sxs-lookup"><span data-stu-id="968f9-104">DRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

<span data-ttu-id="968f9-105">El **atributo \_ \_ CopyToNonSDMIDevice de DRM ActionAllowed** indica si se permite copiar el contenido en un dispositivo que no es de SDMI</span><span class="sxs-lookup"><span data-stu-id="968f9-105">The **DRM\_ActionAllowed\_CopyToNonSDMIDevice** attribute indicates whether the content is allowed to be copied to a non-SDMI device</span></span>

## <a name="global-constant"></a><span data-ttu-id="968f9-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="968f9-106">Global Constant</span></span>

<span data-ttu-id="968f9-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="968f9-107">g\_wszWMDRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="968f9-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="968f9-108">Data Type</span></span>

<span data-ttu-id="968f9-109">**tipo de WMT \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="968f9-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="968f9-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="968f9-110">Remarks</span></span>

<span data-ttu-id="968f9-111">Las licencias de Windows Media DRM 10 usan la acción de copia para restringir la copia a los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="968f9-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="968f9-112">Debe comprobar la propiedad [**de \_ \_ copia de ActionAllowed de DRM**](drm-actionallowed-copy.md) para determinar si se permite la copia.</span><span class="sxs-lookup"><span data-stu-id="968f9-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="968f9-113">Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="968f9-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="968f9-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="968f9-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="968f9-115">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="968f9-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




