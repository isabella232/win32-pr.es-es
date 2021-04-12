---
title: DRM_DRMHeader_KeyID
description: El \_ \_ atributo de ID. de clave de DRMHEADER de DRM contiene el identificador de clave para el archivo.
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- DRM_DRMHeader_KeyID formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebbf2f548725309717993bf29e48de2bf78ed17
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358690"
---
# <a name="drm_drmheader_keyid"></a>ID. de DRMHeader de DRM \_ \_

El atributo de ID. de clave de **\_ \_ DRMHeader de DRM** contiene el identificador de clave para el archivo.

## <a name="global-constant"></a>Constante global

\_wszWMDRM \_ DRMHeader ID. de cuenta \_

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Este atributo solo está presente con el contenido de la versión 7 de DRM. Se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Para establecer el identificador de clave en el archivo mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , debe usar la propiedad ID. de clave de [**DRM \_**](drm-keyid.md) .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




