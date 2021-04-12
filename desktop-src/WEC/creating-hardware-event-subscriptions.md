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
# <a name="creating-hardware-event-subscriptions"></a><span data-ttu-id="db1ca-103">Creación de suscripciones de eventos de hardware</span><span class="sxs-lookup"><span data-stu-id="db1ca-103">Creating Hardware Event Subscriptions</span></span>

<span data-ttu-id="db1ca-104">En los equipos que tienen instalado un controlador de administración de placa base (BMC), los eventos de hardware se producen y registran en el registro de eventos del sistema (SEL), que es el almacén de eventos de BMC que se almacena en memoria no volátil.</span><span class="sxs-lookup"><span data-stu-id="db1ca-104">On computers that have a Baseboard Management Controller (BMC) installed, hardware events are raised and logged in the System event log (SEL), which is the BMC event store that is stored in nonvolatile memory.</span></span> <span data-ttu-id="db1ca-105">Para leer estos eventos de hardware en Windows Server 2008 mediante el Visor de eventos, debe crear una suscripción a los eventos.</span><span class="sxs-lookup"><span data-stu-id="db1ca-105">To read these hardware events on Windows Server 2008 using the Event Viewer, you must create a subscription to the events.</span></span> <span data-ttu-id="db1ca-106">Las suscripciones de eventos de hardware solo funcionarán en Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="db1ca-106">The hardware event subscriptions will only work on Windows Server 2008.</span></span>

<span data-ttu-id="db1ca-107">En el procedimiento siguiente se define cómo crear la suscripción de evento SEL para recuperar los eventos de hardware:</span><span class="sxs-lookup"><span data-stu-id="db1ca-107">The following procedure defines how to create the SEL event subscription to retrieve the hardware events:</span></span>

1.  <span data-ttu-id="db1ca-108">Guarde el siguiente código XML en un archivo. XML (en este ejemplo, el archivo se denomina Wsmanselrg.xml).</span><span class="sxs-lookup"><span data-stu-id="db1ca-108">Save the following XML in an .xml file (in this example the file is named Wsmanselrg.xml).</span></span> <span data-ttu-id="db1ca-109">Este XML define la suscripción.</span><span class="sxs-lookup"><span data-stu-id="db1ca-109">This XML defines the subscription.</span></span>

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

    

2.  <span data-ttu-id="db1ca-110">Cree una suscripción de eventos mediante la ejecución del siguiente comando en una ventana del símbolo del sistema (el programa Wecutil.exe se encuentra en el directorio% SYSTEMROOT% \\ system32):</span><span class="sxs-lookup"><span data-stu-id="db1ca-110">Create an event subscription by executing the following command in a command prompt window (the Wecutil.exe program is located in the %SYSTEMROOT%\\System32 directory.):</span></span>

    <span data-ttu-id="db1ca-111">**Wecutil CS** *<path> \\wsmanselrg.xml*</span><span class="sxs-lookup"><span data-stu-id="db1ca-111">**Wecutil cs** *<path>\\wsmanselrg.xml*</span></span>

3.  <span data-ttu-id="db1ca-112">Asegúrese de que la suscripción está activa ejecutando el siguiente comando en una ventana del símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="db1ca-112">Ensure that the subscription is active by executing the following command in a command prompt window:</span></span>

    <span data-ttu-id="db1ca-113">**Wecutil gr** *wsmanselrg*</span><span class="sxs-lookup"><span data-stu-id="db1ca-113">**Wecutil gr** *wsmanselrg*</span></span>

<span data-ttu-id="db1ca-114">El BMC es un microcontrolador conectado localmente a un servidor.</span><span class="sxs-lookup"><span data-stu-id="db1ca-114">The BMC is a microcontroller attached locally to a server.</span></span> <span data-ttu-id="db1ca-115">Los BMC tienen sensores que supervisan el estado físico del servidor y una conexión de red independiente que se puede comunicar a través de la red, incluso si el servidor está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="db1ca-115">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="db1ca-116">Tiene acceso a los datos de BMC a través del proveedor WMI de interfaz de administración de plataforma inteligente (IPMI).</span><span class="sxs-lookup"><span data-stu-id="db1ca-116">You have access to BMC data through the Intelligent Platform Management Interface (IPMI) WMI Provider.</span></span> <span data-ttu-id="db1ca-117">Para obtener más información acerca del proveedor IPMI, consulte el [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="db1ca-117">For more information about the IPMI provider, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

<span data-ttu-id="db1ca-118">El equipo debe tener instalado el proveedor de BMC y IPMI para que funcione la suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="db1ca-118">The computer must have the BMC and the IPMI provider installed for the event subscription to work.</span></span> <span data-ttu-id="db1ca-119">En el caso de los equipos que ejecutan Windows Server 2008, el proveedor IPMI se instala de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="db1ca-119">For computers running on Windows Server 2008, the IPMI provider is installed by default.</span></span> <span data-ttu-id="db1ca-120">Si el BMC no está disponible, no se puede instalar el controlador IPMI y el estado en tiempo de ejecución de la suscripción siempre mostrará un error (0x8004001: error genérico de WMI).</span><span class="sxs-lookup"><span data-stu-id="db1ca-120">If the BMC is not available, then IPMI driver cannot be installed and the subscription runtime status will always display an error (0x8004001 - WMI Generic Failure).</span></span>

 

 