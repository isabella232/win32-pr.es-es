---
title: DRM_DRMHeader_SubscriptionContentID
description: El atributo \_ DRMHeader \_ SubscriptionContentID de DRM contiene el identificador de contenido de la suscripción.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID windows Media Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b273cf95d2bbb271b055eeff3da80a788a38c88bb2e87db37f5a73e6e918e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086155"
---
# <a name="drm_drmheader_subscriptioncontentid"></a>DRM \_ DRMHeader \_ SubscriptionContentID

El **atributo \_ DRMHeader \_ SubscriptionContentID de DRM** contiene el identificador de contenido de la suscripción.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID

## <a name="data-type"></a>Tipo de datos

**CADENA DE TIPO WMT \_ \_**

## <a name="remarks"></a>Comentarios

Este atributo solo está presente con contenido drm versión 7. El identificador de contenido de la suscripción es opcional y lo determina únicamente el creador del contenido. El objeto writer no hace nada con este atributo. Se puede establecer mediante [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




