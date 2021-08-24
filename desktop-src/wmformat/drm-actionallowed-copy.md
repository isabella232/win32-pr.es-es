---
title: DRM_ActionAllowed_Copy
description: El atributo ActionAllowed Copy de DRM indica si se permite copiar el contenido en un dispositivo, como \_ \_ un reproductor portátil.
ms.assetid: 3a391a14-ccbb-43c6-b362-0db53d93ab79
keywords:
- DRM_ActionAllowed_Copy windows Media Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_Copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437dba087a336322fe1574112dce0b6b5805d05778613924f577c16343d33604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704786"
---
# <a name="drm_actionallowed_copy"></a>Acción \_ de DRMAllowed \_ Copy

El **atributo \_ ActionAllowed \_ Copy** de DRM indica si se permite copiar el contenido en un dispositivo, como un reproductor portátil.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ ActionAllowed \_ Copy

## <a name="data-type"></a>Tipo de datos

**WMT \_ TYPE \_ BOOL**

## <a name="remarks"></a>Comentarios

En Windows DRM 10 de multimedia, todas las operaciones de copia están restringidas mediante la acción Copiar.

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 




