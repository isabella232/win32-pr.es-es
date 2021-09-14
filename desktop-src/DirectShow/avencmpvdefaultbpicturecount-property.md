---
description: Especifica el número predeterminado de fotogramas B consecutivos entre fotogramas I y P.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Propiedad AVEncMPVDefaultBPictureCount (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161856"
---
# <a name="avencmpvdefaultbpicturecount-property"></a>Propiedad AVEncMPVDefaultBPictureCount

Especifica el número predeterminado de fotogramas B consecutivos entre fotogramas I y P.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPVDefaultBPictureCount**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo lineal de valores. Para obtener el intervalo admitido, llame a [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Observaciones

Antes de Windows 8, esta propiedad se aplica a los codificadores de vídeo MPEG. A partir Windows 8, esta propiedad la usan los codificadores de vídeo MPEG, WMV y H.264.

Si el codificador admite esta propiedad, se puede usar para controlar la estructura del grupo de imágenes (GOP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio aplicaciones para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




