---
description: Especifica el valor de la marca de marco desplegable en el encabezado de grupo de imágenes (GOP).
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Propiedad AVEncVideoHeaderDropFrame (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161779"
---
# <a name="avencvideoheaderdropframe-property"></a>AvEncVideoHeaderDropFrame, propiedad

Especifica el valor de la marca de marco desplegable en el encabezado de grupo de imágenes (GOP).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoHeaderDropFrame**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad puede ser 0 o 1.

## <a name="remarks"></a>Observaciones

El modo de colocación de fotogramas se usa en el vídeo de TIME para corregir la discrepancia entre el vídeo, que es de 29,97 fotogramas por segundo, y la visualización del código de tiempo, que es de 30 fotogramas por segundo. En el modo de fotograma desplegable, los números de fotograma 00 y 01 se omiten al principio de cada minuto, excepto en los minutos que son incluso múltiplo de diez (00, 10, 20, etc.). Solo se descartan los números de fotograma del código de tiempo; no se descarta ningún fotograma real.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




