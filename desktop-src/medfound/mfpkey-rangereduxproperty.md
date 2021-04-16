---
description: Especifica el grado en el que el códec debe reducir el intervalo de color efectivo del vídeo.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: Propiedad MFPKEY_RANGEREDUX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706210"
---
# <a name="mfpkey_rangeredux-property"></a>\_Propiedad RANGEREDUX de MFPKEY

Especifica el grado en el que el códec debe reducir el intervalo de color efectivo del vídeo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCRangeRedux

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Reducción del intervalo especifica el grado en el que el códec debe reducir el intervalo de luminancia y de croma del vídeo. Al reducir el intervalo se reduce el tamaño de los fotogramas de vídeo codificados, pero también se reduce el detalle de color del vídeo.

La reducción del intervalo consiste en la reducción durante la codificación y la expansión durante la descodificación. Es posible hacer que los factores de expansión sean distintos de los factores de reducción, pero esto no se recomienda en la mayoría de los escenarios en los que resulta útil volver a asignar intervalos.

La reducción y la expansión del rango se realizan por separado en los canales de luminancia y croma. Reducir el intervalo puede ser una manera eficaz de reducir la complejidad del vídeo de baja velocidad de bits sin sacrificar el detalle de la imagen. Al establecer los cuatro valores en 8, se reduce la cantidad de información de luminancia y cromas a la mitad, lo que hace que se dirija más bits para conservar los detalles de la imagen.

El códec puede optar por usar automáticamente la reducción del intervalo al codificar vídeo a velocidades de bits muy bajas. Al establecer los cuatro valores en 0, se deshabilita completamente la reducción del intervalo incluso en escenarios de velocidad de bits bajo.

Al reducir el intervalo de colores se reduce el tamaño codificado de los fotogramas de vídeo, pero se puede introducir un desenfoque en los fotogramas descodificados.

Si no se establece esta propiedad, el códec determina si se va a usar la reducción del intervalo en el tiempo de codificación. Normalmente, el códec selecciona esta opción solo a velocidades de bits bajas.

El valor de esta propiedad es una combinación de cuatro componentes, separados por ceros, con el formato 0x0M0m0N0n, donde:

-   M es el factor de reducción del intervalo de codificación del componente Y.
-   m es el factor de expansión del intervalo de descodificación del componente Y (normalmente igual que M).
-   N es el factor de reducción del intervalo de codificación del componente UV.
-   n es el factor de expansión del intervalo de descodificación del componente UV (lo que suele ser el mismo que N).

Cada factor es un dígito comprendido entre 0 y 8, donde 0 es sin reducción o expansión y 8 es la reducción o expansión máxima.

Si establece el valor en 0x00000000, la reducción del intervalo se deshabilita completamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




