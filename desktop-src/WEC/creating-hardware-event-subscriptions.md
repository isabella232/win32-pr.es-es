---
title: Creación de suscripciones de eventos de hardware
description: En los equipos que tienen instalado un controlador de administración de placa base (BMC), los eventos de hardware se producen y registran en el registro de eventos del sistema (SEL), que es el almacén de eventos de BMC que se almacena en memoria no volátil.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc5f904e74d1f29b0666c9cb02b13689a0633bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359234"
---
# <a name="creating-hardware-event-subscriptions"></a>Creación de suscripciones de eventos de hardware

En los equipos que tienen instalado un controlador de administración de placa base (BMC), los eventos de hardware se producen y registran en el registro de eventos del sistema (SEL), que es el almacén de eventos de BMC que se almacena en memoria no volátil. Para leer estos eventos de hardware en Windows Server 2008 mediante el Visor de eventos, debe crear una suscripción a los eventos. Las suscripciones de eventos de hardware solo funcionarán en Windows Server 2008.

En el procedimiento siguiente se define cómo crear la suscripción de evento SEL para recuperar los eventos de hardware:

1.  Guarde el siguiente código XML en un archivo. XML (en este ejemplo, el archivo se denomina Wsmanselrg.xml). Este XML define la suscripción.

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <Description>A subscription for the HardwareEvents</Description>
        <SubscriptionId>WSManSelRg</SubscriptionId>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel</Uri>
        <EventSources>
            <EventSource>
                <Address>LOCALHOST</Address>
            </EventSource>
        </EventSources>
        <LogFile>HardwareEvents</LogFile>
        <Delivery Mode="pull">
            <PushSettings>
                <Heartbeat Interval="10000"/>
            </PushSettings>
        </Delivery>
    </Subscription>
    ```

    

2.  Cree una suscripción de eventos mediante la ejecución del siguiente comando en una ventana del símbolo del sistema (el programa Wecutil.exe se encuentra en el directorio% SYSTEMROOT% \\ system32):

    **Wecutil CS** *<path> \\wsmanselrg.xml*

3.  Asegúrese de que la suscripción está activa ejecutando el siguiente comando en una ventana del símbolo del sistema:

    **Wecutil gr** *wsmanselrg*

El BMC es un microcontrolador conectado localmente a un servidor. Los BMC tienen sensores que supervisan el estado físico del servidor y una conexión de red independiente que se puede comunicar a través de la red, incluso si el servidor está sin conexión. Tiene acceso a los datos de BMC a través del proveedor WMI de interfaz de administración de plataforma inteligente (IPMI). Para obtener más información acerca del proveedor IPMI, consulte el [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

El equipo debe tener instalado el proveedor de BMC y IPMI para que funcione la suscripción de eventos. En el caso de los equipos que ejecutan Windows Server 2008, el proveedor IPMI se instala de manera predeterminada. Si el BMC no está disponible, no se puede instalar el controlador IPMI y el estado en tiempo de ejecución de la suscripción siempre mostrará un error (0x8004001: error genérico de WMI).

 

 