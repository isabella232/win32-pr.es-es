---
title: Realizar y procesar llamadas asincrónicas
description: Los objetos COM pueden admitir llamadas asincrónicas.
ms.assetid: bf7f9f8e-66ce-41a4-854c-62dbe840a89e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059f55cc64a70f130e7fb654426803edbe8b7209
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105695766"
---
# <a name="making-and-processing-asynchronous-calls"></a>Realizar y procesar llamadas asincrónicas

Los objetos COM pueden admitir llamadas asincrónicas. Cuando un cliente realiza una llamada asincrónica, el control vuelve al cliente inmediatamente. Mientras el servidor procesa la llamada, el cliente es gratuito para realizar otro trabajo. Cuando el cliente ya no puede continuar sin los resultados de la llamada, puede obtener los resultados de la llamada en ese momento.

Por ejemplo, una solicitud para un conjunto de registros grande o complejo puede llevar mucho tiempo. Un cliente puede solicitar el conjunto de registros mediante una llamada asincrónica y, a continuación, realizar otro trabajo. Cuando el conjunto de registros está disponible, el cliente puede obtenerlo rápidamente sin bloqueos.

Los clientes no realizan llamadas asincrónicas directamente en el objeto de servidor. En su lugar, obtienen un objeto de llamada que implementa una versión asincrónica de una interfaz sincrónica en el objeto de servidor. La interfaz asincrónica en el objeto Call tiene un nombre con el formato Async *interfacename*. Por ejemplo, si un objeto de servidor implementa una interfaz sincrónica denominada IMyInterface, habrá un objeto de llamada que implementa una interfaz asincrónica denominada AsyncIMyInterface.

> [!Note]  
> La compatibilidad asincrónica no está disponible para **IDispatch** o para interfaces que heredan **IDispatch**.

 

Los objetos de servidor que admiten llamadas asincrónicas implementan la interfaz [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) . Esta interfaz expone un método único, [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), que crea una instancia de un objeto de llamada especificado. Los clientes pueden consultar **ICallFactory** para determinar si un objeto admite llamadas asincrónicas.

Para cada método en una interfaz sincrónica, la interfaz asincrónica correspondiente implementa dos métodos. Estos métodos adjuntan los prefijos Begin \_ y Finish \_ al nombre del método sincrónico. Por ejemplo, si una interfaz denominada ISimpleStream tiene un método de lectura, la interfaz AsyncISimpleStream tendrá un método de lectura Begin \_ y de finalización \_ . Para comenzar una llamada asincrónica, el cliente llama al método Begin \_ .

Cuando se implementa un objeto de servidor, no es necesario proporcionar un objeto de llamada para cada interfaz que implementa el objeto. Si el objeto de servidor implementa la interfaz [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) y usa el cálculo de referencias estándar, un cliente con cálculo de referencias siempre puede obtener un objeto de llamada de proxy, incluso si no hay ningún objeto de llamada en el lado del servidor. Este proxy serializará el \_ método Begin como una llamada sincrónica, el servidor procesará la llamada de forma sincrónica y el cliente puede obtener los parámetros out llamando al método Finish \_ .

Por el contrario, si un cliente realiza una llamada sincrónica de serialización en una interfaz para la que hay un objeto de llamada en el lado servidor, el servidor siempre procesará la llamada de forma asincrónica. Este comportamiento no será aparente para el cliente, ya que el cliente recibirá los mismos parámetros out y el mismo valor devuelto que habría recibido del método sincrónico.

En cualquier caso, la interacción entre el cliente y el servidor se calcula como si la llamada fuera sincrónica: la salida de los proxies sincrónicos y asincrónicos es indistinguible, como es la salida del código auxiliar correspondiente. Este comportamiento simplifica considerablemente el modelo de programación de los clientes y de los servidores. Si un objeto de servidor implementa [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory), un cliente serializado no tiene que intentar crear un objeto de llamada que puede no estar disponible; para el cliente, siempre está disponible un objeto de llamada.

Cuando el cliente y el servidor están en el mismo apartamento, el objeto de servidor procesará la llamada que realice el cliente. Si un objeto de llamada no está disponible, el cliente debe obtener explícitamente la interfaz sincrónica y hacer una llamada sincrónica.

Para obtener más información, vea los temas siguientes:

-   [Realización de una llamada asincrónica](making-an-asynchronous-call.md)
-   [Cancelar una llamada asincrónica](canceling-an-asynchronous-call.md)
-   [Cancelar llamadas a métodos](canceling-method-calls.md)
-   [Sincronización de llamadas](call-synchronization.md)

 

 