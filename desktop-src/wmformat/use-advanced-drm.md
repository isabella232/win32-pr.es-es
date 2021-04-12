---
title: Use_Advanced_DRM
description: El \_ atributo usar \_ DRM avanzada especifica si se utiliza DRM versión 7 para proteger el contenido.
ms.assetid: a385152f-d72e-473c-93a0-5697659df23c
keywords:
- Use_Advanced_DRM formato de Windows Media
topic_type:
- apiref
api_name:
- Use_Advanced_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8720d5b401a1a1cec5240920bfb4a3811012420
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104270738"
---
# <a name="use_advanced_drm"></a>Usar \_ \_ DRM avanzada

El **atributo \_ usar \_ DRM avanzada** especifica si se utiliza DRM versión 7 para proteger el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMUse \_ \_ DRM avanzada

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

Se trata de una propiedad de lectura y escritura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) y se establece mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). No se puede obtener acceso a esta propiedad desde el objeto de lector.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




