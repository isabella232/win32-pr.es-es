---
title: Use_Advanced_DRM
description: El atributo Usar DRM avanzado especifica si la versión 7 de \_ DRM se usa para proteger el \_ contenido.
ms.assetid: a385152f-d72e-473c-93a0-5697659df23c
keywords:
- Use_Advanced_DRM windows Media Format
topic_type:
- apiref
api_name:
- Use_Advanced_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a11731fbe212c8b87cd52300da1885206230c7329491a6512ab3c261923c74e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658225"
---
# <a name="use_advanced_drm"></a>Uso \_ de \_ DRM avanzado

El **atributo \_ Usar \_ DRM** avanzado especifica si la versión 7 de DRM se usa para proteger el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMUse \_ Advanced \_ DRM

## <a name="data-type"></a>Tipo de datos

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Comentarios

Se trata de una propiedad de lectura y escritura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) y se establece mediante [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). Esta propiedad no es accesible desde el objeto de lector.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




