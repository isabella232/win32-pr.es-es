---
description: Describe las estadísticas que se pueden recuperar de un códec de Windows Media.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Obtener estadísticas de codificación (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808065"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a>Obtener estadísticas de codificación (Microsoft Media Foundation)

La información sobre lo que ocurre en una sesión de codificación suele estar disponible de forma inmediata en forma de códigos de error devueltos al procesar las muestras. Sin embargo, hay algunas estadísticas que puede recuperar del códec sobre diversos aspectos de codificación.

## <a name="video-frame-information"></a>Información del fotograma de vídeo

Algunas estadísticas de vídeo que puede recuperar se ocupan del número de fotogramas procesados por el codificador. Hay tres propiedades de número de fotogramas que se pueden leer desde el codificador de vídeo:

-   [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) es el número de fotogramas procesados a través del flujo de entrada de DMO.
-   [MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md) es el número de Marcos codificados. Al restar este valor del número total de fotogramas pasados, se puede determinar el número de fotogramas que se han quitado.
-   [MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) es el número de fotogramas no codificados porque ya están incluidos en el contenido duplicado. Este valor no se resta del número de fotogramas codificados comunicados por DMO.

Puede leer las propiedades de los fotogramas de vídeo en cualquier momento durante la codificación. Esto puede ser útil para determinar si la configuración de codificación es adecuada para el contenido; Si hay una diferencia importante entre los marcos totales y los marcos codificados, el contenido comprimido podría no satisfacer sus requisitos de calidad. Puede leer los valores finales después de finalizar la codificación.

## <a name="vbr-buffer-statistics"></a>Estadísticas de búfer de VBR

Dependiendo del modo de codificación utilizado, algunos o todos los valores de configuración del búfer se pueden determinar durante la codificación (por ejemplo, la velocidad de bits de VBR basada en calidad no se conoce hasta que se codifica el contenido). Hay cuatro propiedades de búfer VBR que puede obtener mediante el método **IPropertyBag:: Read** :

-   [MFPKEY \_ RAVG](mfpkey-ravgproperty.md) es la velocidad de bits promedio del contenido de VBR.
-   [MFPKEY \_ BAVG](mfpkey-bavgproperty.md) es la ventana de búfer para la velocidad de bits media.
-   [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) es la velocidad de bits máxima del contenido de VBR.
-   [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) es la ventana de búfer máximo.

Después de comenzar a procesar ejemplos, no debe leer ninguna de las propiedades de VBR hasta que termine de codificar la secuencia. Si lo hace, el codificador interpreta la solicitud como una señal de que la codificación está completa. El siguiente ejemplo que se procesa se trata como una nueva sesión de codificación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



