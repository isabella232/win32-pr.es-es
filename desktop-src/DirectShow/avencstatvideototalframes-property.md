---
description: Devuelve el número de fotogramas de vídeo recibidos por el codificador.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Propiedad AVEncStatVideoTotalFrames (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 461708e9006db183992cf550bf7f98eeaeacbfe16c100675ab4992b54f0768d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663446"
---
# <a name="avencstatvideototalframes-property"></a>Propiedad AVEncStatVideoTotalFrames

Devuelve el número de fotogramas de vídeo recibidos por el codificador.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncStatVideoTotalFrames**

## <a name="remarks"></a>Observaciones

Esta propiedad está disponible una vez completada la codificación.

El valor de esta propiedad es el número total de fotogramas enviados al codificador, incluidos los fotogramas que se han eliminado. Para obtener el número de marcos codificados, lea la [**propiedad AVEncStatVideoCodedFrames.**](avencstatvideocodedframes-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




