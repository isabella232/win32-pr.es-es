---
description: Especifica el valor de la marca de fotogramas en el encabezado grupo de imágenes (GOP).
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Propiedad AVEncVideoHeaderDropFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906827"
---
# <a name="avencvideoheaderdropframe-property"></a>Propiedad AVEncVideoHeaderDropFrame

Especifica el valor de la marca de fotogramas en el encabezado grupo de imágenes (GOP).

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoHeaderDropFrame**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad puede ser 0 o 1.

## <a name="remarks"></a>Observaciones

El modo de marco de colocación se usa en vídeo NTSC para corregir la discrepancia entre el vídeo, que es 29,97 fotogramas por segundo, y la presentación del código de tiempo, que es 30 fotogramas por segundo. En el modo de marco de colocación, los números de fotogramas 00 y 01 se omiten al principio de cada minuto, excepto en los minutos que son incluso múltiplos de diez (00, 10, 20, etc.). Solo se quitan los números de fotogramas del código de tiempo; no se quita ningún fotograma real.

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

 

 




