---
description: Especifica el número máximo de imágenes de un encabezado de grupo de imágenes (GOP) al siguiente encabezado GOP.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Propiedad AVEncMPVGOPSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080030"
---
# <a name="avencmpvgopsize-property"></a>Propiedad AVEncMPVGOPSize

Especifica el número máximo de imágenes de un encabezado de grupo de imágenes (GOP) al siguiente encabezado GOP.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPVGOPSize**

## <a name="property-value"></a>Valor de propiedad

Los codificadores pueden implementar esta propiedad como un conjunto enumerado o como un intervalo lineal.

## <a name="remarks"></a>Observaciones

Establezca esta propiedad antes de iniciar una grabación.

**Se aplica a Windows 8:** El tamaño de GOP codificado debe ser menor o igual que el número especificado a través de esta propiedad, para mantener el mismo patrón de marco B establecido por [CODECAPI \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) en el GOP o debido al cambio de la escena. Por ejemplo, cuando el número de fotogramas B de un GOP se especifica en 2, y el tamaño del GOP es 11, el codificador producirá un tamaño GOP de 10 fotogramas o menos. Cuando se produce un cambio de escena en medio de un GOP, el codificador también podría insertar el fotograma clave y producir un GOP más pequeño.

El tamaño de GOP 0 es dependiente del codificador y los codificadores pueden elegir diferentes tamaños de GOP en función de su implementación, calidad y rendimiento. Los codificadores deben respetar el tamaño del GOP y truncar los fotogramas B en este caso.

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

 

 




