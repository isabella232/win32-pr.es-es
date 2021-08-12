---
description: Errores Client-Side persistentes
ms.assetid: f991db71-8319-414d-8a25-2d02bc7c8b51
title: Errores Client-Side persistentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e832ec8339c33263600a1657b8d29ef2d2aecf4ceb3e000666f9db5776b3ac13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305778"
---
# <a name="persistent-client-side-failures"></a>Errores Client-Side persistentes

En algunos casos, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) puede mover un mensaje a la cola de destino. Por ejemplo, si los controles de acceso a la cola no permiten que el mensaje se traslade del cliente al servidor, el mensaje infractor se mueve a la cola de mensajes no enviados del lado cliente. Cuando esto sucede, el servicio de componentes en cola de COM+ permite asociar una clase de excepción a un componente. Para asociar la clase de excepción con el componente, use la **pestaña Avanzadas** de la página de propiedades del componente de la herramienta de administración Servicios de componentes. También puede asociar la clase de excepción mediante programación mediante el atributo del componente de catálogo ExceptionClass de las funciones administrativas de COM+.

La clase de excepción se define como progID o CLSID de un componente que implementa [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). El servicio de componentes en cola tiene un monitor de cola de mensajes fallidos que examina la cola de mensajes no enviados de Xact. Si hay un mensaje en la cola, el monitor de cola de mensajes fallidos crea una instancia del controlador de excepciones asociado al componente de destino y llama a [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry), lo que indica que se ha producido un error irrecuperable del lado cliente.

Además de [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol), el controlador de excepciones debe implementar el mismo conjunto de interfaces que el componente de servidor para el que controla las excepciones. Cuando [**se llama a IPlaybackControl::FinalClientRetry,**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) los componentes en cola en tiempo de ejecución reproducen el mensaje con errores en el controlador de excepciones. Esto permite que el controlador de excepciones implemente un comportamiento alternativo para los mensajes que no se pueden mover al servidor, por ejemplo, mediante la generación de una transacción de compensación.

Si el controlador de excepciones completa todas las llamadas de método reproducidas, el mensaje se quita de la cola de mensajes no enviados de Xact y se descarta. Sin embargo, si el controlador de excepciones anula el mensaje devolviendo un estado de error de una de las llamadas de método, el mensaje se devuelve a la cola de mensajes no enviados de Xact. La siguiente secuencia de eventos muestra cómo se controlan las excepciones del lado cliente:

1.  Message Queuing no puede entregar un mensaje al servidor y coloca el mensaje en la cola de mensajes no enviados de Xact.
2.  El agente de escucha de cola de mensajes no enviados (DLQL) busca un mensaje en la cola de mensajes no enviados de Xact.
3.  DLQL recupera el CLSID del componente de destino del mensaje y comprueba si hay una clase de excepción.
4.  DLQL crea una instancia de la clase de excepción.
5.  DlQL consulta [**IPlaybackControl para**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) la clase de excepción.
6.  DLQL llama al método [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) en la clase de excepción.
7.  DLQL reproduce todas las llamadas de propiedad y método del mensaje a la clase de excepción.
8.  DLQL elimina el mensaje si el controlador de excepciones completa la transacción correctamente. El controlador de excepciones puede emitir [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)y el mensaje permanecerá en la cola de mensajes no enviados.

Si se producirá un error en cualquiera de los pasos anteriores, el mensaje se deja en la cola de mensajes no enviados de Xact.

Cuando se inicia, DLQL lee cada mensaje de la cola de mensajes no enviados transaccionales de Message Queuing y crea instancias de la clase de excepción para cada mensaje de componentes en cola. Después de pasar por la cola, espera nuevos mensajes. A continuación, procesa cada nuevo mensaje de cola de mensajes fallidos a medida que llega.

Si necesita intervención en el proceso descrito aquí o si necesita mover un mensaje dudoso de su cola de reposo final, use la utilidad de mover mensajes. Para obtener más información sobre la utilidad de mover mensajes, vea [Controlar errores.](handling-errors-in-queued-components.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores del lado cliente](client-side-errors.md)
</dt> <dt>

[Errores del lado servidor](server-side-errors.md)
</dt> </dl>

 

 



