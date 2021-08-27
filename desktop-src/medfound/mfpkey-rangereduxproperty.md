---
description: Especifica el grado en que el códec debe reducir el intervalo de colores efectivo del vídeo.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: MFPKEY_RANGEREDUX propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3a186522cdc328ab7b6f8e11154ae605673d2cca9d988e0e07c0d159e71589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113315"
---
# <a name="mfpkey_rangeredux-property"></a>Propiedad RANGEREDUX de MFPKEY \_

Especifica el grado en que el códec debe reducir el intervalo de colores efectivo del vídeo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCRangeRedux

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Comentarios

La reducción del intervalo especifica el grado en el que el códec debe reducir el intervalo de luma y de rango del vídeo. La reducción del intervalo reduce el tamaño de los fotogramas de vídeo codificados, pero también reduce los detalles de color del vídeo.

La reducción de intervalos consiste en una reducción durante la codificación y expansión durante la codificación. Es posible diferenciar los factores de expansión de los factores de reducción, pero esto no se recomienda en la mayoría de los escenarios en los que resulta útil la remapping de intervalos.

La reducción y expansión del intervalo se realiza por separado en los canales luma y croma. La reducción del intervalo puede ser una manera eficaz de reducir la complejidad del vídeo de baja velocidad de bits sin sacrificar los detalles de la imagen. Al establecer los cuatro valores en 8, se reduce la cantidad de luma y la información de los colores a la mitad, lo que permite que se dirijan más bits a la conservación de los detalles de la imagen.

El códec puede optar por usar automáticamente la reducción de intervalo al codificar vídeo a velocidades de bits muy bajas. Establecer los cuatro valores en 0 deshabilita completamente la reducción del intervalo incluso en escenarios de velocidad de bits baja.

La reducción del intervalo de colores reduce el tamaño codificado de los fotogramas de vídeo, pero puede introducir desenfoque en los fotogramas descodificados.

Si no se establece esta propiedad, el códec determina si se debe usar la reducción de intervalos en tiempo de codificación. Normalmente, el códec selecciona esta opción solo a velocidades de bits bajas.

El valor de esta propiedad es una combinación de cuatro componentes, separados por ceros, con el formato 0x0M0m0N0n, donde:

-   M es el factor de reducción del intervalo de codificación para el componente Y.
-   m es el factor de expansión del intervalo de decodificación para el componente Y (normalmente igual que M).
-   N es el factor de reducción del intervalo de codificación para el componente UV.
-   n es el factor de expansión del intervalo de descodización para el componente UV (normalmente igual que N).

Cada factor es un dígito de 0 a 8, donde 0 es ninguna reducción o expansión y 8 es la reducción o expansión máxima.

Si establece el valor en 0x00000000, la reducción de intervalos se deshabilita completamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




