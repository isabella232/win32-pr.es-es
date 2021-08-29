---
title: DRM_DRMHeader_KeyID
description: El atributo \_ DRMHeader KeyID de DRM contiene el identificador de clave del \_ archivo.
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- DRM_DRMHeader_KeyID windows Media Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11d940c9ea76095983542aab380b9abd82c7b037bf0180f532e6f540438a305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931165"
---
# <a name="drm_drmheader_keyid"></a>DRM \_ DRMHeader \_ KeyID

El **atributo \_ DRMHeader \_ KeyID de DRM** contiene el identificador de clave del archivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ KeyID

## <a name="data-type"></a>Tipo de datos

**CADENA DE TIPO WMT \_ \_**

## <a name="remarks"></a>Comentarios

Este atributo solo está presente con contenido drm versión 7. Se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Para establecer el identificador de clave en el archivo [**mediante IWMDRMWriter::SetDRMAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) debe usar la [**propiedad \_ KeyID de DRM.**](drm-keyid.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




