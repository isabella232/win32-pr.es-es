---
title: Creación de suscripciones de eventos de hardware
description: En los equipos que tienen instalado un controlador de administración de placa base (BMC), los eventos de hardware se inician y registran en el registro de eventos del sistema (SEL), que es el almacén de eventos de BMC que se almacena en memoria no volátil.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a56f2fa627de3a640e03be7c60f3950d06f752b3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885861"
---
# <a name="creating-hardware-event-subscriptions"></a>Creación de suscripciones de eventos de hardware

En los equipos que tienen instalado un controlador de administración de placa base (BMC), los eventos de hardware se inician y registran en el registro de eventos del sistema (SEL), que es el almacén de eventos de BMC que se almacena en memoria no volátil. Para leer estos eventos de hardware en Windows Server 2008 mediante el Visor de eventos, debe crear una suscripción a los eventos. Las suscripciones de eventos de hardware solo funcionarán Windows Server 2008.

El procedimiento siguiente define cómo crear la suscripción de eventos SEL para recuperar los eventos de hardware:

1.  Guarde el siguiente xml en un archivo .xml (en este ejemplo, el archivo se denomina Wsmanselrg.xml). Este XML define la suscripción.

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

    

2.  Cree una suscripción de eventos ejecutando el siguiente comando en una ventana del símbolo del sistema (el programa Wecutil.exe se encuentra en el directorio %SYSTEMROOT% \\ System32).):

    **Ruta de acceso de Wecutil cs** *&lt; &gt; \\wsmanselrg.xml*

3.  Asegúrese de que la suscripción está activa ejecutando el siguiente comando en una ventana del símbolo del sistema:

    **Wecutil gr** *wsmanselrg*

BMC es un microcontrolador conectado localmente a un servidor. Los BMC tienen sensores que supervisan el estado físico del servidor y una conexión de red independiente que se puede comunicar a través de la red, incluso si el servidor está sin conexión. Tiene acceso a los datos de BMC a través del proveedor WMI de interfaz de administración de plataforma inteligente (IPMI). Para obtener más información sobre el proveedor de IPMI, vea [Proveedor de IPMI.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)

El equipo debe tener el BMC y el proveedor de IPMI instalados para que la suscripción de eventos funcione. En el caso de los equipos Windows Server 2008, el proveedor de IPMI se instala de forma predeterminada. Si el BMC no está disponible, no se puede instalar el controlador IPMI y el estado de tiempo de ejecución de la suscripción siempre mostrará un error (0x8004001- Error genérico de WMI).

 

 
