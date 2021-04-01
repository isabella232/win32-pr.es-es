---
description: Crear un filtro de publicador
ms.assetid: d91efecc-f02a-41c6-acf7-37b74723e7e8
title: Crear un filtro de publicador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997fe37cf0021bcb2aa153c2dc4b73597e0c43cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153465"
---
# <a name="creating-a-publisher-filter"></a>Crear un filtro de publicador

Hay dos métodos para establecer el filtro del publicador: mediante la propiedad MultiPublisherFilterCLSID de la clase de eventos o mediante [**IEventControl:: SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter).

-   Dado que permite crear el objeto de evento con el servicio de [componentes en cola de com+](com--queued-components.md) , el método preferido es usar la propiedad MultiPublisherFilterCLSID en la clase de eventos para establecer el filtro del publicador. Esto establece un objeto de filtro para todos los métodos de las interfaces de eventos de un objeto de evento. El objeto de evento activa el filtro del publicador cuando se crea una instancia del objeto de la clase de evento mediante [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).
-   También puede usar [**SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter). Sin embargo, si elige este método, la interfaz no se queuable y, por lo tanto, no puede usar el objeto de evento con el servicio de componentes en cola de COM+ entre el publicador y el objeto de la clase de evento. Para obtener información adicional acerca del uso del servicio de componentes en cola con eventos COM+, vea [using com+ events with com+ queued Components](using-com--events-with-com--queued-components.md).

Un evento puede tener uno o más objetos de filtro o ninguno. Los objetos de filtro del publicador deben admitir [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) o [**IMultiInterfacePublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-imultiinterfacepublisherfilter), en función de si tiene una sola interfaz de activación o varias interfaces de activación en el objeto de la clase de evento. Las interfaces **IPublisherFilter** y **IMultiInterfacePublisherFilter** especifican un método **Initialize** . El objeto de la clase de eventos llama al método **Initialize** inmediatamente después de crear el objeto de filtro.

Los eventos COM+ intentan invocar dos métodos en el filtro. En primer lugar, llama a [**IPublisherFilter::P reparetofire**](/windows/desktop/api/EventSys/nf-eventsys-ipublisherfilter-preparetofire) y pasa un puntero de interfaz [**IFiringControl**](/windows/desktop/api/EventSys/nn-eventsys-ifiringcontrol) al filtro. A continuación, consulta el objeto de filtro de la interfaz de eventos. Si el filtro es compatible con la interfaz de eventos, invoca un método en él. Esto proporciona acceso a los parámetros del publicador para un evento. El filtro puede utilizar estos parámetros para determinar qué suscripciones se van a activar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de eventos en COM+](filtering-events-in-com-.md)
</dt> </dl>

 

 
