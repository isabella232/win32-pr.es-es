---
title: DRM_LicenseID
description: La propiedad LicenseID de DRM contiene una cadena recuperada de la licencia asociada al archivo abierto actualmente que identifica de forma única \_ esa licencia.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID windows Media Format
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9dea32903de18dd1bde8f132b8acf993d3eba2deb0d45c814f0572ce8591ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930955"
---
# <a name="drm_licenseid"></a>Id. de licencia de DRM \_

La **propiedad \_ LicenseID de DRM** contiene una cadena recuperada de la licencia asociada al archivo abierto actualmente que identifica de forma única esa licencia.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ LicenseID

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Este atributo solo está presente con el contenido de la versión 7 de DRM. Se puede establecer mediante [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

El identificador de licencia se almacena en una licencia, no en un archivo ASF. Cada licencia individual tiene un identificador único asignado por el generador de licencias en el momento de crear la licencia. Por ejemplo, si obtiene dos licencias para el mismo contenido, cada una tendrá un atributo LicenseID diferente. Normalmente, las aplicaciones no necesitan recuperar este valor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




