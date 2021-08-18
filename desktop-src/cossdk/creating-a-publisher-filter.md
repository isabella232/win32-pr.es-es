---
description: Crear un filtro Publisher filtro
ms.assetid: d91efecc-f02a-41c6-acf7-37b74723e7e8
title: Crear un filtro Publisher filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2cf3391cd331f7d81c3bb7ff467c140a78b0c8e30fb609ea655596dfe745a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128797"
---
# <a name="creating-a-publisher-filter"></a>Crear un filtro Publisher filtro

Hay dos métodos para establecer el filtro del publicador: mediante la propiedad MultiPublisherFilterCLSID de la clase de evento o [**mediante IEventControl::SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter).

-   Dado que permite crear el objeto de evento con el servicio de componentes en cola [de COM+,](com--queued-components.md) el método preferido es usar la propiedad MultiPublisherFilterCLSID en la clase de eventos para establecer el filtro del publicador. Esto establece un objeto de filtro para todos los métodos de las interfaces de evento para un objeto de evento. El objeto de evento activa el filtro del publicador cuando se crea una instancia del objeto de clase de eventos [**mediante CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).
-   También puede usar [**SetPublisherFilter.**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter) Sin embargo, si elige este método, la interfaz no se puede poner en cola y, por tanto, no puede usar el objeto de evento con el servicio de componentes en cola de COM+ entre el publicador y el objeto de clase de eventos. Para obtener información adicional sobre el uso del servicio de componentes en cola con eventos COM+, vea [Using COM+ Events with COM+ Queued Components](using-com--events-with-com--queued-components.md).

Un evento puede tener uno o varios objetos de filtro o ninguno en absoluto. Los objetos de filtro del publicador deben admitir [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) o [**IMultiInterfacePublisherFilter,**](/windows/desktop/api/EventSys/nn-eventsys-imultiinterfacepublisherfilter)en función de si tiene una sola interfaz de activación o varias interfaces de activación en el objeto de clase de evento. Las **interfaces IPublisherFilter** **e IMultiInterfacePublisherFilter** especifican un **método Initialize.** El **objeto de** clase de eventos llama al método Initialize inmediatamente después de crear el objeto de filtro.

Eventos COM+ intenta invocar dos métodos en el filtro. En primer lugar, llama a [**IPublisherFilter::P repareToFire**](/windows/desktop/api/EventSys/nf-eventsys-ipublisherfilter-preparetofire) y pasa un puntero de interfaz [**IFiringControl**](/windows/desktop/api/EventSys/nn-eventsys-ifiringcontrol) al filtro. A continuación, consulta el objeto de filtro para la interfaz de eventos. Si el filtro admite la interfaz de eventos, invoca un método en ella. Esto proporciona acceso a los parámetros del publicador para un evento. El filtro puede usar estos parámetros para determinar qué suscripciones se deben activa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de eventos en COM+](filtering-events-in-com-.md)
</dt> </dl>

 

 
