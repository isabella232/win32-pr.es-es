---
title: DRM_DRMHeader_ContentID
description: El \_ atributo DRMHeader \_ contentid de DRM contiene los objetos contentid generados por el propietario del contenido.
ms.assetid: fda38778-2fdf-4218-aad2-e4cf351d74e9
keywords:
- DRM_DRMHeader_ContentID formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66edd858451e5d1a58b2a91f9f2362d4cabe9da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994945"
---
# <a name="drm_drmheader_contentid"></a>DRMHeader de de DRM \_ \_

El **atributo \_ DRMHeader \_ contentid de DRM** contiene los objetos contentid generados por el propietario del contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ contentid

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Este atributo solo está presente con el contenido de la versión 7 de DRM. Se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Para establecer el identificador de contenido en el archivo mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , debe usar la propiedad de [**\_ contentid de DRM**](drm-contentid.md) .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




