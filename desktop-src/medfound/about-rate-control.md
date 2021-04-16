---
description: Acerca del control tasa
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Acerca del control tasa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705564"
---
# <a name="about-rate-control"></a>Acerca del control tasa

En Media Foundation, la *velocidad* de reproducción se expresa como la relación entre la velocidad de reproducción actual y la velocidad de reproducción normal. Por ejemplo, una velocidad de 2,0 es dos veces la velocidad normal y 0,5 es la velocidad media normal. Los valores negativos indican la reproducción inversa. Una velocidad de reproducción de-2,0 se reproduce hacia atrás a lo largo de la secuencia dos veces la velocidad normal. Una tasa de cero hace que se represente un fotograma; después, el reloj de la presentación no avanza. Para obtener otro fotograma a la velocidad de cero, la aplicación debe buscar en una nueva posición.

Las aplicaciones usan las siguientes interfaces para controlar la velocidad de reproducción.

-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). Se usa para averiguar las velocidades de reproducción más rápidas y lentas posibles.
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Se usa para cambiar la velocidad de reproducción.

Para obtener estas dos interfaces, llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en la sesión multimedia. El identificador del servicio es MF \_ rate \_ control \_ Service.

Con el servicio de control de tarifas, una aplicación puede implementar una reproducción rápida y directa.

## <a name="thinning"></a>Simplificación

El *ligero* es cualquier proceso que reduzca el número de muestras de un flujo para reducir la velocidad de bits general. En el caso de los vídeos, la reducción de los fotogramas Delta y la entrega solo de los fotogramas clave se logra con el ligero. A menudo, la canalización puede admitir velocidades de reproducción más rápidas mediante la reproducción reducida, ya que la velocidad de datos es menor porque las tramas Delta no se descodifican.

El ligero no cambia las marcas de tiempo ni las duraciones de los ejemplos. Por ejemplo, si la tasa nominal de la secuencia de vídeo es de 25 fotogramas por segundo, la duración de cada fotograma se mantiene marcada como 40 milisegundos, incluso si el origen de medios está quitando todos los fotogramas Delta. Esto significa que habrá un intervalo de tiempo entre el final de un fotograma y el inicio de la siguiente.

## <a name="scrubbing"></a>Scrubbing

La *limpieza* es el proceso de búsqueda instantánea de puntos específicos en el flujo interactuando con una barra de desplazamiento, una escala de tiempo u otra representación visual del tiempo. El término proviene de la era de los reproductores de cintas carretes cuando se produce un carrete hacia atrás y hacia delante para buscar una sección, como la limpieza del cabezal de reproducción con la cinta.

La limpieza se implementa en Media Foundation estableciendo la velocidad de reproducción en cero. Para obtener más información, vea [Cómo realizar la limpieza](how-to-perform-scrubbing.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de tasa](rate-control.md)
</dt> <dt>

[Búsqueda, avance rápido y reproducción inversa](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[Interfaces de servicio](service-interfaces.md)
</dt> </dl>

 

 



