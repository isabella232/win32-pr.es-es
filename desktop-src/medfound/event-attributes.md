---
description: Atributos de eventos
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Atributos de evento (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633e8f3857582422fe4a2d65ba34e68be483e7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539550"
---
# <a name="event-attributes-microsoft-media-foundation"></a>Atributos de evento (Microsoft Media Foundation)

Los atributos siguientes se aplican a los eventos.



| Atributo                                                                                                        | Descripción                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**el \_ evento \_ MF \_ simplifica**](mf-event-do-thinning-attribute.md)                                                | Cuando un origen multimedia solicita una nueva velocidad de reproducción, especifica si el origen también solicita el ligero.                |
| [**\_nodo de \_ salida de evento MF \_**](mf-event-output-node-attribute.md)                                                | Identifica el nodo de la topología para un receptor de flujo.                                                                       |
| [**\_desplazamiento de \_ tiempo de presentación de evento MF \_ \_**](mf-event-presentation-time-offset-attribute.md)                     | Desplazamiento entre el tiempo de presentación y las marcas de tiempo del origen del medio.                                              |
| [**\_hora de \_ SCRUBSAMPLE de eventos de MF \_**](mf-event-scrubsample-time-attribute.md)                                      | Tiempo de presentación de un ejemplo que se representó durante la limpieza.                                                     |
| [**\_evento MF \_ SESSIONCAPS**](mf-event-sessioncaps-attribute.md)                                                 | Contiene marcas que definen las funciones de la sesión multimedia, basándose en la presentación actual.                  |
| [**\_SESSIONCAPS de evento MF \_ \_ Delta**](mf-event-sessioncaps-delta-attribute.md)                                    | Contiene marcas que indican qué capacidades han cambiado en la sesión multimedia, en función de la presentación actual. |
| [**\_ \_ Inicio real del origen de eventos MF \_ \_**](mf-event-source-actual-start-attribute.md)                               | Contiene la hora de inicio cuando un origen multimedia se reinicia desde su posición actual.                                       |
| [**\_características del \_ origen de eventos MF \_**](mf-event-source-characteristics-attribute.md)                          | Especifica las características actuales del origen de los medios.                                                            |
| [**\_características de origen de eventos MF \_ \_ \_ anteriores**](mf-event-source-characteristics-old-attribute.md)                 | Especifica las características anteriores del origen multimedia.                                                           |
| [**\_ \_ Inicio falso de origen de evento MF \_ \_**](mf-event-source-fake-start-attribute.md)                                   | Especifica si la topología de segmento actual está vacía.                                                              |
| [**\_origen de evento MF \_ \_ PROJECTSTART**](mf-event-source-projectstart-attribute.md)                                | Especifica la hora de inicio de una topología de segmento.                                                                      |
| [**\_topología de origen de eventos MF \_ \_ \_ cancelada**](mf-event-source-topology-canceled-attribute.md)                     | Especifica si el origen del secuenciador canceló una topología.                                                           |
| [**\_tiempo de \_ presentación de inicio de evento de MF \_ \_**](mf-event-start-presentation-time-attribute.md)                       | La hora de inicio de la presentación, en unidades de 100-nanosegundos, según lo medido por el reloj de la presentación.               |
| [**\_ \_ \_ \_ tiempo de presentación de inicio \_ de evento MF en la \_ salida**](mf-event-start-presentation-time-at-output-attribute.md) | El momento de la presentación en el que los receptores de medios van a representar el primer ejemplo de la nueva topología.                      |
| [**Estado de la \_ topología de eventos MF \_ \_**](mf-event-topology-status-attribute.md)                                        | Especifica el estado de una topología durante la reproducción.                                                                   |
| [**\_tiempo de \_ \_ repetición de \_ evento \_ de sesión MF aprox.**](mf-session-approx-event-occurrence-time-attribute.md)        | La hora aproximada a la que la sesión multimedia generó un evento.                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



