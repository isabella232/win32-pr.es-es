---
description: Un proveedor de eventos debe implementar la interfaz IWbemEventProvider para generar notificaciones de eventos.
ms.assetid: ae33c9f5-61f7-4488-a281-01d7f9c62c46
ms.tgt_platform: multiple
title: Implementar la interfaz principal para un proveedor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5621a2c6d0901a7925828149dd5c1480c2b11456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002433"
---
# <a name="implementing-the-primary-interface-for-an-event-provider"></a>Implementar la interfaz principal para un proveedor de eventos

Un proveedor de eventos debe implementar la interfaz [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) para generar notificaciones de eventos. WMI llama al método [**IWbemEventProvider::P rovideevents**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovider-provideevents) del proveedor y pasa un puntero al objeto receptor, que es una implementación de la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) . Cuando el proveedor de eventos está listo para generar una notificación, el proveedor llama al método [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

Un proveedor de eventos debe colocar las notificaciones generadas a través de [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) en objetos de evento. Debe implementar los objetos de evento como entradas en una matriz de interfaces [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) representadas por el parámetro *PpObjArray* del método [**indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) . Dado que **IWbemClassObjects** son objetos com, el proveedor debe incrementar el recuento de referencias para el receptor llamando al método [**IWbemObjectSink:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) . Los proveedores de eventos que deben proporcionar muchas notificaciones (por ejemplo, eventos 400) deben crear un objeto de evento único para cada notificación generando una nueva instancia o clonando una existente. WMI nunca se mantiene en un objeto de evento más allá de la finalización de la llamada a **indica** y no tiene ningún requisito especial para **AddRef** superior y superior al estándar com.

Tenga en cuenta las siguientes directrices al implementar un proveedor de eventos:

-   No realice ningún cambio de clase mientras atiende una llamada de cliente.
-   No emita llamadas relacionadas con eventos, como una llamada que modifique un filtro de eventos.
-   Procese cualquier solicitud que el servicio de administración de Windows emita, como [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery), antes de volver a desencadenar un evento.

    Si no procesa la solicitud, volver a desencadenar el evento podría impedir que se aceptara el evento.

-   Nunca llame a [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) desde dentro de un proveedor.

 

 
