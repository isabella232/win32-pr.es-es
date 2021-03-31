---
description: Errores de Client-Side persistentes
ms.assetid: f991db71-8319-414d-8a25-2d02bc7c8b51
title: Errores de Client-Side persistentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d303e712257d62e4ae42497cb4463e782cfbb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423375"
---
# <a name="persistent-client-side-failures"></a>Errores de Client-Side persistentes

En algunos casos, [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) puede trasladar un mensaje a la cola de destino. Por ejemplo, si los controles de acceso a la cola no permiten que el mensaje se mueva del cliente al servidor, el mensaje infractor se mueve a la cola de mensajes no enviados del lado cliente. Cuando esto ocurre, el servicio de componentes en cola de COM+ permite asociar una clase de excepción a un componente. Para asociar la clase de excepción al componente, utilice la pestaña **Opciones avanzadas** de la página Propiedades del componente de la herramienta de administración servicios de componentes. También puede asociar la clase de excepción mediante programación, mediante el atributo del componente de catálogo ExceptionClass de las funciones administrativas de COM+.

La clase de excepción se define como el ProgID o el CLSID de un componente que implementa [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). El servicio de componentes en cola tiene un monitor de cola de mensajes con problemas de entrega que examina la cola de mensajes no enviados Xact. Si hay un mensaje en la cola, el monitor de cola de mensajes con problemas de entrega crea una instancia del controlador de excepciones asociado al componente de destino y llama a [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry), lo que indica que se ha producido un error irrecuperable en el cliente.

Además de [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol), el controlador de excepciones debe implementar el mismo conjunto de interfaces que el componente de servidor para el que está controlando las excepciones. Cuando se llama a [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) , el tiempo de ejecución de los componentes en cola reproduce el mensaje con error al controlador de excepciones. Esto permite al controlador de excepciones implementar un comportamiento alternativo para los mensajes que no se pueden pasar al servidor, por ejemplo, mediante la generación de una transacción de compensación.

Si el controlador de excepciones completa todas las llamadas al método reproducidas, el mensaje se quita de la cola de mensajes con problemas de entrega Xact y se descarta. Sin embargo, si el controlador de excepciones anula el mensaje devolviendo un estado de error de una de las llamadas al método, el mensaje se devuelve a la cola de mensajes con problemas de entrega de transacciones. La siguiente secuencia de eventos muestra cómo se controlan las excepciones del cliente:

1.  Message Queue Server no puede enviar un mensaje al servidor y lo coloca en la cola de mensajes con problemas de entrega de transacciones.
2.  El agente de escucha de la cola de mensajes con problemas de entrega (DLQL) encuentra un mensaje en la cola de mensajes no enviados Xact.
3.  DLQL recupera el CLSID del componente de destino del mensaje y comprueba si existe una clase de excepción.
4.  El DLQL crea una instancia de la clase de excepción.
5.  DLQL consulta para [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) para la clase de excepción.
6.  DLQL llama al método [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) en la clase de excepción.
7.  DLQL reproduce todas las llamadas a propiedades y métodos desde el mensaje a la clase de excepción.
8.  El DLQL elimina el mensaje si el controlador de excepciones completa la transacción correctamente. El controlador de excepciones puede emitir [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)y el mensaje permanecerá en la cola de mensajes con problemas de entrega.

Si se produce un error en alguno de los pasos anteriores, el mensaje se deja en la cola de mensajes con problemas de entrega Xact.

Cuando se inicia, el DLQL Lee cada mensaje en la cola de mensajes con problemas de entrega transaccional de Message Queue Server y crea instancias de la clase de excepción para cada mensaje de componentes en cola. Después de un paso a través de la cola, espera mensajes nuevos. Después procesa cada nuevo mensaje de cola de mensajes con problemas de entrega cuando llega.

Si necesita intervenir en el proceso que se describe aquí o si necesita mover un mensaje dudoso fuera de la cola de salida final, use la utilidad del Movedor de mensajes. Para obtener más información sobre la utilidad del Movedor de mensajes, vea [control de errores](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores del lado cliente](client-side-errors.md)
</dt> <dt>

[Errores del lado servidor](server-side-errors.md)
</dt> </dl>

 

 



