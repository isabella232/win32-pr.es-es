---
title: DRM_ActionAllowed_Copy
description: El \_ atributo de copia ActionAllowed de DRM \_ indica si se permite copiar el contenido en un dispositivo, como un reproductor portátil.
ms.assetid: 3a391a14-ccbb-43c6-b362-0db53d93ab79
keywords:
- DRM_ActionAllowed_Copy formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_Copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea4a890ae03d3adf3b28bb2dce03e2eac5578abe
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105704900"
---
# <a name="drm_actionallowed_copy"></a>\_Copia de ActionAllowed de DRM \_

El atributo de **\_ \_ copia ActionAllowed de DRM** indica si se permite copiar el contenido en un dispositivo, como un reproductor portátil.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

En Windows Media DRM 10, todas las operaciones de copia están restringidas mediante la acción de copia.

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




