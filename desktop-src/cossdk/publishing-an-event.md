---
description: Publicación de un evento
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Publicación de un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705320"
---
# <a name="publishing-an-event"></a>Publicación de un evento

Para publicar un evento, basta con crear una instancia de un objeto de evento llamando a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o el método **CreateObject** de Microsoft Visual Basic mediante EventClassID o EventClassName como argumento. El publicador llama a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto de evento para obtener las interfaces admitidas por el objeto de la clase de evento e invoca un método en el objeto de evento a través de la interfaz para publicar el evento. Después, el sistema de eventos publica eventos en la clase de evento CLSID \_ EventObjectChange con el identificador de interfaz IID \_ IEventObjectChange.

Para admitir la entrega de eventos a varios suscriptores, los métodos de la clase de evento solo deben contener parámetros in.

Mediante el uso de la propiedad FireInParallel del objeto de la [clase de eventos](the-com--event-class-object.md) , los publicadores pueden solicitar que el sistema de eventos utilice varios subprocesos para proporcionar un evento a más de un suscriptor. La selección de un mecanismo de entrega en paralelo no garantiza la entrega simultánea del evento a varios suscriptores, pero indica al servicio de eventos COM+ que le permita que esto suceda.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Publicar y entregar eventos en COM+](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
