---
description: El atributo de velocidad de fotogramas especifica una velocidad de fotogramas por segundo.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: velocidad de fotogramas (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1af5deb8ae2a851b328fcd6d9ffa3923328708
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997828"
---
# <a name="framerate-attribute-directshow"></a>velocidad de fotogramas (DirectShow)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `framerate` atributo especifica una velocidad de fotogramas por segundo.

## <a name="possible-values"></a>Valores posibles

Valor de punto flotante. El valor debe incluir el cero inicial delante de la posición decimal. Por ejemplo, 0,3, no. 3. No use más de siete dígitos decimales.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md), [**Grupo**](group-element.md), [**escala de tiempo**](timeline-element.md)

## <a name="remarks"></a>Observaciones

En el caso del elemento **clip** , este atributo especifica la velocidad de fotogramas predeterminada del origen. Especifique el atributo para las secuencias de andDIB de imágenes fijas. En el caso de una imagen fija, establezca el valor en cero. En el caso de una secuencia DIB, use un valor distinto de cero. El valor predeterminado es cero.

En el caso del elemento **Group** , este atributo especifica la velocidad de fotogramas de salida para el grupo.

En el caso del elemento **Timeline** , este atributo especifica la velocidad de fotogramas predeterminada para todos los grupos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[**IAMTimeline::SetDefaultFPS**](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



