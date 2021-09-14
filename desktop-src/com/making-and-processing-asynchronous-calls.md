---
title: Realización y procesamiento de llamadas asincrónicas
description: Los objetos COM pueden admitir llamadas asincrónicas.
ms.assetid: bf7f9f8e-66ce-41a4-854c-62dbe840a89e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059f55cc64a70f130e7fb654426803edbe8b7209
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249231"
---
# <a name="making-and-processing-asynchronous-calls"></a>Realización y procesamiento de llamadas asincrónicas

Los objetos COM pueden admitir llamadas asincrónicas. Cuando un cliente realiza una llamada asincrónica, el control vuelve al cliente inmediatamente. Mientras el servidor procesa la llamada, el cliente puede realizar otro trabajo de forma gratuita. Cuando el cliente ya no puede continuar sin los resultados de la llamada, puede obtener los resultados de la llamada en ese momento.

Por ejemplo, una solicitud para un conjunto de registros grande o complejo puede llevar mucho tiempo. Un cliente puede solicitar el conjunto de registros mediante una llamada asincrónica y, a continuación, realizar otro trabajo. Cuando el conjunto de registros está disponible, el cliente puede obtenerlo rápidamente sin bloquearlo.

Los clientes no hacen llamadas asincrónicas directamente en el objeto de servidor. En su lugar, obtienen un objeto de llamada que implementa una versión asincrónica de una interfaz sincrónica en el objeto de servidor. La interfaz asincrónica en el objeto de llamada tiene un nombre con el formato Async *InterfaceName*. Por ejemplo, si un objeto de servidor implementa una interfaz sincrónica denominada IMyInterface, habrá un objeto de llamada que implementa una interfaz asincrónica denominada AsyncIMyInterface.

> [!Note]  
> La compatibilidad asincrónica no está disponible para **IDispatch** ni para las interfaces que heredan **IDispatch.**

 

Los objetos de servidor que admiten llamadas asincrónicas implementan [**la interfaz ICallFactory.**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) Esta interfaz expone un único método, [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), que crea una instancia de un objeto de llamada especificado. Los clientes pueden consultar **ICallFactory para** determinar si un objeto admite llamadas asincrónicas.

Para cada método de una interfaz sincrónica, la interfaz asincrónica correspondiente implementa dos métodos. Estos métodos asocian los prefijos Begin \_ y Finish al nombre del método \_ sincrónico. Por ejemplo, si una interfaz denominada ISimpleStream tiene un método Read, la interfaz AsyncISimpleStream tendrá un método Begin Read y \_ Finish \_ Read. Para iniciar una llamada asincrónica, el cliente llama al método \_ Begin.

Al implementar un objeto de servidor, no es necesario proporcionar un objeto de llamada para cada interfaz que implementa el objeto. Si el objeto de servidor implementa la interfaz [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) y usa la serialización estándar, un cliente serializado siempre puede obtener un objeto de llamada de proxy, incluso si no hay ningún objeto de llamada en el lado servidor. Este proxy serializará el método Begin como una llamada sincrónica, el servidor procesará la llamada sincrónicamente y el cliente puede obtener los parámetros out llamando al \_ método \_ Finish.

Por el contrario, si un cliente realiza una llamada sincrónica serializada en una interfaz para la que hay un objeto de llamada en el lado servidor, el servidor siempre procesará la llamada de forma asincrónica. Este comportamiento no será evidente para el cliente, ya que el cliente recibirá los mismos parámetros out y el mismo valor devuelto que habría recibido del método sincrónico.

En cualquier caso, la interacción entre el cliente y el servidor se serializa como si la llamada fuera sincrónica: la salida de los servidores proxy sincrónicos y asincrónicos no se puede diferenciar, al igual que la salida de los códigos auxiliares correspondientes. Este comportamiento simplifica en gran medida el modelo de programación tanto de los clientes como de los servidores. Si un objeto de servidor implementa [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory), un cliente serializado no tiene que intentar crear un objeto de llamada que puede no estar disponible para el cliente, siempre hay disponible un objeto de llamada.

Cuando el cliente y el servidor están en el mismo apartamento, el objeto de servidor procesará la llamada que haga el cliente. Si un objeto de llamada no está disponible, el cliente debe obtener explícitamente la interfaz sincrónica y realizar una llamada sincrónica.

Para obtener más información, vea los temas siguientes:

-   [Realizar una llamada asincrónica](making-an-asynchronous-call.md)
-   [Cancelación de una llamada asincrónica](canceling-an-asynchronous-call.md)
-   [Cancelación de llamadas a métodos](canceling-method-calls.md)
-   [Sincronización de llamadas](call-synchronization.md)

 

 