---
description: En esta sección se describe cómo configurar secuencias de VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Usar la codificación VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363646"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a>Usar la codificación VBR (Microsoft Media Foundation)

Como se detalla en el tema [Métodos](encodingmethods.md) de codificación, la codificación de velocidad de bits variable (VBR) se usa para mejorar la coherencia de la calidad del contenido. Las secuencias de VBR se configuran de la misma manera que se codifican secuencias de velocidad de bits constante (CBR), excepto para los parámetros de búfer (velocidad de bits y ventana de búfer). En esta sección se describe cómo configurar secuencias de VBR.

## <a name="configuring-quality-based-vbr"></a>Configuración de VBR basado en calidad

La codificación mediante el método VBR basado en calidad no requiere ningún parámetro de búfer predefinido. En su lugar, especifique un nivel de calidad (de 0 a 100) que el codificador usa para determinar dinámicamente los parámetros de búfer adecuados. Este modo de codificación solo usa un paso de codificación.

Puede enumerar los tipos de salida de VBR basados en calidad admitidos para los códecs de audio. Debe usar uno de los tipos devueltos por el DMO al establecer el tipo de salida. Para obtener más información, vea [Enumerar tipos de audio para modos de codificación específicos.](enumeratingaudiotypesforspecificencodingmodes.md)

Para configurar una secuencia de vídeo de VBR basada en la calidad, debe establecer las propiedades que se enumeran en la tabla siguiente.



| Propiedad.                                            | Descripción                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Establezca en VARIANT \_ TRUE.                                                                                                                                   |
| [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md) | Establezca en el valor de calidad deseado, de 0 a 100. No todos los valores de calidad representan configuraciones discretas. Consulte la descripción de la propiedad para obtener más información. |



 

## <a name="configuring-unconstrained-vbr"></a>Configuración de VBR sin restricciones

La codificación VBR sin restricciones permite al codificador variar el tamaño de las muestras individuales sin límites de búfer explícitos. Sin embargo, la velocidad de bits media durante la duración del contenido resultante debe ser menor o igual que el valor especificado. VBR sin restricciones requiere dos pases de codificación.

Puede enumerar los tipos de salida de VBR de dos pases admitidos para los códecs de audio. Debe usar uno de los tipos devueltos por el DMO al establecer el tipo de salida. Para obtener más información, vea [Enumerar tipos de audio para modos de codificación específicos.](enumeratingaudiotypesforspecificencodingmodes.md)

Para configurar una secuencia de vídeo de VBR sin restricciones, debe establecer las propiedades que se enumeran en la tabla siguiente.



| Propiedad.                                            | Descripción                          |
|-----------------------------------------------------|--------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Establezca en VARIANT \_ TRUE.                |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Establezca en 2.                            |
| [MFPKEY \_ ESTOG](mfpkey-ravgproperty.md)             | Establezca en la velocidad de bits media deseada. |



 

## <a name="configuring-peak-constrained-vbr"></a>Configuración de Peak-Constrained VBR

VBR con restricciones máximas es como VBR sin restricciones, ya que se limita a una velocidad de bits media durante la duración de la secuencia. Además, VBR con restricción máxima se ajusta a un búfer máximo. Este búfer se describe mediante una velocidad de bits máxima y una ventana de búfer máxima, igual que un búfer CBR se describe mediante una velocidad de bits media y una ventana de búfer. Este modo proporciona al codificador flexibilidad en la forma en que codifica muestras individuales a la vez que se cumplen las limitaciones máximas. Esto es especialmente útil cuando la descodización se realiza mediante un chip en un dispositivo, como un reproductor de DVD, donde hay limitaciones de hardware que deben tenerse en cuenta.

Los tipos de salida del codificador de audio VBR con restricciones máximas admitidas son los mismos tipos enumerados para VBR sin restricciones. Establezca los valores máximos en el DMO y use el tipo entregado. Para obtener más información, vea [Enumerar tipos de audio para modos de codificación específicos.](enumeratingaudiotypesforspecificencodingmodes.md)

Para configurar una secuencia de vídeo de VBR con restricciones máximas, debe establecer las propiedades que se enumeran en la tabla siguiente mediante el **método IPropertyBag::Write.**



| Propiedad.                                            | Descripción                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Establezca en VARIANT \_ TRUE.                                           |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Establezca en 2.                                                       |
| [MFPKEY \_ ESTOG](mfpkey-ravgproperty.md)             | Establezca en la velocidad de bits media deseada.                            |
| [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)             | Establezca en la velocidad de bits máxima deseada.                               |
| [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)             | Se establece en la ventana de búfer que corresponde a la velocidad de bits máxima. |



 

> [!Note]  
> Se recomienda establecer la velocidad de bits máxima en al menos el doble de la velocidad de bits media. Si se establece la velocidad máxima en un valor inferior, el códec puede codificar el contenido como CBR de dos pases en lugar de VBR con restricciones máximas.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> <dt>

[Uso de Two-Pass codificación](usingtwoencodingpasses.md)
</dt> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 



