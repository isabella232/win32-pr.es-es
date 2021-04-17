---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: El \_ atributo CopyToSDMIDevice de DRM ActionAllowed \_ indica si se permite copiar el contenido en un dispositivo de SDMI.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420216"
---
# <a name="drm_actionallowed_copytosdmidevice"></a>\_CopyToSDMIDevice ACTIONALLOWED \_ DRM

El **atributo \_ \_ CopyToSDMIDevice de DRM ActionAllowed** indica si se permite copiar el contenido en un dispositivo de SDMI.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

Las licencias de Windows Media DRM 10 usan la acción de copia para restringir la copia a los dispositivos. Debe comprobar la propiedad [**de \_ \_ copia de ActionAllowed de DRM**](drm-actionallowed-copy.md) para determinar si se permite la copia.

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




