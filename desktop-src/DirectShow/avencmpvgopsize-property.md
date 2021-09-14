---
description: Especifica el número máximo de imágenes de un encabezado de grupo de imágenes (GOP) al siguiente encabezado GOP.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Propiedad AVEncMPVGOPSize (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161837"
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

**Se aplica a Windows 8:** El tamaño de GOP codificado debe ser menor o igual que el número especificado a través de esta propiedad, con el fin de mantener el mismo patrón de fotograma B establecido por [CODECAPI \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) en todo el GOP o debido al cambio de escena. Por ejemplo, cuando se especifica que el número de fotogramas B de un GOP es 2 y el tamaño de GOP es 11, el codificador debe generar un tamaño de GOP de 10 fotogramas o menos. Cuando se produce un cambio en la escena en medio de un GOP, el codificador también podría insertar un fotograma clave y producir un GOP más pequeño.

El tamaño 0 de GOP depende del codificador y los codificadores pueden elegir diferentes tamaños de GOP en función de su implementación, calidad y rendimiento. En este caso, los codificadores deben respetar el tamaño de GOP y truncar los fotogramas B.

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

 

 




