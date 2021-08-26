---
description: Seguimiento de COM+
ms.assetid: ad3bdeb5-f303-411a-abfb-ccde3f9a86b9
title: Seguimiento de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d910f0c559776125342b861e71566fb20f45231f960b1c1dcb18262171926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029495"
---
# <a name="com-tracking"></a>Seguimiento de COM+

El servicio de seguimiento com+ permite crear sus propios programas administrativos y de diagnóstico que realicen un seguimiento del estado y el rendimiento de la ejecución de aplicaciones COM+. El seguimiento de COM+ proporciona información estadística sobre el uso de aplicaciones COM+, así como información de estado, como si una instancia de aplicación de servidor COM+ está en pausa o se ha reciclado. Las herramientas pueden usar información de seguimiento en la supervisión de diagnóstico o con fines de presentación. Por ejemplo, la herramienta administrativa Servicios de componentes usa el seguimiento de COM+ para mostrar el estado de las instancias de aplicación COM+ en las carpetas Aplicaciones COM+ y Procesos en ejecución.

El seguimiento de COM+ calcula y actualiza periódicamente un conjunto de métricas de uso frecuente, lo que hace que esta información esté disponible para los programas que la necesiten. Es similar a la instrumentación de COM+, ya que ambos servicios recopilan automáticamente datos de instancias de aplicación COM+ y hacen que estos datos estén disponibles para los consumidores. Sin embargo, hay algunas diferencias importantes entre estos servicios, tanto en la funcionalidad proporcionada como en el uso típico. En la tabla siguiente se resumen estas diferencias.



| Instrumentación com+                                                                                                                                                                                                   | Seguimiento de COM+                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Datos más completos. El servicio de instrumentación COM+ notifica a los suscriptores registrados los eventos discretos individuales (por ejemplo, el método denominado , objeto destructor) que se producen en una instancia de aplicación COM+.<br/> | Datos agregados. El seguimiento de COM+ calcula y actualiza periódicamente las métricas que se usan con frecuencia para el estado y el rendimiento de las instancias de aplicación COM+.<br/> |
| Normalmente, los suscriptores de eventos calculan las métricas por sí mismos, mediante algoritmos y directivas ad hoc.<br/>                                                                                                           | El servicio de seguimiento de COM+ calcula automáticamente las métricas. Todos los consumidores obtienen los mismos datos, sin compatibilidad con métricas personalizadas.<br/>                |
| Después de registrar una suscripción, el consumidor no recibe información sobre una instancia de aplicación COM+ hasta que se produce un evento.<br/>                                                                    | Los datos de seguimiento de todas las instancias de aplicación COM+ se pueden recuperar en cualquier momento.<br/>                                                                         |
| Solo admite un mecanismo de suscripción basado en eventos COM+ para los consumidores.<br/>                                                                                                                                     | Admite un mecanismo de suscripción basado en eventos COM+ y sondeo en una interfaz de servidor local COM.<br/>                                                  |
| Ejemplos                                                                                                                                                                                                               |                                                                                                                                                                   |
| Notificaciones cuando se llama a un método o se devuelve.<br/>                                                                                                                                                           | Tiempo medio de respuesta de llamada, número de llamadas de método que se han hecho correctamente o con errores en un período de tiempo reciente, número de objetos actualmente en una llamada de método.<br/>     |
| Notificaciones cuando se agrega u obtiene un objeto del grupo de objetos.<br/>                                                                                                                                  | Número de objetos del grupo, número total de objetos.<br/>                                                                                                |
| Notificaciones cuando se inicia, pausa o recicla una aplicación de servidor COM+.<br/>                                                                                                                               | Estado del proceso de aplicación de servidor COM+ (por ejemplo, si está en pausa o reciclada).<br/>                                                         |
| Notificaciones de eventos de inicio, preparación, anulación y confirmación de transacciones.<br/>                                                                                                                                      | No equivalente.<br/>                                                                                                                                         |
| Notificaciones de intentos de autenticación de nivel de llamada de método correctos y con errores.<br/>                                                                                                                           | No equivalente.<br/>                                                                                                                                         |



 

Aunque el seguimiento de COM+ es más limitado en términos de ámbito de datos y flexibilidad para calcular las métricas, las métricas que proporciona deben ser suficientes para una amplia variedad de programas administrativos y de diagnóstico. El uso del seguimiento de COM+, cuando sea posible, puede simplificar el diseño de estos programas. Además, el uso del seguimiento de COM+ en sistemas de producción puede tener un impacto significativamente menor en el rendimiento, lo que hace que sea más adecuado para las herramientas de supervisión en tiempo real.

## <a name="how-com-tracking-collects-data"></a>Cómo recopila datos el seguimiento de COM+

Cuando se inicia un proceso de aplicación de servidor COM+, COM+ registra el proceso con el servidor de seguimiento *,* un componente de la aplicación del sistema. Los componentes de aplicaciones y servicios de biblioteca COM+ sin contextos de componentes (SWC) también admiten el seguimiento. Cuando se crea un componente de biblioteca o contexto SWC en un proceso, COM+ registra el proceso con el servidor de seguimiento si aún no se ha registrado.

COM+ actualiza las estadísticas de un proceso de seguimiento cuando se producen determinados eventos en el proceso, como la creación de un objeto o la finalización de una llamada de método. Los datos actualizados se envían periódicamente al servidor de seguimiento, momento en el que están disponibles para los consumidores. El servidor de seguimiento también es responsable de calcular algunas de las métricas usadas por las características de supervisión de reciclaje y de cuelgue de aplicaciones COM+. Estos datos también están disponibles para los consumidores.

Los datos de seguimiento se organizan según el proceso que generó los datos. Los datos en el nivel de componentes o aplicaciones COM+ individuales del proceso también están disponibles para los consumidores que necesitan esta información.

## <a name="events-versus-polling"></a>Eventos frente a sondeo

El seguimiento de COM+ admite dos mecanismos para que un consumidor obtenga datos de seguimiento del servidor de seguimiento, un mecanismo de suscripción basado en eventos COM+ y una interfaz de servidor local COM.

Los programas que necesitan recibir notificaciones periódicamente con datos de seguimiento actualizados pueden registrar una suscripción para la interfaz de eventos [**IComTrackingInfoEvents.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfoevents) Aproximadamente cada tres segundos, el servidor de seguimiento llama al método [**IComTrackingInfoEvents::OnNewTrackingInfo**](/windows/desktop/api/ComSvcs/nf-comsvcs-icomtrackinginfoevents-onnewtrackinginfo) de cada suscriptor, enviando los datos de seguimiento más recientes en forma de objeto de colección. Este objeto implementa la [**interfaz IComTrackingInfoCollection**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfocollection) y los suscriptores pueden navegar por esta colección para buscar los datos que les interesan.

Por varias razones, podría tener más sentido que un programa sondee los datos del servidor de seguimiento. Por ejemplo, una herramienta de supervisión puede necesitar actualizaciones con mucha menos frecuencia que un programa que muestra el estado en una interfaz de usuario. Además, un programa puede usar solo una pequeña parte de los datos de seguimiento disponibles para el sistema (por ejemplo, una herramienta solo puede supervisar el rendimiento de las instancias de una sola aplicación COM+). El modelo de suscripción envía a cada suscriptor los datos de seguimiento de todas las aplicaciones COM+ en cada notificación y es responsabilidad del suscriptor encontrar los datos que desea. Por último, los eventos COM+ son un mecanismo de notificación de eventos de mejor esfuerzo. No se proporcionan servicios de entrega de mensajes confiables y no hay ninguna manera de que un suscriptor detecte que el servidor de seguimiento no pudo enviarle una notificación.

Un programa que necesita un mayor control sobre su recuperación de datos de seguimiento puede usar la [**interfaz IGetAppTrackerData**](/windows/desktop/api/ComSvcs/nn-comsvcs-igetapptrackerdata) del servidor de seguimiento.

 

 




