---
description: Devuelve el promedio de bits por segundo del audio codificado.
ms.assetid: c90c9247-825f-4602-bb16-809969703a98
title: Propiedad AVEncStatAudioAverageBPS (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76bcf1ca7b3ee74ae406ebd71f85988a4d13313
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161812"
---
# <a name="avencstataudioaveragebps-property"></a>Propiedad AVEncStatAudioAverageBPS

Devuelve el promedio de bits por segundo del audio codificado.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncStatAudioAverageBPS**

## <a name="remarks"></a>Observaciones

Esta propiedad está disponible una vez completada la codificación.

Esta propiedad solo se aplica a la codificación de velocidad de bits variable basada en calidad (VBR).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| aplicaciones para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP de 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




