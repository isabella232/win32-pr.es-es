---
description: En este tema se describe cómo el origen del secuenciador controla los tiempos de presentación durante la reproducción.
ms.assetid: 0d095e25-5ccf-4319-8767-07b417ed7ee8
title: Tiempos de presentación de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45ea9c8b315171365810f33bb9a66ca4d223fb2119d7aea19288c3ebdd93ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238371"
---
# <a name="sequence-presentation-times"></a>Tiempos de presentación de secuencia

En este tema se describe cómo el [origen del secuenciador](sequencer-source.md) controla los tiempos de presentación durante la reproducción.

## <a name="overview"></a>Información general

El origen del secuenciador admite dos modos diferentes: secuencias de lista de reproducción y secuencias de edición.

En una secuencia de edición, la aplicación especifica la duración de cada segmento de antemano, antes de iniciar la reproducción. En una secuencia de lista de reproducción, la aplicación no especifica la duración de antemano. (De hecho, es posible que no se conozca la duración).

En ambos casos, puede especificar la hora de inicio y de detención de medios de un segmento. Estas horas especifican la posición en el archivo de origen donde comienza y termina el segmento. Por ejemplo, suponga que el archivo de origen tiene una duración de 90 segundos. Si quisiera recortar los primeros 10 segundos y los últimos 10 segundos, especificaría los siguientes valores:

-   Inicio multimedia: 10 segundos
-   Detención de medios: 80 segundos

Para especificar la hora de inicio del medio, establezca el atributo [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) en el nodo de origen. Para especificar la hora de detenerse de los medios, establezca el atributo [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) en el nodo de origen.

Para crear una secuencia de edición, establezca el atributo [MF \_ SESSION GLOBAL \_ \_ TIME](mf-session-global-time-attribute.md) al crear la sesión multimedia. De lo contrario, la sesión multimedia espera secuencias de lista de reproducción. En una secuencia de edición, cada topología de segmento debe tener el atributo [ \_ MF TOPOLOGY \_ PROJECTSTART](mf-topology-projectstart-attribute.md) y el atributo [MF \_ TOPOLOGY \_ PROJECTSTOP.](mf-topology-projectstop-attribute.md)

## <a name="playlist-sequences"></a>Secuencias de lista de reproducción

En una secuencia de lista de reproducción, el reloj de presentación comienza en cero y continúa a través de los límites del segmento. Los orígenes nativos proporcionan ejemplos con marcas de tiempo iguales a la hora del medio. La canalización convierte las marcas de tiempo en el tiempo de presentación correcto como se muestra a continuación:

-   Nueva marca de tiempo = media time + offset - media start

El valor de *offset es* el tiempo de presentación en el que finalizó el segmento anterior. Para el primer segmento, el desplazamiento es cero. Estos son dos ejemplos de cómo se calculan estas conversiones de marca de tiempo:

-   Ejemplo 1: supongamos que el primer segmento (S1) tiene una duración de 10 segundos y el segundo segmento (S2) tiene una hora de inicio multimedia de cero. El origen nativo usa la hora del medio para sus marcas de tiempo, por lo que el primer ejemplo de S2 tiene una marca de tiempo de cero. El desplazamiento es de 10 segundos (la duración de S1), por lo que la marca de tiempo ajustada es:0 + 10 - 0 = 10 segundos.
-   Ejemplo 2: Supongamos que el segmento S1 tiene una longitud de 10 segundos y S2 tiene una hora de inicio multimedia de 5 segundos. El primer ejemplo de S2 tiene una marca de tiempo de 5 segundos (tiempo medio). El desplazamiento es de 10 segundos, por lo que la marca de tiempo ajustada es:5 + 10 - 5 = 10 segundos.

Todos los componentes de canalización de nivel inferior de los nodos de origen reciben ejemplos con las marcas de tiempo ajustadas. Los nodos de origen de una topología pueden tener diferentes horas de inicio multimedia, por lo que los ajustes se calculan por separado para cada rama de la topología.

Cuando la presentación cambia al segmento siguiente, el reloj de presentación no se detiene ni se restablece, y el tiempo de presentación aumenta de forma monótica. Antes de que se inicie un nuevo segmento, la sesión multimedia envía a la aplicación un [evento MESessionNotifyPresentationTime.](mesessionnotifypresentationtime.md) El evento especifica la hora de inicio del segmento, en relación con el reloj de presentación, y el valor del desplazamiento. Cuando se inicia un nuevo segmento, la canalización llama a [**Start en**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) el origen del secuenciador con el valor VT \_ EMPTY. El origen del secuenciador envía un [evento MESourceStarted](mesourcestarted.md) sin hora de inicio.

Para buscar, la aplicación especifica un identificador de segmento más un desplazamiento de tiempo dentro del segmento. Después de la búsqueda, el reloj de presentación comienza en el *desplazamiento del* segmento. Este es un ejemplo de cómo funciona ese proceso:

-   Ejemplo 3: la aplicación busca segmentar S3, con un desplazamiento de segmento de 10 segundos. El reloj de presentación comienza en 10 segundos (desplazamiento del segmento). El desplazamiento no incluye la duración de los segmentos S1 y S2. El origen del secuenciador envía un [evento MESourceStarted](mesourcestarted.md) con una hora de inicio igual al desplazamiento del segmento, 10 segundos.

Después de una búsqueda, si la reproducción continúa hasta el segmento siguiente, la transición funciona igual que en los ejemplos anteriores, salvo que el desplazamiento no incluye los segmentos omitido.

Estos son algunos detalles adicionales que afectan a cómo se marca el tiempo de las muestras:

-   Los descodificadores pueden necesitar datos más allá del tiempo de detenerse los medios. La canalización extrae tantos datos del origen como el descodificador requiere y, a continuación, recorta los ejemplos de salida del descodificador.
-   Las transformaciones pueden almacenar en búfer los datos. Por ejemplo, un efecto de audio podría necesitar hacerlo. Cuando finaliza un segmento, la marca de tiempo de la última muestra de la transformación es anterior al final del segmento, porque la transformación retiene algunos datos. Cuando se inicia el segmento siguiente, la marca de tiempo de la primera muestra es ligeramente anterior al inicio del segmento. No hay ninguna diferencia en las marcas de tiempo, por lo que los datos que llegan al receptor de medios son continuos. Cuando finaliza el segmento final, la canalización purga la transformación, por lo que no se pierde ningún dato.
-   Es posible que el origen deba iniciarse ligeramente antes de la hora de inicio del medio para seleccionar el fotograma clave anterior. Por lo tanto, después del ajuste, el primer ejemplo podría tener un tiempo de presentación negativo.

## <a name="editing-sequences"></a>Editar secuencias

En una secuencia de edición, la aplicación especifica los límites de segmento de antemano estableciendo los atributos [**MF \_ TOPOLOGY \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) y [**MF \_ TOPOLOGY \_ PROJECTSTOP.**](mf-topology-projectstop-attribute.md) La canalización calcula los ajustes de las marcas de tiempo casi de la misma manera que para una secuencia de lista de reproducción:

-   Para el desplazamiento, usa el valor de [**MF \_ TOPOLOGY \_ PROJECTSTART**](mf-topology-projectstart-attribute.md), en lugar de usar el final observado del segmento.

-   Para las búsquedas, el desplazamiento usa un valor igual al valor [**MF \_ TOPOLOGY \_ PROJECTSTART del**](mf-topology-projectstart-attribute.md) segmento más el desplazamiento del segmento.

Por lo tanto, el tiempo de presentación de una secuencia de edición siempre es relativo al inicio de la presentación, incluso si la aplicación busca en otro segmento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión multimedia](media-session.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 



