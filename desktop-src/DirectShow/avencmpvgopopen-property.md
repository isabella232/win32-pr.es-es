---
description: Especifica si el codificador genera grupos abiertos de imágenes (GOP) o GOP cerrados. Esta propiedad se aplica a los codificadores de vídeo MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Propiedad AVEncMPVGOPOpen (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806344"
---
# <a name="avencmpvgopopen-property"></a>Propiedad AVEncMPVGOPOpen

Especifica si el codificador genera grupos abiertos de imágenes (GOP) o GOP cerrados. Esta propiedad se aplica a los codificadores de vídeo MPEG.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPVGOPOpen**

## <a name="property-value"></a>Valor de propiedad



| Value          | Descripción |
|----------------|-------------|
| VARIANTE \_ false | GOP cerrado |
| VARIANTE \_ true  | Abrir GOP   |



 

## <a name="remarks"></a>Observaciones

Un GOP abierto contiene fotogramas Delta que hacen referencia a fotogramas del GOP anterior. Un GOP cerrado no contiene ningún fotograma Delta que haga referencia al GOP anterior.

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

 

 




