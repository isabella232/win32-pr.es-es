---
description: Establece el umbral en el que el codificador considera redundante un campo de vídeo.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Propiedad AVEncVideoInverseTelevideoThreshold (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161756"
---
# <a name="avencvideoinversetelecinethreshold-property"></a>AvEncVideoInverseTelevideoThreshold, propiedad

Establece el umbral en el que el codificador considera redundante un campo de vídeo.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoInverseTelevideoThreshold**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad tiene el intervalo siguiente.



| Value | Descripción                                                    |
|-------|----------------------------------------------------------------|
| 0     | Es menos probable que el codificador considere los campos de vídeo redundantes. |
| 100   | Es más probable que el codificador considere los campos de vídeo redundantes. |



 

## <a name="remarks"></a>Observaciones

Establezca esta propiedad si el codificador está realizando teleconferencia inversa con un origen de vídeo análogo.

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

 

 




