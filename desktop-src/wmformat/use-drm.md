---
title: Use_DRM
description: El \_ atributo use DRM indica al objeto de escritor que aplique la protección de DRM versión 1 al archivo actual.
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Use_DRM formato de Windows Media
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fcb010855ac4660792a7c579556001d5d7c4c96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532974"
---
# <a name="use_drm"></a>Usar \_ DRM

El atributo **use \_ DRM** indica al objeto de escritor que aplique la protección de DRM versión 1 al archivo actual.

## <a name="global-constant"></a>Constante global

g \_ wszWMUse \_ DRM

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

Use [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para establecer esta propiedad en **true** al crear el contenido de la versión 1 de DRM. No se puede obtener acceso a esta propiedad desde el objeto de lector.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




