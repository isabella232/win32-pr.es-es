---
description: Atributos de eventos
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Atributos de evento (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36d64efbc4ed36569ef85514d38563fe09a01902218833b029455c48e2c6e3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600515"
---
# <a name="event-attributes-microsoft-media-foundation"></a>Atributos de evento (Microsoft Media Foundation)

Los atributos siguientes se aplican a los eventos.



| Atributo                                                                                                        | Descripción                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**MF \_ EVENT \_ \_ DONNING**](mf-event-do-thinning-attribute.md)                                                | Cuando un origen multimedia solicita una nueva velocidad de reproducción, especifica si el origen también solicita la simplificación.                |
| [**NODO DE \_ SALIDA \_ DE EVENTOS MF \_**](mf-event-output-node-attribute.md)                                                | Identifica el nodo de topología para un receptor de flujo.                                                                       |
| [**DESPLAZAMIENTO \_ DE TIEMPO DE PRESENTACIÓN DE EVENTOS \_ \_ \_ MF**](mf-event-presentation-time-offset-attribute.md)                     | Desplazamiento entre el tiempo de presentación y las marcas de tiempo del origen multimedia.                                              |
| [**MF \_ EVENT \_ SCRUBSAMPLE \_ TIME**](mf-event-scrubsample-time-attribute.md)                                      | Tiempo de presentación de una muestra que se representó durante la limpieza.                                                     |
| [**MF \_ EVENT \_ SESSIONCAPS**](mf-event-sessioncaps-attribute.md)                                                 | Contiene marcas que definen las funciones de la sesión multimedia, en función de la presentación actual.                  |
| [**MF \_ EVENT \_ SESSIONCAPS \_ DELTA**](mf-event-sessioncaps-delta-attribute.md)                                    | Contiene marcas que indican qué funcionalidades han cambiado en la sesión multimedia, en función de la presentación actual. |
| [**INICIO \_ REAL DEL ORIGEN DEL EVENTO \_ \_ \_ MF**](mf-event-source-actual-start-attribute.md)                               | Contiene la hora de inicio en la que un origen multimedia se reinicia desde su posición actual.                                       |
| [**CARACTERÍSTICAS DE \_ ORIGEN \_ DE EVENTOS MF \_**](mf-event-source-characteristics-attribute.md)                          | Especifica las características actuales del origen de medios.                                                            |
| [**CARACTERÍSTICAS ANTIGUAS \_ DEL ORIGEN DE EVENTOS \_ \_ \_ MF**](mf-event-source-characteristics-old-attribute.md)                 | Especifica las características anteriores del origen de medios.                                                           |
| [**MF \_ EVENT \_ SOURCE \_ FAKE \_ START**](mf-event-source-fake-start-attribute.md)                                   | Especifica si la topología del segmento actual está vacía.                                                              |
| [**MF \_ EVENT \_ SOURCE \_ PROJECTSTART**](mf-event-source-projectstart-attribute.md)                                | Especifica la hora de inicio de una topología de segmento.                                                                      |
| [**TOPOLOGÍA \_ DE ORIGEN DE EVENTOS MF \_ \_ \_ CANCELADA**](mf-event-source-topology-canceled-attribute.md)                     | Especifica si el origen del secuenciador canceló una topología.                                                           |
| [**HORA DE \_ PRESENTACIÓN DEL \_ EVENTO \_ MF \_**](mf-event-start-presentation-time-attribute.md)                       | Hora de inicio de la presentación, en unidades de 100 nanosegundos, medida por el reloj de presentación.               |
| [**HORA DE PRESENTACIÓN DEL EVENTO MF \_ \_ EN LA \_ \_ \_ \_ SALIDA**](mf-event-start-presentation-time-at-output-attribute.md) | Hora de presentación en la que los receptores multimedia representarán el primer ejemplo de la nueva topología.                      |
| [**ESTADO \_ DE LA TOPOLOGÍA DE EVENTOS \_ \_ MF**](mf-event-topology-status-attribute.md)                                        | Especifica el estado de una topología durante la reproducción.                                                                   |
| [**HORA DE \_ REPETICIÓN DE EVENTOS DE MF SESSION \_ APPROX \_ \_ \_**](mf-session-approx-event-occurrence-time-attribute.md)        | Hora aproximada a la que la sesión multimedia ha producido un evento.                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 



