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
# <a name="drm_drmheader_subscriptioncontentid"></a>\_SubscriptionContentID DRMHEADER \_ DRM

El **atributo \_ \_ SubscriptionContentID de DRM DRMHEADER** contiene el identificador de contenido de la suscripción.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Este atributo solo está presente con el contenido de la versión 7 de DRM. El identificador de contenido de la suscripción es opcional y está determinado únicamente por el creador del contenido. El objeto de escritor no hace nada con este atributo. Se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




