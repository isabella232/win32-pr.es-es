---
title: DRM_ActionAllowed_CopyToCD
description: El \_ atributo CopyToCD de DRM ActionAllowed \_ indica si se permite copiar el contenido en un CD.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105704899"
---
# <a name="drm_actionallowed_copytocd"></a><span data-ttu-id="bc6f0-104">\_CopyToCD ACTIONALLOWED \_ DRM</span><span class="sxs-lookup"><span data-stu-id="bc6f0-104">DRM\_ActionAllowed\_CopyToCD</span></span>

<span data-ttu-id="bc6f0-105">El **atributo \_ \_ CopyToCD de DRM ActionAllowed** indica si se permite copiar el contenido en un CD.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-105">The **DRM\_ActionAllowed\_CopyToCD** attribute indicates whether the content is allowed to be copied to a CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="bc6f0-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="bc6f0-106">Global Constant</span></span>

<span data-ttu-id="bc6f0-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="bc6f0-107">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>

## <a name="data-type"></a><span data-ttu-id="bc6f0-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bc6f0-108">Data Type</span></span>

<span data-ttu-id="bc6f0-109">**tipo de WMT \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="bc6f0-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="bc6f0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc6f0-110">Remarks</span></span>

<span data-ttu-id="bc6f0-111">Las licencias de Windows Media DRM 10 usan la acción de copia para restringir la copia a CD.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to CD.</span></span> <span data-ttu-id="bc6f0-112">Debe comprobar la propiedad [**de \_ \_ copia de ActionAllowed de DRM**](drm-actionallowed-copy.md) para determinar si se permite la copia.</span><span class="sxs-lookup"><span data-stu-id="bc6f0-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="bc6f0-113">Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="bc6f0-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="bc6f0-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc6f0-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc6f0-115">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="bc6f0-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




