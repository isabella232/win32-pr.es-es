---
description: Especifica si el codificador genera grupos abiertos de imágenes (GOP) o GOP cerrados. Esta propiedad se aplica a los codificadores de vídeo MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Propiedad AVEncMPVGOPOpen (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6be085bde5588fecd5a2274d442f38d4198702475f3ed13c7bb3a5569687375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540905"
---
# <a name="avencmpvgopopen-property"></a>AVEncMPVGOPOpen, propiedad

Especifica si el codificador genera grupos abiertos de imágenes (GOP) o GOP cerrados. Esta propiedad se aplica a los codificadores de vídeo MPEG.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPVGOPAbrir**

## <a name="property-value"></a>Valor de propiedad



| Valor          | Descripción |
|----------------|-------------|
| VARIANT \_ FALSE | GOP cerrados |
| VARIANT \_ TRUE  | Abrir GOP   |



 

## <a name="remarks"></a>Comentarios

Un GOP abierto contiene marcos delta que hacen referencia a fotogramas del GOP anterior. Un GOP cerrado no contiene ningún marco delta que haga referencia al GOP anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




