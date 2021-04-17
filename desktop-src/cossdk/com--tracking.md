---
description: Seguimiento de COM+
ms.assetid: ad3bdeb5-f303-411a-abfb-ccde3f9a86b9
title: Seguimiento de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 828cc87b5a24363fd814d37c29e61a3ce204d988
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496049"
---
# <a name="com-tracking"></a>Seguimiento de COM+

El servicio de seguimiento de COM+ le permite crear sus propios programas administrativos y de diagnóstico que realizan el seguimiento del estado y el rendimiento de la ejecución de aplicaciones COM+. El seguimiento de COM+ proporciona información estadística sobre el uso de aplicaciones COM+, así como información de estado, por ejemplo, si una instancia de aplicación de servidor COM+ está en pausa o se ha reciclado. Las herramientas pueden usar la información de seguimiento en la supervisión de diagnóstico o para fines de presentación. Por ejemplo, la herramienta administrativa Servicios de componentes utiliza el seguimiento de COM+ para mostrar el estado de las instancias de la aplicación COM+ en las carpetas aplicaciones COM+ y procesos en ejecución.

El seguimiento de COM+ calcula y actualiza periódicamente un conjunto de métricas usadas con frecuencia, lo que hace que esta información esté disponible para los programas que la necesiten. Es similar a la instrumentación de COM+ en que ambos servicios recopilan datos automáticamente de las instancias de la aplicación COM+ y hacen que estos datos estén disponibles para los consumidores. Sin embargo, hay algunas diferencias importantes entre estos servicios, tanto en la funcionalidad proporcionada como en el uso típico. En la tabla siguiente se resumen estas diferencias.



| Instrumentación de COM+                                                                                                                                                                                                   | Seguimiento de COM+                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Datos específicos. El servicio Instrumental de COM+ notifica a los suscriptores registrados de eventos discretos individuales (por ejemplo, método denominado, objeto destruido) que se producen en una instancia de la aplicación COM+.<br/> | Datos agregados. El seguimiento de COM+ calcula y actualiza periódicamente las métricas usadas con frecuencia para el estado y el rendimiento de las instancias de la aplicación COM+.<br/> |
| Normalmente, los suscriptores de eventos calculan las métricas por su cuenta mediante el uso de directivas y algoritmos ad hoc.<br/>                                                                                                           | El servicio de seguimiento de COM+ calcula automáticamente las métricas. Todos los consumidores obtienen los mismos datos, sin compatibilidad con las métricas personalizadas.<br/>                |
| Después de registrar una suscripción, el consumidor no recibe ninguna información sobre una instancia de la aplicación COM+ hasta que se produce un evento.<br/>                                                                    | Los datos de seguimiento de todas las instancias de la aplicación COM+ se pueden recuperar en cualquier momento.<br/>                                                                         |
| Solo admite un mecanismo de suscripción basado en eventos COM+ para los consumidores.<br/>                                                                                                                                     | Admite un mecanismo de suscripción basado en eventos COM+ y el sondeo en una interfaz de servidor local COM.<br/>                                                  |
| Ejemplos                                                                                                                                                                                                               |                                                                                                                                                                   |
| Notificaciones cuando se llama a un método o se devuelve.<br/>                                                                                                                                                           | Tiempo medio de respuesta de la llamada, número de llamadas a métodos que se realizaron correctamente o con errores en un período de tiempo reciente, número de objetos actualmente en una llamada al método.<br/>     |
| Notificaciones cuando se agrega o se obtiene un objeto del grupo de objetos.<br/>                                                                                                                                  | Número de objetos del grupo, número total de objetos.<br/>                                                                                                |
| Notificaciones cuando se inicia, se pausa o recicla una aplicación de servidor COM+.<br/>                                                                                                                               | Estado del proceso de la aplicación de servidor COM+ (por ejemplo, si está pausado o reciclado).<br/>                                                         |
| Notificaciones de eventos de inicio, preparación, anulación y confirmación de transacciones.<br/>                                                                                                                                      | No equivalente.<br/>                                                                                                                                         |
| Notificaciones de intentos de autenticación de nivel de llamada de método correctos y erróneos.<br/>                                                                                                                           | No equivalente.<br/>                                                                                                                                         |



 

Aunque el seguimiento de COM+ es más limitado en términos de ámbito de datos y flexibilidad para calcular métricas, las métricas que proporciona deben ser suficientes para una amplia variedad de programas administrativos y de diagnóstico. Con el seguimiento de COM+, siempre que sea posible, puede simplificar el diseño de estos programas. Además, el seguimiento de COM+ en sistemas de producción puede tener un impacto significativo en el rendimiento, por lo que es más adecuado para las herramientas de supervisión en tiempo real.

## <a name="how-com-tracking-collects-data"></a>Cómo el seguimiento de COM+ recopila datos

Cuando se inicia un proceso de aplicación de servidor COM+, COM+ registra el proceso con el *servidor de seguimiento*, un componente de la aplicación del sistema. Los componentes de las aplicaciones de biblioteca COM+ y los contextos de servicios sin componentes (SWC) también admiten el seguimiento. Cuando se crea un componente de biblioteca o un contexto SWC en un proceso, COM+ registra el proceso con el servidor de seguimiento si aún no se ha registrado.

COM+ actualiza las estadísticas de un proceso sometido a seguimiento cuando se producen determinados eventos en el proceso, como la creación de un objeto o la finalización de una llamada al método. Los datos actualizados se envían periódicamente al servidor de seguimiento, momento en el que pasa a estar disponible para los consumidores. El servidor de Tracker también es responsable de calcular algunas de las métricas usadas por las características de supervisión de bloqueos y reciclaje de aplicaciones COM+. Estos datos también están disponibles para los consumidores.

Los datos de seguimiento se organizan según el proceso que generó los datos. Los datos en el nivel de aplicaciones o componentes COM+ individuales del proceso también están disponibles para los consumidores que necesitan esta información.

## <a name="events-versus-polling"></a>Eventos frente a sondeo

El seguimiento de COM+ admite dos mecanismos para que un consumidor Obtenga datos de seguimiento del servidor de seguimiento, un mecanismo de suscripción basado en eventos COM+ y una interfaz de servidor local COM.

Los programas que se deben notificar periódicamente con datos de seguimiento actualizados pueden registrar una suscripción para la interfaz de eventos [**IComTrackingInfoEvents**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfoevents) . Aproximadamente cada tres segundos, el servidor de seguimiento llama al método [**IComTrackingInfoEvents:: OnNewTrackingInfo**](/windows/desktop/api/ComSvcs/nf-comsvcs-icomtrackinginfoevents-onnewtrackinginfo) de cada suscriptor y envía los datos de seguimiento más recientes en forma de un objeto de colección. Este objeto implementa la interfaz [**IComTrackingInfoCollection**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfocollection) y los suscriptores pueden navegar por esta colección para buscar los datos que le interesan.

Por varias razones, puede que tenga más sentido que un programa sondee los datos del servidor de seguimiento. Por ejemplo, una herramienta de supervisión puede necesitar actualizaciones con mucha menos frecuencia que un programa que muestra el estado en una interfaz de usuario. Además, un programa puede utilizar solo una pequeña parte de los datos de seguimiento disponibles para el sistema (por ejemplo, una herramienta solo puede supervisar el rendimiento de las instancias de una sola aplicación COM+). El modelo de suscripción envía a cada suscriptor los datos de seguimiento de todas las aplicaciones COM+ en cada notificación, y es responsabilidad del suscriptor encontrar los datos que desea. Por último, los eventos COM+ son un mecanismo de notificación de eventos de mejor esfuerzo. No se proporcionan servicios de entrega de mensajes confiables y no hay ninguna manera de que un suscriptor detecte que el servidor de seguimiento no pudo enviarle una notificación.

Un programa que necesite un mayor control sobre su recuperación de datos de seguimiento puede usar la interfaz [**IGetAppTrackerData**](/windows/desktop/api/ComSvcs/nn-comsvcs-igetapptrackerdata) del servidor de seguimiento.

 

 




