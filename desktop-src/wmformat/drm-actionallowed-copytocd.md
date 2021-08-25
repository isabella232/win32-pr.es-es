---
title: DRM_ActionAllowed_CopyToCD
description: El atributo \_ ActionAllowed CopyToCD de DRM indica si el contenido se puede \_ copiar en un CD.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD windows Media Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852d44a4c812aed0d2f188b5ab18e9b74a1813bd9605bf348ca23b96b72f7d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809415"
---
# <a name="drm_actionallowed_copytocd"></a>Acción \_ de DRMAllowed \_ CopyToCD

El **atributo \_ ActionAllowed \_ CopyToCD de DRM** indica si el contenido se puede copiar en un CD.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD

## <a name="data-type"></a>Tipo de datos

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentarios

Windows Las licencias de DRM 10 multimedia usan la acción Copiar para restringir la copia a CD. Debe comprobar la propiedad [**Acción \_ DRMAllowed \_ Copy para**](drm-actionallowed-copy.md) determinar si se permite la copia.

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




