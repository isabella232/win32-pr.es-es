---
description: Describe las estadísticas que se pueden recuperar de un códec Windows media.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Obtener estadísticas de codificación (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474272"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a>Obtener estadísticas de codificación (Microsoft Media Foundation)

Por lo general, la información sobre lo que sucede en una sesión de codificación está disponible inmediatamente en forma de códigos de error devueltos al procesar muestras. Sin embargo, hay algunas estadísticas que puede recuperar del códec sobre varios aspectos de codificación.

## <a name="video-frame-information"></a>Información de fotogramas de vídeo

Algunas estadísticas de vídeo que puede recuperar se tratan con el número de fotogramas procesados por el codificador. Hay tres propiedades de número de fotograma que puede leer desde el codificador de vídeo:

-   [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) es el número de fotogramas procesados a través del flujo de entrada de la DMO.
-   [MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md) es el número de fotogramas codificados. Al restar este valor del número total de fotogramas pasados, puede determinar cuántos fotogramas se quitaron.
-   [MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) es el número de fotogramas no codificados porque ya incluye contenido duplicado. Este valor no se resta del número de fotogramas codificados notificados por el DMO.

Puede leer las propiedades del fotograma de vídeo en cualquier momento durante la codificación. Esto puede ser útil para determinar si la configuración de codificación es adecuada para el contenido; Si hay una gran diferencia entre el total de fotogramas y los fotogramas codificados, es posible que el contenido comprimido no cumpla los requisitos de calidad. Puede leer los valores finales después de finalizar la codificación.

## <a name="vbr-buffer-statistics"></a>Estadísticas de búfer de VBR

Según el modo de codificación utilizado, se pueden determinar algunas o todas las configuraciones de búfer durante la codificación (por ejemplo, la velocidad de bits de VBR basada en calidad no se conoce hasta que se codifica el contenido). Hay cuatro propiedades de búfer de VBR que puede obtener mediante el **método IPropertyBag::Read:**

-   [MFPKEY \_ VBG](mfpkey-ravgproperty.md) es la velocidad de bits media del contenido de VBR.
-   [MFPKEY \_ BAVG es](mfpkey-bavgproperty.md) la ventana de búfer para la velocidad de bits media.
-   [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) es la velocidad de bits máxima del contenido de VBR.
-   [MFPKEY \_ BMAX es](mfpkey-bmaxproperty.md) la ventana de búfer máximo.

Después de comenzar a procesar ejemplos, no debe leer ninguna de las propiedades de VBR hasta que haya terminado de codificar la secuencia. Si lo hace, el codificador interpreta la solicitud como una señal de que la codificación está completa. El ejemplo siguiente que se procesa se trata como una nueva sesión de codificación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



