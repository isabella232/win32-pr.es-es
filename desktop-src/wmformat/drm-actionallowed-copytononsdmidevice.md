---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: El \_ atributo CopyToNonSDMIDevice de DRM ActionAllowed \_ indica si se permite copiar el contenido en un dispositivo que no es de SDMI.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077344"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a>\_CopyToNonSDMIDevice ACTIONALLOWED \_ DRM

El **atributo \_ \_ CopyToNonSDMIDevice de DRM ActionAllowed** indica si se permite copiar el contenido en un dispositivo que no es de SDMI

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

Las licencias de Windows Media DRM 10 usan la acción de copia para restringir la copia a los dispositivos. Debe comprobar la propiedad [**de \_ \_ copia de ActionAllowed de DRM**](drm-actionallowed-copy.md) para determinar si se permite la copia.

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




