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
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360960"
---
# <a name="drm_licenseid"></a>Id. de licencia de DRM \_

La **propiedad \_ LicenseID de DRM** contiene una cadena recuperada de la licencia asociada al archivo abierto actualmente que identifica de forma única esa licencia.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ LicenseID

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

Este atributo solo está presente con el contenido de la versión 7 de DRM. Se puede establecer mediante [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

El identificador de licencia se almacena en una licencia, no en un archivo ASF. Cada licencia individual tiene un identificador único asignado por el generador de licencias en el momento de crear la licencia. Por ejemplo, si obtiene dos licencias para el mismo contenido, cada una tendrá un atributo LicenseID diferente. Normalmente, las aplicaciones no necesitan recuperar este valor.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




