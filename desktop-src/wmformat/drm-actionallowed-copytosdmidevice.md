---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: El atributo \_ ActionAllowed CopyToSDMIDevice de DRM indica si se permite copiar el contenido \_ en un dispositivo SDMI.
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
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467091"
---
# <a name="drm_actionallowed_copytosdmidevice"></a>Acción \_ de DRMAllowed \_ CopyToSDMIDevice

El **atributo \_ ActionAllowed \_ CopyToSDMIDevice** de DRM indica si se permite copiar el contenido en un dispositivo SDMI.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice

## <a name="data-type"></a>Tipo de datos

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Observaciones

Windows Las licencias de DRM 10 multimedia usan la acción Copiar para restringir la copia a los dispositivos. Debe comprobar la propiedad [**Acción \_ DRMAllowed \_ Copy para**](drm-actionallowed-copy.md) determinar si se permite la copia.

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




