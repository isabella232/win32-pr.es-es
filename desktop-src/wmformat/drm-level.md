---
title: DRM_Level
description: Nivel de DRM es un atributo de licencia que el SDK de Windows Media Format establece cuando crea una licencia local para los archivos protegidos con \_ DRM versión 1.
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level windows Media Format
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4767f839c5d21610e7e425aea4a20a52c3cb0d8658848f578a33ca403f4ad60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848696"
---
# <a name="drm_level"></a>Nivel de \_ DRM

**DRM \_ Level** es un atributo de licencia que el SDK Windows Media Format establece cuando crea una licencia local para los archivos protegidos con DRM versión 1. Contiene el nivel de seguridad que debe tener la aplicación que realiza la llamada para acceder al contenido del archivo. El valor predeterminado es 150.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ Level

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

El nivel de seguridad de DRM de una aplicación viene determinado por la biblioteca wmstubdrm determinada a la que se vincula en tiempo de compilación. Para obtener más información sobre estos niveles de seguridad, [consulte Obtención de la biblioteca DRM necesaria.](obtaining-the-required-drm-library.md) Use [**IWMHeaderInfo::SetAttribute para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) establecer esta propiedad al proteger archivos ASF con DRM versión 1.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




