---
description: Un consumidor físico es un objeto COM que implementa la interfaz IWbemUnboundObjectSink.
ms.assetid: 497457dc-61ca-4527-89fd-2af0383de5e9
ms.tgt_platform: multiple
title: Implementación de un consumidor físico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed667c59a703087ba09481bacaf57b517df7ecf38fe31fb8e9883f765bc85f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108653"
---
# <a name="implementing-a-physical-consumer"></a>Implementación de un consumidor físico

Un consumidor físico es un objeto COM que implementa la [**interfaz IWbemUnboundObjectSink.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) WMI carga el consumidor físico y pasa eventos a través de **IWbemUnboundObjectSink** en respuesta a uno o varios eventos, tal y como define el consumidor lógico asociado. Los consumidores permanentes tienen requisitos de seguridad especiales. Para obtener más información, vea [Securing WMI Events](securing-wmi-events.md).

En el procedimiento siguiente se describe cómo implementar un consumidor físico para un consumidor de eventos permanente.

**Para implementar un consumidor físico para un consumidor de eventos permanente**

1.  Cree un objeto COM.

    Debe implementar un consumidor físico como un servidor local o remoto mediante el protocolo COM.

2.  Determine si desea admitir la notificación de eventos sincrónica o asincrónica.

    Con la notificación de eventos asincrónica, el subproceso de envío no está relacionado con el subproceso receptor. Por lo tanto, ni WMI ni el proveedor de eventos se bloquean mientras WMI entrega una notificación a cualquier consumidor registrado para recibir el evento. La desventaja de la entrega asincrónica es que se produce un cambio de contexto entre el momento en que el proveedor genera el evento y el momento en que el consumidor recibe el evento. Para obtener más información sobre cómo trabajar de forma asincrónica, vea el tema [Aspectos básicos](../com/guide.md) de COM en la sección COM del Kit de desarrollo de software (SDK) de Microsoft Windows. Para obtener más información sobre los modificadores de contexto, vea el tema [Cambios de](../procthread/context-switches.md) contexto en la sección DLL, procesos y subprocesos del SDK de Windows.

    > [!Note]  
    > Dado que es posible que la devolución de llamada al receptor no se devuelva en el mismo nivel de autenticación que el cliente requiere, se recomienda usar la comunicación semisincronosa en lugar de la asincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

     

    Con la notificación sincrónica, WMI entrega la notificación en el mismo subproceso que el proveedor de eventos usó para entregar el evento a WMI. En este caso, cuando un proveedor de eventos envía una notificación, WMI bloquea el proveedor de eventos hasta que WMI entrega la notificación. Solo si el consumidor es extremadamente rápido y puede procesar un evento en 100 microsegundos o menos, debe considerar la posibilidad de admitir la notificación sincrónica. Los consumidores sincrónicos que tardan demasiado tiempo en procesar eventos pueden ralentizar gravemente la entrega de eventos a todos los demás consumidores. Además, pueden bloquear accidentalmente el proveedor. Para obtener más información, vea [Enlazar un filtro de eventos con un consumidor lógico.](binding-an-event-filter-with-a-logical-consumer.md)

3.  Implemente [**la función IWbemUnboundObjectSink::IndicateToConsumer.**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer)

    WMI usa la [**función IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) para pasar los punteros y eventos necesarios al consumidor físico para las comunicaciones sincrónicas y asincrónicas. La implementación de **IndicateToConsumer** debe contener todo el código necesario para responder a un evento.

    A diferencia de un consumidor de eventos temporal, no es necesario llamar a la [**interfaz IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) para ponerse en contacto con WMI. En su lugar, WMI busca un puntero al consumidor a través del proveedor de consumidores de eventos. Para obtener más información, vea [Escribir un proveedor de consumidores de eventos.](writing-an-event-consumer-provider.md)

    Sin embargo, si desea volver a llamar a WMI, use las interfaces [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) [**e IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) El método tradicional para conectarse a WMI es durante el proceso de inicialización del objeto COM. Para obtener más información, vea [Crear una aplicación WMI o script](creating-a-wmi-application-or-script.md).

    Si implementa el consumidor físico como un servidor COM en proceso y se conecta a WMI independientemente del proceso de inicialización, debe usar el identificador de clase **\_ CLSID WbemAdministrativeLocator** para tener acceso a la interfaz [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) en la llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    En el ejemplo siguiente se muestra cómo usar el identificador de clase **\_ CLSID WbemAdministrativeLocator** para tener acceso a la [**interfaz IWbemLocator.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)

    ```C++
    IWbemLocator *pLoc = 0;

    DWORD dwRes = CoCreateInstance(CLSID_WbemAdministrativeLocator, 0, 
        CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
    ```

    

    La [**interfaz IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) obtiene el puntero de espacio de nombres inicial a WMI en un equipo host determinado. Si no se usa el **identificador \_ WBEMAdministrativeLocator de CLSID** en la llamada [**a CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) se produce un error de "acceso denegado".

    En circunstancias habituales, WMI entrega eventos asincrónicos al cliente de uno en uno. Sin embargo, si un cliente no puede recibir notificaciones de eventos asincrónicas tan rápido como llegan los eventos, WMI comienza a procesar automáticamente los eventos por lotes en una sola llamada. El procesamiento por lotes automático ayuda si los tiempos de ida y vuelta son un problema, como suele ser el caso en escenarios de alto rendimiento. Sin embargo, el procesamiento por lotes no mejora el rendimiento del sistema si el cliente o el ancho de banda de red tienen un error.

 

 
