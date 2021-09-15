---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: El atributo \_ CopyToNonSDMIDevice de acción DRM permitido indica si se permite copiar el contenido en un dispositivo que no \_ es SDMI.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice windows Media Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467092"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a>Acción \_ de DRMAllowed \_ CopyToNonSDMIDevice

El **atributo \_ \_ CopyToNonSDMIDevice** de acción DRM permitido indica si se permite copiar el contenido en un dispositivo que no es SDMI.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice

## <a name="data-type"></a>Tipo de datos

**WMT \_ TYPE \_ BOOL**

## <a name="remarks"></a>Observaciones

Windows Las licencias de DRM 10 multimedia usan la acción Copiar para restringir la copia a los dispositivos. Debe comprobar la propiedad [**Acción \_ DRMAllowed \_ Copy para**](drm-actionallowed-copy.md) determinar si se permite la copia.

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




