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
ms.openlocfilehash: 3ebbf2f548725309717993bf29e48de2bf78ed17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572213"
---
# <a name="drm_drmheader_keyid"></a>DRM \_ DRMHeader \_ KeyID

El **atributo \_ DRMHeader \_ KeyID de DRM** contiene el identificador de clave del archivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ KeyID

## <a name="data-type"></a>Tipo de datos

**CADENA DE TIPO WMT \_ \_**

## <a name="remarks"></a>Observaciones

Este atributo solo está presente con contenido drm versión 7. Se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Para establecer el identificador de clave en el archivo [**mediante IWMDRMWriter::SetDRMAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) debe usar la [**propiedad \_ KeyID de DRM.**](drm-keyid.md)

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




