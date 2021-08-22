---
description: Acerca del control de velocidad
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Acerca del control de velocidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ae8ad5bcfaaf415c888418a7a6bd5d77f72434150e30fcac071d078b8ee6d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035663"
---
# <a name="about-rate-control"></a>Acerca del control de velocidad

En Media Foundation, la *velocidad de reproducción* se expresa como la proporción de la velocidad de reproducción actual con la velocidad de reproducción normal. Por ejemplo, una velocidad de 2,0 es el doble de la velocidad normal y 0,5 es la velocidad media normal. Los valores negativos indican la reproducción inversa. Una velocidad de reproducción de -2,0 se reproduce hacia atrás a través de la secuencia a una velocidad del doble de la normal. Una velocidad de cero hace que se represente un fotograma; Después de eso, el reloj de presentación no avanza. Para obtener otro fotograma a la velocidad de cero, la aplicación debe buscar una nueva posición.

Las aplicaciones usan las interfaces siguientes para controlar la velocidad de reproducción.

-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). Se usa para averiguar las velocidades de reproducción más rápidas y lentas posibles.
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Se usa para cambiar la velocidad de reproducción.

Para obtener estas dos interfaces, llame [**a IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en la sesión multimedia. El identificador de servicio es MF \_ RATE \_ CONTROL \_ SERVICE.

Mediante el uso del servicio de control de velocidad, una aplicación puede implementar una reproducción de avance rápido e inverso.

## <a name="thinning"></a>Adelgazamiento

*La reducción* es cualquier proceso que reduce el número de muestras de una secuencia para reducir la velocidad de bits general. En el caso del vídeo, la simplificación suele realizarse quitando los fotogramas delta y entregando solo los fotogramas clave. A menudo, la canalización puede admitir velocidades de reproducción más rápidas mediante la reproducción fina, ya que la velocidad de datos es menor porque los fotogramas delta no están descodificados.

La simplificación no cambia las marcas de tiempo ni las duraciones de los ejemplos. Por ejemplo, si la velocidad nominal de la secuencia de vídeo es de 25 fotogramas por segundo, la duración de cada fotograma todavía se marca como 40 milisegundos, incluso si el origen multimedia quita todos los fotogramas delta. Esto significa que habrá un intervalo de tiempo entre el final de un fotograma y el inicio del siguiente.

## <a name="scrubbing"></a>Scrubbing

*La limpieza* es el proceso de buscar instantáneamente puntos específicos en la secuencia mediante la interacción con una barra de desplazamiento, una escala de tiempo u otra representación visual del tiempo. El término proviene de la era de los reproductores de cintas de uno a otro al mecer un rebosante hacia delante y hacia atrás para localizar una sección era como limpiar la cabeza de reproducción con la cinta.

La limpieza se implementa en Media Foundation al establecer la velocidad de reproducción en cero. Para obtener más información, [vea How to Perform Scrubbing](how-to-perform-scrubbing.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de velocidad](rate-control.md)
</dt> <dt>

[Búsqueda, Inserción rápida y reproducción inversa](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[Interfaces de servicio](service-interfaces.md)
</dt> </dl>

 

 



