---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: El atributo \_ CopyToSDMIDevice de acción DRM permitido indica si se permite copiar el contenido \_ en un dispositivo SDMI.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice windows Media Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a868eab52d354672802ef1f736bbc2754af605371708247415cbe78a42442e1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809425"
---
# <a name="drm_actionallowed_copytosdmidevice"></a>Acción \_ drmAllowed \_ CopyToSDMIDevice

El **atributo \_ \_ CopyToSDMIDevice** de acción DRM permitido indica si se permite copiar el contenido en un dispositivo SDMI.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice

## <a name="data-type"></a>Tipo de datos

**WMT \_ TYPE \_ BOOL**

## <a name="remarks"></a>Comentarios

Windows Las licencias de DRM 10 multimedia usan la acción Copiar para restringir la copia a los dispositivos. Debe comprobar la propiedad [**Acción \_ DRMAllowed \_ Copy para**](drm-actionallowed-copy.md) determinar si se permite la copia.

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




