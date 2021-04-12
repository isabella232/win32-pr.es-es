---
title: DRM_LicenseID
description: La \_ propiedad LicenseID de DRM contiene una cadena recuperada de la licencia asociada al archivo abierto que identifica de forma única esa licencia.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358710"
---
# <a name="drm_licenseid"></a>\_LICENSEID DRM

La **propiedad \_ LicenseID de DRM** contiene una cadena recuperada de la licencia asociada al archivo abierto que identifica de forma única esa licencia.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ LicenseID

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Este atributo solo está presente con el contenido de la versión 7 de DRM. Se puede establecer mediante [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y se puede recuperar con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

El identificador de licencia se almacena en una licencia, no en un archivo ASF. Cada licencia individual tiene un identificador único que se asigna mediante el generador de licencias en el momento en que se crea la licencia. Por ejemplo, si obtiene dos licencias para el mismo contenido, cada una tendrá un atributo LicenseID diferente. Normalmente, las aplicaciones no tienen necesidad de recuperar este valor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




