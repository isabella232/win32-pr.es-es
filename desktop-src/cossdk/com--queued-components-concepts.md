---
description: Conceptos de componentes en cola de COM+
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: Conceptos de componentes en cola de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705277"
---
# <a name="com-queued-components-concepts"></a>Conceptos de componentes en cola de COM+

En función de los servicios de [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) , el servicio de componentes en cola de com+ proporciona una manera sencilla de invocar y ejecutar componentes de forma asincrónica. El procesamiento se puede realizar sin tener en cuenta la disponibilidad o la accesibilidad del remitente o del receptor.

En términos COM, una *cola* es un área de almacenamiento que guarda los mensajes para su posterior recuperación. Queue Server proporciona un mecanismo para la comunicación sin conexión. Es decir, el remitente y el receptor no se conectan directamente y solo se comunican a través de las colas. Queue Server proporciona una manera de conservar la información hasta que el receptor esté listo para obtenerla. El remitente y el receptor se comunican indirectamente para que cada uno de ellos pueda funcionar de manera independiente, no se ve afectado por el otro.

En el pasado, era necesario un conocimiento exhaustivo de la serialización para poner en cola, enviar y recibir mensajes asincrónicos. Ahora, el servicio de componentes en cola COM+ calcula automáticamente las referencias a los datos en forma de mensaje de Message Queue Server y los utiliza para los desarrolladores de componentes. Y dado que el servicio de componentes en cola ofrece compatibilidad integrada para transacciones, un estado incoherente no puede poner en peligro los datos si se produce un error en el servidor.

Los temas siguientes de esta sección contienen información general sobre el diseño y la escritura de componentes en cola.



| Tema                                                                           | Descripción                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Ventajas del procesamiento en cola](benefits-of-queued-processing.md)<br/>   | Describe las ventajas de la programación con componentes en cola de COM+.<br/>                                         |
| [Arquitectura de componentes en cola](queued-components-architecture.md)<br/> | Describe la arquitectura del servicio de componentes en cola de COM+.<br/>                                          |
| [Message Queue Server transaccional](transactional-message-queuing.md)<br/>   | Describe cómo administra las transacciones el servicio de componentes en cola de COM+.<br/>                              |
| [Seguridad de componentes en cola](queued-components-security.md)<br/>         | Describe las opciones de directiva para la autenticación de mensajes de cliente y sus implicaciones.<br/>                 |
| [Desarrollar componentes en cola](developing-queued-components.md)<br/>     | Describe las consideraciones de programación al escribir componentes de queuable.<br/>                                     |
| [Errores de componentes en cola](queued-components-errors.md)<br/>             | Describe los tipos de errores más comunes que pueden producirse al usar el servicio de componentes en cola de COM+.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas de componentes en cola de COM+](com--queued-components-tasks.md)
</dt> </dl>

 

 




