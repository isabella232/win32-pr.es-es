---
description: En esta sección se describe cómo configurar secuencias VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Usar la codificación VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275808"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a>Usar la codificación VBR (Microsoft Media Foundation)

Tal y como se detalla en el tema [métodos de codificación](encodingmethods.md) , se usa la codificación de velocidad de bits variable (VBR) para mejorar la coherencia de la calidad del contenido. Los flujos VBR se configuran de la misma manera que se codifican secuencias de velocidad de bits constante (CBR), excepto los parámetros de búfer (velocidad de bits y ventana de búfer). En esta sección se describe cómo configurar secuencias VBR.

## <a name="configuring-quality-based-vbr"></a>Configuración de VBR basada en la calidad

La codificación con el método VBR basado en la calidad no requiere ningún parámetro de búfer predefinido. En su lugar, especifique un nivel de calidad (de 0 a 100) que el codificador usa para determinar dinámicamente los parámetros de búfer adecuados. Este modo de codificación solo usa un paso de codificación.

Puede enumerar los tipos de salida VBR basados en la calidad admitidos para los códecs de audio. Debe usar uno de los tipos devueltos por DMO al establecer el tipo de salida. Para obtener más información, consulte [enumeración de tipos de audio para modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md).

Para configurar una secuencia de vídeo VBR basada en la calidad, debe establecer las propiedades que se enumeran en la tabla siguiente.



| Propiedad                                            | Descripción                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Establézcalo en VARIANT \_ true.                                                                                                                                   |
| [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md) | Establezca en el valor de calidad deseado, de 0 a 100. No todos los valores de calidad representan valores discretos. Vea la descripción de la propiedad para obtener más información. |



 

## <a name="configuring-unconstrained-vbr"></a>Configuración de VBR sin restricciones

La codificación VBR no restringida permite que el codificador varíe el tamaño de los ejemplos individuales sin ningún límite explícito de búfer. Sin embargo, la velocidad de bits promedio a lo largo de la duración del contenido resultante debe ser menor o igual que el valor especificado. La VBR sin restricciones requiere dos pasos de codificación.

Puede enumerar los tipos de salida VBR de dos pasos compatibles para los códecs de audio. Debe usar uno de los tipos devueltos por DMO al establecer el tipo de salida. Para obtener más información, consulte [enumeración de tipos de audio para modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md).

Para configurar una secuencia de vídeo VBR sin restricciones, debe establecer las propiedades que se enumeran en la tabla siguiente.



| Propiedad                                            | Descripción                          |
|-----------------------------------------------------|--------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Establézcalo en VARIANT \_ true.                |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Establezca en 2.                            |
| [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)             | Establezca en la velocidad de bits promedio deseada. |



 

## <a name="configuring-peak-constrained-vbr"></a>Configuración de Peak-Constrained VBR

La VBR máxima restringida es como VBR no restringida, ya que se limita a una velocidad de bits promedio a lo largo de la secuencia. Además, la VBR máxima restringida se ajusta a un búfer máximo. Este búfer se describe con una velocidad de bits máxima y una ventana de búfer máximo, al igual que un búfer CBR se describe mediante una velocidad de bits promedio y una ventana de búfer. Este modo proporciona la flexibilidad del codificador en cómo codifica los ejemplos individuales mientras se respetan las limitaciones máximas. Esto es especialmente útil cuando se realiza la descodificación en un chip de un dispositivo, como un reproductor de DVD, donde se deben tener en cuenta limitaciones de hardware.

Los tipos de salida del codificador de audio VBR, restringido y máximo admitidos son los mismos tipos enumerados para VBR no restringida. Establezca los valores máximos en DMO y use el tipo entregado. Para obtener más información, consulte [enumeración de tipos de audio para modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md).

Para configurar una secuencia de vídeo VBR máxima restringida, debe establecer las propiedades que se enumeran en la siguiente tabla mediante el método **IPropertyBag:: Write** .



| Propiedad                                            | Descripción                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Establézcalo en VARIANT \_ true.                                           |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Establezca en 2.                                                       |
| [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)             | Establezca en la velocidad de bits promedio deseada.                            |
| [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)             | Establezca en la velocidad de bits máxima deseada.                               |
| [MFPKEY \_ Bmax](mfpkey-bmaxproperty.md)             | Se establece en la ventana de búfer que corresponde a la velocidad de bits máxima. |



 

> [!Note]  
> Se recomienda establecer la velocidad de bits máxima en al menos dos veces la velocidad de bits promedio. La configuración de la velocidad máxima en un valor inferior puede hacer que el códec codifique el contenido como CBR de dos pasadas en lugar de VBR máxima restringida.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> <dt>

[Uso de la codificación de Two-Pass](usingtwoencodingpasses.md)
</dt> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 



