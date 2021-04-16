---
description: Devuelve el número de fotogramas de vídeo que el codificador ha recibido.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Propiedad AVEncStatVideoTotalFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659267"
---
# <a name="avencstatvideototalframes-property"></a>Propiedad AVEncStatVideoTotalFrames

Devuelve el número de fotogramas de vídeo que el codificador ha recibido.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncStatVideoTotalFrames**

## <a name="remarks"></a>Observaciones

Esta propiedad está disponible una vez completada la codificación.

El valor de esta propiedad es el número total de fotogramas enviados al codificador, incluidos los fotogramas que se quitaron. Para obtener el número de Marcos codificados, lea la propiedad [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




