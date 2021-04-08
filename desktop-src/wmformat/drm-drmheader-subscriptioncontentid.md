---
title: DRM_DRMHeader_SubscriptionContentID
description: El \_ atributo SubscriptionContentID de DRM DRMHeader \_ contiene el identificador de contenido de la suscripción.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151665777aa6b68078361eb6e063e374a52f30bf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994944"
---
# <a name="drm_drmheader_subscriptioncontentid"></a><span data-ttu-id="46473-104">\_SubscriptionContentID DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="46473-104">DRM\_DRMHeader\_SubscriptionContentID</span></span>

<span data-ttu-id="46473-105">El **atributo \_ \_ SubscriptionContentID de DRM DRMHEADER** contiene el identificador de contenido de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="46473-105">The **DRM\_DRMHeader\_SubscriptionContentID** attribute contains the subscription content ID.</span></span>

## <a name="global-constant"></a><span data-ttu-id="46473-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="46473-106">Global Constant</span></span>

<span data-ttu-id="46473-107">g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="46473-107">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span>

## <a name="data-type"></a><span data-ttu-id="46473-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="46473-108">Data Type</span></span>

<span data-ttu-id="46473-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="46473-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="46473-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46473-110">Remarks</span></span>

<span data-ttu-id="46473-111">Este atributo solo está presente con el contenido de la versión 7 de DRM.</span><span class="sxs-lookup"><span data-stu-id="46473-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="46473-112">El identificador de contenido de la suscripción es opcional y está determinado únicamente por el creador del contenido.</span><span class="sxs-lookup"><span data-stu-id="46473-112">The subscription content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="46473-113">El objeto de escritor no hace nada con este atributo.</span><span class="sxs-lookup"><span data-stu-id="46473-113">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="46473-114">Se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="46473-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="46473-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="46473-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46473-116">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="46473-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




