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
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467094"
---
# <a name="drm_actionallowed_copytocd"></a>Acción \_ de DRMAllowed \_ CopyToCD

El **atributo \_ ActionAllowed \_ CopyToCD de DRM** indica si el contenido se puede copiar en un CD.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD

## <a name="data-type"></a>Tipo de datos

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Observaciones

Windows Las licencias de DRM 10 multimedia usan la acción Copiar para restringir la copia en CD. Debe comprobar la propiedad [**Acción \_ DRMAllowed \_ Copy para**](drm-actionallowed-copy.md) determinar si se permite la copia.

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




