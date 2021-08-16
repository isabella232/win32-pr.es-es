---
title: Use_DRM
description: El atributo \_ Usar DRM indica al objeto de escritor que aplique la protección drm versión 1 al archivo actual.
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Use_DRM windows Media Format
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b802a7bef777fab4ed835aa3a1770169deaa6eeea9a7eddeb802fb2e4b0a9dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845306"
---
# <a name="use_drm"></a>Uso de \_ DRM

El **atributo \_ Usar DRM** indica al objeto de escritor que aplique la protección drm versión 1 al archivo actual.

## <a name="global-constant"></a>Constante global

g \_ wszWMUse \_ DRM

## <a name="data-type"></a>Tipo de datos

**WMT \_ TYPE \_ BOOL**

## <a name="remarks"></a>Comentarios

Use [**IWMHeaderInfo::SetAttribute para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) establecer esta propiedad en **TRUE** al crear contenido de la versión 1 de DRM. Esta propiedad no es accesible desde el objeto de lector.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




