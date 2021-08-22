---
description: El atributo framerate especifica una velocidad de fotogramas, en fotogramas por segundo.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: atributo framerate (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2939126dbd849538bb30fcf7729e5f91dafa292b6db512398c915c8f8de2c9a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015663"
---
# <a name="framerate-attribute-directshow"></a>atributo framerate (DirectShow)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `framerate` atributo especifica una velocidad de fotogramas, en fotogramas por segundo.

## <a name="possible-values"></a>Valores posibles

Valor de punto flotante. El valor debe incluir el cero inicial antes de la posición decimal. Por ejemplo, 0,3, no .3. No use más de siete dígitos decimales.

## <a name="applies-to"></a>Se aplica a

[**clip**](clip-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md)

## <a name="remarks"></a>Comentarios

Para el **elemento clip,** este atributo especifica la velocidad de fotogramas predeterminada del origen. Especifique el atributo para las imágenes fijas y las secuencias deDIB. Para una imagen fija, establezca el valor en cero. Para una secuencia DIB, use un valor distinto de cero. El valor predeterminado es cero.

Para el **elemento group,** este atributo especifica la velocidad de fotogramas de salida para el grupo.

Para el elemento **timeline,** este atributo especifica la velocidad de fotogramas predeterminada para todos los grupos.

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

 

 



