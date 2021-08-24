---
title: DRM_DRMHeader_ContentID
description: El atributo \_ DRMHeader ContentID de DRM \_ contiene el contentID generado por el propietario del contenido.
ms.assetid: fda38778-2fdf-4218-aad2-e4cf351d74e9
keywords:
- DRM_DRMHeader_ContentID windows Media Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b17df75902ec41eed935a9b10dbbf4799c92bae2a54c76b4ed676c9e7a3a572
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586435"
---
# <a name="drm_drmheader_contentid"></a>DRM \_ DRMHeader \_ ContentID

El **atributo \_ DRMHeader \_ ContentID de DRM** contiene el contentID generado por el propietario del contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ ContentID

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Este atributo solo está presente con el contenido de la versión 7 de DRM. Se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Para establecer el identificador de contenido en el archivo [**mediante IWMDRMWriter::SetDRMAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) debe usar la [**propiedad \_ ContentID de DRM.**](drm-contentid.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




