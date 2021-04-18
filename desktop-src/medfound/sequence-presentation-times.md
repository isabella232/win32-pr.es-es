---
description: En este tema se describe cómo el origen del secuenciador controla los tiempos de presentación durante la reproducción.
ms.assetid: 0d095e25-5ccf-4319-8767-07b417ed7ee8
title: Tiempos de presentación de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17f5b0ff4bd6f0cfee2b1b461d6fbd11bdbf0fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543806"
---
# <a name="sequence-presentation-times"></a>Tiempos de presentación de secuencia

En este tema se describe cómo el [origen del secuenciador](sequencer-source.md) controla los tiempos de presentación durante la reproducción.

## <a name="overview"></a>Información general

El origen del secuenciador admite dos modos diferentes: secuencias de lista de reproducción y secuencias de edición.

En una secuencia de edición, la aplicación especifica la duración de cada segmento de antemano antes de comenzar la reproducción. En una secuencia de lista de reproducción, la aplicación no especifica la duración de antemano. (De hecho, es posible que no se conozca la duración).

En ambos casos, puede especificar el tiempo de inicio y detención del medio de un segmento. Estas horas especifican la posición en el archivo de código fuente donde comienza y finaliza el segmento. Por ejemplo, supongamos que el archivo de código fuente tiene una longitud de 90 segundos. Si desea recortar los primeros 10 segundos y los últimos 10 segundos, debe especificar los valores siguientes:

-   Inicio de medio: 10 segundos
-   Detención de medios: 80 segundos

Para especificar la hora de inicio del medio, establezca el atributo [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) en el nodo de origen. Para especificar la hora de detención del medio, establezca el atributo [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) en el nodo de origen.

Para crear una secuencia de edición, establezca el atributo [ \_ \_ \_ hora global de sesión MF](mf-session-global-time-attribute.md) al crear la sesión multimedia. De lo contrario, la sesión multimedia espera secuencias de lista de reproducción. En una secuencia de edición, cada topología de segmento debe tener el atributo [MF \_ Topology \_ PROJECTSTART](mf-topology-projectstart-attribute.md) y el atributo [MF \_ Topology \_ PROJECTSTOP](mf-topology-projectstop-attribute.md) .

## <a name="playlist-sequences"></a>Secuencias de lista de reproducción

En una secuencia de lista de reproducción, el reloj de la presentación comienza en cero y continúa a lo largo de los límites del segmento. Los orígenes nativos proporcionan ejemplos con marcas de tiempo iguales a la hora del medio. La canalización convierte las marcas de tiempo en el tiempo de presentación correcto de la siguiente manera:

-   Nueva marca de tiempo = tiempo medio + desplazamiento − inicio de medios

El valor de *offset* es la hora de presentación en la que finalizó el segmento anterior. En el primer segmento, el desplazamiento es cero. A continuación se muestran dos ejemplos de cómo se calculan estas conversiones de marca de tiempo:

-   Ejemplo 1: Supongamos que el primer segmento (S1) tiene una longitud de 10 segundos y el segundo segmento (S2) tiene una hora de inicio del medio de cero. El origen nativo utiliza la hora del medio para sus marcas de tiempo, por lo que el primer ejemplo de S2 tiene una marca de tiempo de cero. El desplazamiento es de 10 segundos (la duración de S1), por lo que la marca de tiempo ajustada es: 0 + 10 − 0 = 10 segundos.
-   Ejemplo 2: Supongamos que el segmento S1 tiene una longitud de 10 segundos y S2 tiene una hora de inicio del medio de 5 segundos. La primera muestra de S2 tiene una marca de tiempo de 5 segundos (tiempo medio). El desplazamiento es de 10 segundos, por lo que la marca de tiempo ajustada es: 5 + 10 − 5 = 10 segundos.

Todos los componentes de canalización de nivel inferior de los nodos de origen reciben muestras con las marcas de tiempo ajustadas. Los nodos de origen de una topología pueden tener distintas horas de inicio de medios, por lo que los ajustes se calculan por separado para cada rama de la topología.

Cuando la presentación cambia al siguiente segmento, el reloj de la presentación no se detiene ni se restablece, y el tiempo de presentación aumenta de una vez más. Antes de que se inicie un nuevo segmento, la sesión multimedia envía a la aplicación un evento [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) . El evento especifica la hora de inicio del segmento, relativa al reloj de la presentación y el valor del desplazamiento. Cuando se inicia un nuevo segmento, las llamadas de canalización se [**inician**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) en el origen del secuenciador con el valor VT \_ vacío. El origen del secuenciador envía un evento [MESourceStarted](mesourcestarted.md) sin hora de inicio.

Para buscar, la aplicación especifica un identificador de segmento más un desplazamiento de tiempo dentro del segmento. Después de la búsqueda, el reloj de la presentación comienza en el desplazamiento del *segmento* . Este es un ejemplo de cómo funciona este proceso:

-   Ejemplo 3: la aplicación busca el segmento S3, con un desplazamiento de segmento de 10 segundos. El reloj de la presentación comienza en 10 segundos (el desplazamiento del segmento). El desplazamiento no incluye la duración de los segmentos S1 y S2. El origen del secuenciador envía un evento [MESourceStarted](mesourcestarted.md) con una hora de inicio igual al desplazamiento del segmento, 10 segundos.

Después de una búsqueda, si la reproducción continúa en el segmento siguiente, la transición funciona igual que los ejemplos anteriores, salvo que el desplazamiento no incluye los segmentos omitidos.

A continuación se muestran algunos detalles adicionales que afectan al modo en que los ejemplos tienen marca de tiempo:

-   Los descodificadores pueden necesitar datos más allá del tiempo de detención del medio. La canalización extrae todos los datos del origen que el descodificador requiere y, a continuación, recorta los ejemplos de salida del descodificador.
-   Las transformaciones pueden almacenar en búfer los datos. Por ejemplo, un efecto de audio podría necesitar hacerlo. Cuando un segmento finaliza, la marca de tiempo del último ejemplo de la transformación es anterior al final del segmento, porque la transformación retiene algunos datos. Cuando se inicia el siguiente segmento, la marca de tiempo de la primera muestra es ligeramente anterior al inicio del segmento. No hay ninguna brecha en las marcas de tiempo, por lo que los datos que llegan al receptor de medios son continuos. Cuando finaliza el segmento final, la canalización purga la transformación, por lo que no se pierde ningún dato.
-   Es posible que el origen tenga que iniciarse ligeramente anterior a la hora de inicio del medio, para recoger el fotograma clave anterior. Por lo tanto, después del ajuste, el primer ejemplo podría tener un tiempo de presentación negativo.

## <a name="editing-sequences"></a>Editar secuencias

En una secuencia de edición, la aplicación especifica los límites del segmento de antemano mediante el establecimiento de los atributos de la topología [**MF \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) y [**MF \_ \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) . La canalización calcula los ajustes de las marcas de tiempo prácticamente de la misma manera que para una secuencia de lista de reproducción:

-   Para el desplazamiento, usa el valor de [**MF \_ Topology \_ PROJECTSTART**](mf-topology-projectstart-attribute.md), en lugar de usar el extremo observado del segmento.

-   En la búsqueda, el desplazamiento usa un valor igual al valor de [**\_ \_ PROJECTSTART de la topología MF**](mf-topology-projectstart-attribute.md) del segmento más el desplazamiento del segmento.

Por lo tanto, el tiempo de presentación en una secuencia de edición siempre es relativo al inicio de la presentación, incluso si la aplicación busca en otro segmento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión de medios](media-session.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 



