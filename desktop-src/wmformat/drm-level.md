---
title: DRM_Level
description: '\_El nivel DRM es un atributo de licencia que el SDK de formato de Windows Media establece al crear una licencia local para los archivos protegidos con DRM versión 1.'
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358711"
---
# <a name="drm_level"></a>Nivel de DRM \_

**DRM \_ Level** es un atributo de licencia que el SDK de formato de Windows Media establece cuando crea una licencia local para archivos protegidos con DRM versión 1. Contiene el nivel de seguridad que la aplicación que realiza la llamada debe tener para tener acceso al contenido del archivo. El valor predeterminado es 150.

## <a name="global-constant"></a>Constante global

\_nivel g wszWMDRM \_

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ DWORD**

## <a name="remarks"></a>Observaciones

El nivel de seguridad de DRM de una aplicación viene determinado por la biblioteca wmstubdrm determinada a la que se vincula en tiempo de compilación. Para obtener más información sobre estos niveles de seguridad, consulte [obtención de la biblioteca DRM necesaria](obtaining-the-required-drm-library.md). Use [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para establecer esta propiedad al proteger los archivos ASF con DRM versión 1.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




