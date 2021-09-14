---
description: Publicación de un evento
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Publicación de un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063894"
---
# <a name="publishing-an-event"></a>Publicación de un evento

Para publicar un evento, simplemente cree una instancia de un objeto de evento mediante una llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o al método **CreateObject** de Microsoft Visual Basic mediante EventClassID o EventClassName como argumento. El publicador llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto de evento para obtener las interfaces admitidas por el objeto de clase de eventos e invoca un método en el objeto de evento a través de la interfaz para publicar el evento. A continuación, el sistema de eventos publica eventos en la clase de eventos CLSID EventObjectChange con el identificador de \_ interfaz \_ IID IEventObjectChange.

Para admitir la entrega de eventos a varios suscriptores, los métodos de clase de eventos solo deben contener en parámetros.

Mediante el uso de la propiedad [](the-com--event-class-object.md) FireInParallel del objeto de clase de eventos, los publicadores pueden solicitar que el sistema de eventos use varios subprocesos para entregar un evento a más de un suscriptor. La selección de un mecanismo de entrega en paralelo no garantiza la entrega simultánea del evento a varios suscriptores, pero indica al servicio de eventos COM+ que permita que esto suceda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Publicación y entrega de eventos en COM+](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
