---
title: Marca de tiempo de paquetes
description: Las API de marca de tiempo de paquetes del asistente de IP proporcionan la capacidad de determinar la funcionalidad de marca de tiempo de un adaptador de red y de consultar marcas de tiempo desde el adaptador de red en forma de marcas de tiempo cruzadas.
ms.topic: article
ms.date: 01/19/2021
ms.openlocfilehash: 07743473bcb606ccdb86c55f14a3413adf10d73a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110560021"
---
# <a name="packet-timestamping"></a><span data-ttu-id="3f585-103">Marca de tiempo de paquetes</span><span class="sxs-lookup"><span data-stu-id="3f585-103">Packet timestamping</span></span>

## <a name="introduction"></a><span data-ttu-id="3f585-104">Introducción</span><span class="sxs-lookup"><span data-stu-id="3f585-104">Introduction</span></span>

<span data-ttu-id="3f585-105">Muchas tarjetas de interfaz de red (NIC o adaptadores de red) pueden generar una marca de tiempo en su hardware cada vez que se recibe o transmite un paquete.</span><span class="sxs-lookup"><span data-stu-id="3f585-105">Many network interface cards (NICs, or network adapters) can generate a timestamp in their hardware whenever a packet is received or transmitted.</span></span> <span data-ttu-id="3f585-106">La marca de tiempo se genera mediante el reloj de hardware propio de la NIC.</span><span class="sxs-lookup"><span data-stu-id="3f585-106">The timestamp is generated using the NIC's own hardware clock.</span></span> <span data-ttu-id="3f585-107">Esta característica la usa en particular el Protocolo de tiempo de precisión (PTP), que es un protocolo de sincronización de hora.</span><span class="sxs-lookup"><span data-stu-id="3f585-107">This feature is used in particular by the Precision Time Protocol (PTP), which is a time synchronization protocol.</span></span> <span data-ttu-id="3f585-108">PTP realiza el aprovisionamiento para usar estas marcas de tiempo de hardware dentro del propio protocolo.</span><span class="sxs-lookup"><span data-stu-id="3f585-108">PTP makes provision to use such hardware timestamps within the protocol itself.</span></span>

<span data-ttu-id="3f585-109">Las marcas de tiempo se pueden usar, por ejemplo, para calcular el tiempo empleado por un paquete dentro de la pila de red de la máquina antes de enviarse o recibirse desde la conexión.</span><span class="sxs-lookup"><span data-stu-id="3f585-109">The timestamps can, for example, be used to compute the time spent by a packet within the network stack of the machine before being sent to or received from the wire.</span></span> <span data-ttu-id="3f585-110">PtP puede usar esos cálculos para mejorar la precisión de la sincronización de la hora.</span><span class="sxs-lookup"><span data-stu-id="3f585-110">Those calculations can then be used by PTP to improve the accuracy of time synchronization.</span></span> <span data-ttu-id="3f585-111">La compatibilidad con la marca de tiempo de paquetes de los adaptadores de red está orientada a veces específicamente para el protocolo PTP.</span><span class="sxs-lookup"><span data-stu-id="3f585-111">The packet timestamping support of network adapters is geared sometimes specifically for the PTP protocol.</span></span> <span data-ttu-id="3f585-112">En otros casos, se proporciona un soporte técnico más general.</span><span class="sxs-lookup"><span data-stu-id="3f585-112">In other cases, a more general support is provided.</span></span>

<span data-ttu-id="3f585-113">Las API de marca de tiempo dan a Windows la capacidad de admitir la funcionalidad de marca de tiempo de hardware de los adaptadores de red para el protocolo PTP versión 2.</span><span class="sxs-lookup"><span data-stu-id="3f585-113">Timestamping APIs give Windows the ability to support the hardware timestamping capability of network adapters for the PTP version 2 protocol.</span></span> <span data-ttu-id="3f585-114">En general, las características incluyen proporcionar la capacidad de los controladores de adaptadores de red para admitir marcas de tiempo y para que las aplicaciones en modo de usuario consuman marcas de tiempo asociadas a los paquetes a través de [Windows Sockets](/windows/win32/winsock/windows-sockets-start-page-2) (consulte Marca de tiempo [winsock](/windows/win32/winsock/winsock-timestamping)).</span><span class="sxs-lookup"><span data-stu-id="3f585-114">Overall, the features include providing the ability to drivers of network adapters to support timestamps, and for user-mode applications to consume timestamps associated with packets through [Windows Sockets](/windows/win32/winsock/windows-sockets-start-page-2) (see [Winsock timestamping](/windows/win32/winsock/winsock-timestamping)).</span></span> <span data-ttu-id="3f585-115">Además, también está disponible la capacidad de generar marcas de tiempo de software, lo que permite que un controlador de red genere marcas de tiempo en el software.</span><span class="sxs-lookup"><span data-stu-id="3f585-115">In addition, the ability to generate software timestamps is also available, which allows a network driver to generate timestamps in software.</span></span> <span data-ttu-id="3f585-116">Estos controladores NIC generan estas marcas de tiempo de software mediante el equivalente en modo kernel [**de QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC).</span><span class="sxs-lookup"><span data-stu-id="3f585-116">Such software timestamps are generated by NIC drivers using the kernel-mode equivalent of [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC).</span></span> <span data-ttu-id="3f585-117">Sin embargo, no se admite tener *las marcas* de tiempo de hardware y software habilitadas juntas.</span><span class="sxs-lookup"><span data-stu-id="3f585-117">However, having both hardware *and* software timestamps enabled together isn't supported.</span></span>

<span data-ttu-id="3f585-118">En concreto, las API de marca de tiempo de paquetes del asistente de protocolos de Internet (asistente de IP) descritas en este tema proporcionan la capacidad de las aplicaciones en modo de usuario para determinar la funcionalidad de marca de tiempo de un adaptador de red y para consultar marcas de tiempo del adaptador de red en forma de marcas de tiempo cruzadas (que se describen a continuación).</span><span class="sxs-lookup"><span data-stu-id="3f585-118">In particular, the Internet Protocol Helper (IP Helper) packet timestamping APIs described in this topic provide the ability for user-mode applications to determine the timestamping capability of a network adapter, and to query timestamps from the network adapter in the form of cross timestamps (described below).</span></span>

## <a name="supporting-precision-time-protocol-version-2"></a><span data-ttu-id="3f585-119">Compatibilidad con el protocolo de tiempo de precisión versión 2</span><span class="sxs-lookup"><span data-stu-id="3f585-119">Supporting Precision Time Protocol version 2</span></span>

<span data-ttu-id="3f585-120">Como se mencionó, el objetivo principal de la compatibilidad con la marca de tiempo en Windows es admitir el protocolo de protocolo de tiempo de precisión versión 2 (PTPv2).</span><span class="sxs-lookup"><span data-stu-id="3f585-120">As mentioned, the main goal of timestamping support in Windows is to support the Precision Time Protocol version 2 (PTPv2) protocol.</span></span> <span data-ttu-id="3f585-121">En PTPv2, no todos los mensajes necesitan una marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3f585-121">Within PTPv2, not all messages need a timestamp.</span></span> <span data-ttu-id="3f585-122">En concreto, los mensajes de eventos PTP usan marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3f585-122">In particular, PTP event messages do use timestamps.</span></span> <span data-ttu-id="3f585-123">Actualmente, el ámbito de la compatibilidad es PTPv2 a través del Protocolo de datagramas de usuario (UDP).</span><span class="sxs-lookup"><span data-stu-id="3f585-123">Currently, support is scoped to PTPv2 over User Datagram Protocol (UDP).</span></span> <span data-ttu-id="3f585-124">No se admite PTP a través de Ethernet sin procesar.</span><span class="sxs-lookup"><span data-stu-id="3f585-124">PTP over raw ethernet isn't supported.</span></span>

<span data-ttu-id="3f585-125">La marca de tiempo es compatible con PTPv2 que funciona en *modo de dos* pasos.</span><span class="sxs-lookup"><span data-stu-id="3f585-125">Timestamping is supported for PTPv2 operating in *2 step* mode.</span></span> <span data-ttu-id="3f585-126">*2* paso hace referencia al modo en el que las marcas de tiempo reales de los paquetes PTP no se generan sobre la marcha en el hardware, sino que se recuperan del hardware y se transmiten como mensajes independientes (por ejemplo, mediante un mensaje de seguimiento).</span><span class="sxs-lookup"><span data-stu-id="3f585-126">*2 step* refers to the mode in which the actual timestamps in the PTP packets aren't generated on the fly in the hardware, but are instead retrieved from the hardware and conveyed as separate messages (for example, using a follow-up message).</span></span>

<span data-ttu-id="3f585-127">En resumen, puede usar las API de marca de tiempo de paquetes del asistente de protocolos de Internet (asistente de IP), junto con la compatibilidad con marcas de tiempo de Winsock, en una aplicación PTPv2 para mejorar su precisión de sincronización de hora.</span><span class="sxs-lookup"><span data-stu-id="3f585-127">In summary, you can use the Internet Protocol Helper (IP Helper) packet timestamping APIs, together with Winsock's timestamping support, in a PTPv2 application to improve its time synchronization accuracy.</span></span>

## <a name="retrieving-the-timestamping-capabilities-of-a-network-adapter"></a><span data-ttu-id="3f585-128">Recuperación de las funcionalidades de marca de tiempo de un adaptador de red</span><span class="sxs-lookup"><span data-stu-id="3f585-128">Retrieving the timestamping capabilities of a network adapter</span></span>

<span data-ttu-id="3f585-129">Una aplicación como un servicio de sincronización de hora PTP debe determinar la funcionalidad de marca de tiempo de un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="3f585-129">An application such as a PTP time synchronization service needs to determine the timestamping capability of a network adapter.</span></span> <span data-ttu-id="3f585-130">Con las funcionalidades recuperadas, la aplicación puede decidir si quiere o no usar marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3f585-130">Using the retrieved capabilities, the application can then decide whether or not it wants to use timestamps.</span></span>

<span data-ttu-id="3f585-131">Incluso si un adaptador de red *admite* marcas de tiempo, es necesario mantener desactivada la capacidad de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3f585-131">Even if a network adapter *does* support timestamps, it's required to keep the ability turned off by default.</span></span> <span data-ttu-id="3f585-132">Un adaptador activa la marca de tiempo cuando se le indica que lo haga.</span><span class="sxs-lookup"><span data-stu-id="3f585-132">An adapter turns on timestamping when instructed to do so.</span></span> <span data-ttu-id="3f585-133">Windows proporciona API para que una aplicación recupere la funcionalidad del hardware, así como qué funcionalidades están activadas.</span><span class="sxs-lookup"><span data-stu-id="3f585-133">Windows provides APIs for an application to retrieve the hardware's capability, as well as which capabilities are turned on.</span></span>

<span data-ttu-id="3f585-134">Para recuperar las funcionalidades de marca de tiempo admitidas de un adaptador de red, llame a la función [**GetInterfaceSupportedTimestampCapabilities,**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) proporcionando el identificador único local (LUID) del adaptador de red y, a cambio, recuperando las funcionalidades de marca de tiempo admitidas en forma de [**un objeto INTERFACE_TIMESTAMP_CAPABILITIES.**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities)</span><span class="sxs-lookup"><span data-stu-id="3f585-134">To retrieve the supported timestamp capabilities of a network adapter, you call the [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the supported timestamping capabilities in the form of an [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) object.</span></span>

<span data-ttu-id="3f585-135">El código devuelto por **GetInterfaceSupportedTimestampCapabilities** indica si la llamada se ha  producido correctamente o no, y si se ha recuperado un INTERFACE_TIMESTAMP_CAPABILITIES rellenado.</span><span class="sxs-lookup"><span data-stu-id="3f585-135">The code returned from **GetInterfaceSupportedTimestampCapabilities** indicates whether or not the call succeeded, and whether or not a populated **INTERFACE_TIMESTAMP_CAPABILITIES** value was retrieved.</span></span>

<span data-ttu-id="3f585-136">Para recuperar las funcionalidades de marca de tiempo habilitadas actualmente de un adaptador de red, llame a la función [**GetInterfaceActiveTimestampCapabilities,**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) proporcionando el identificador único local (LUID) del adaptador de red y, a cambio, recuperando las funcionalidades de marca de tiempo habilitadas [**en forma de un objeto INTERFACE_TIMESTAMP_CAPABILITIES.**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities)</span><span class="sxs-lookup"><span data-stu-id="3f585-136">To retrieve the currently enabled timestamp capabilities of a network adapter, you call the [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the enabled timestamping capabilities in the form of an [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) object.</span></span>

<span data-ttu-id="3f585-137">De nuevo, el código devuelto por **GetInterfaceActiveTimestampCapabilities** indica que  se ha producido correctamente o no, y si se ha recuperado un valor INTERFACE_TIMESTAMP_CAPABILITIES válido.</span><span class="sxs-lookup"><span data-stu-id="3f585-137">Again, the code returned from **GetInterfaceActiveTimestampCapabilities** indicates success or failure, and whether or not a valid **INTERFACE_TIMESTAMP_CAPABILITIES** value was retrieved.</span></span>

<span data-ttu-id="3f585-138">Los adaptadores de red pueden admitir una variedad de funcionalidades de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3f585-138">Network adapters can support a variety of timestamping capabilities.</span></span> <span data-ttu-id="3f585-139">Por ejemplo, algunos adaptadores pueden crear marcas de tiempo de cada paquete durante el envío y la recepción, mientras que otros solo admiten paquetes PTPv2.</span><span class="sxs-lookup"><span data-stu-id="3f585-139">For example, some adapters can timestamp every packet during send and receive, while others support only PTPv2 packets.</span></span> <span data-ttu-id="3f585-140">La [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) describe las funcionalidades exactas que admite un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="3f585-140">The [**INTERFACE_TIMESTAMP_CAPABILITIES**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_timestamp_capabilities) structure describes the exact capabilities that a network adapter supports.</span></span>

## <a name="retrieving-cross-timestamps-from-a-network-adapter"></a><span data-ttu-id="3f585-141">Recuperación de marcas de tiempo cruzadas desde un adaptador de red</span><span class="sxs-lookup"><span data-stu-id="3f585-141">Retrieving cross timestamps from a network adapter</span></span>

<span data-ttu-id="3f585-142">Cuando se usan marcas de tiempo de hardware, una aplicación PTP debe establecer una relación (por ejemplo, mediante técnicas matemáticas adecuadas) entre el reloj de hardware del adaptador de red y un reloj del sistema.</span><span class="sxs-lookup"><span data-stu-id="3f585-142">When using hardware timestamps, a PTP application needs to establish a relation (for example, by using appropriate mathematical techniques) between the hardware clock of the network adapter and a system clock.</span></span> <span data-ttu-id="3f585-143">Esto es necesario para que un valor que representa una hora de la unidad de un reloj se pueda convertir en la unidad de otro reloj.</span><span class="sxs-lookup"><span data-stu-id="3f585-143">This is necessary so that a value representing a time in one clock's unit can be converted into another clock's unit.</span></span> <span data-ttu-id="3f585-144">Las marcas de tiempo cruzadas se proporcionan para este propósito y la aplicación puede muestrear marcas de tiempo cruzadas periódicamente para establecer dicha relación.</span><span class="sxs-lookup"><span data-stu-id="3f585-144">Cross timestamps are provided for this purpose, and your application can sample cross timestamps periodically in order to establish such a relation.</span></span>

<span data-ttu-id="3f585-145">Para ello, llame a la función [**CaptureInterfaceHardwareCrossTimestamp,**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) proporcionando el identificador único local (LUID) del adaptador de red y, a cambio, recuperando la marca de tiempo del adaptador de red en forma de [**un objeto INTERFACE_HARDWARE_CROSSTIMESTAMP.**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp)</span><span class="sxs-lookup"><span data-stu-id="3f585-145">To do that, call the [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) function, providing the locally unique identifier (LUID) of the network adapter, and in return retrieving the timestamp from the network adapter in the form of an [**INTERFACE_HARDWARE_CROSSTIMESTAMP**](/windows/win32/api/iphlpapi/ns-iphlpapi-interface_hardware_crosstimestamp) object.</span></span>

## <a name="timestamp-capability-change-notifications"></a><span data-ttu-id="3f585-146">Notificaciones de cambio de funcionalidad de marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="3f585-146">Timestamp capability change notifications</span></span>

<span data-ttu-id="3f585-147">Para recibir una notificación si cambian las funciones de marca de tiempo de un adaptador de red, llame a la función [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange) y proporcione un puntero a la función de devolución de llamada que ha implementado, junto con un contexto opcional asignado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3f585-147">To be notified should the timestamp capabilities for a network adapter change, call the [**RegisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-registerinterfacetimestampconfigchange) function, providing a pointer to the callback function that you've implemented, together with an optional caller-allocated context.</span></span>

<span data-ttu-id="3f585-148">**RegisterInterfaceTimestampConfigChange** devuelve un identificador que puede pasar posteriormente a [**UnregisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange) para anular el registro de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3f585-148">**RegisterInterfaceTimestampConfigChange** returns a handle that you can subsequently pass to [**UnregisterInterfaceTimestampConfigChange**](/windows/win32/api/iphlpapi/nf-iphlpapi-unregisterinterfacetimestampconfigchange) in order to unregister your callback function.</span></span>

## <a name="code-example-1mdashretrieving-timestamp-capabilities-and-cross-timestamps"></a><span data-ttu-id="3f585-149">Ejemplo de código 1: &mdash; recuperación de funcionalidades de marca de tiempo y marcas de tiempo cruzadas</span><span class="sxs-lookup"><span data-stu-id="3f585-149">Code example 1&mdash;retrieving timestamp capabilities and cross timestamps</span></span>

```c
// main.cpp in a Console App project.

#include <stdio.h>
#include <winsock2.h>
#include <iphlpapi.h>
#pragma comment(lib, "Iphlpapi")

BOOL
IsPTPv2HardwareTimestampingSupportedForIPv4(PINTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities)
{
    // Supported if both receive and transmit side support is present
    if (((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4EventMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4AllMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.AllReceive))
         &&
        ((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4EventMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv4AllMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.TaggedTransmit) ||
         (timestampCapabilities->HardwareCapabilities.AllTransmit)))
    {
        return TRUE;
    }

    return FALSE;
}

BOOL
IsPTPv2HardwareTimestampingSupportedForIPv6(PINTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities)
{
    // Supported if both receive and transmit side support is present
    if (((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6EventMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6AllMessageReceive) ||
         (timestampCapabilities->HardwareCapabilities.AllReceive))
         &&
        ((timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6EventMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.PtpV2OverUdpIPv6AllMessageTransmit) ||
         (timestampCapabilities->HardwareCapabilities.TaggedTransmit) ||
         (timestampCapabilities->HardwareCapabilities.AllTransmit)))
    {
        return TRUE;
    }

    return FALSE;
}

enum SupportedTimestampType
{
    TimestampTypeNone = 0,
    TimestampTypeSoftware = 1,
    TimestampTypeHardware = 2
};

// This function checks and returns the supported timestamp capabilities for an interface for
// a PTPv2 application
SupportedTimestampType
CheckActiveTimestampCapabilitiesForPtpv2(NET_LUID interfaceLuid)
{
    DWORD result = NO_ERROR;
    INTERFACE_TIMESTAMP_CAPABILITIES timestampCapabilities;
    SupportedTimestampType supportedType = TimestampTypeNone;

    result = GetInterfaceActiveTimestampCapabilities(
                 &interfaceLuid,
                 &timestampCapabilities);
    if (result != NO_ERROR)
    {
        printf("Error retrieving hardware timestamp capabilities: %d\n", result);
        goto Exit;
    }

    if (IsPTPv2HardwareTimestampingSupportedForIPv4(&timestampCapabilities) &&
        IsPTPv2HardwareTimestampingSupportedForIPv6(&timestampCapabilities))
    {
        supportedType = TimestampTypeHardware;
        goto Exit;
    }
    else
    {
        if ((timestampCapabilities.SoftwareCapabilities.AllReceive) &&
            ((timestampCapabilities.SoftwareCapabilities.AllTransmit) ||
             (timestampCapabilities.SoftwareCapabilities.TaggedTransmit)))
        {
            supportedType = TimestampTypeSoftware;
        }
    }

Exit:
    return supportedType;
}

// Helper function which does the correlation between hardware and system clock
// using mathematical techniques
void ComputeCorrelationOfHardwareAndSystemTimestamps(INTERFACE_HARDWARE_CROSSTIMESTAMP *crossTimestamp);

// An application would call this function periodically to gather a set 
// of matching timestamps for use in converting hardware timestamps to
// system timestamps
DWORD
RetrieveAndProcessCrossTimestamp(NET_LUID interfaceLuid)
{
    DWORD result = NO_ERROR;
    INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp;

    result = CaptureInterfaceHardwareCrossTimestamp(
                 &interfaceLuid,
                 &crossTimestamp);
    if (result != NO_ERROR)
    {
        printf("Error retrieving cross timestamp for the interface: %d\n", result);
        goto Exit;
    }

    // Process crossTimestamp further to create a relation between the hardware clock
    // of the NIC and the QPC values using appropriate mathematical techniques
    ComputeCorrelationOfHardwareAndSystemTimestamps(&crossTimestamp);

Exit:
    return result;
}

int main()
{
}
```

## <a name="code-example-2mdashregistering-for-timestamp-capability-change-notifications"></a><span data-ttu-id="3f585-150">Ejemplo de código &mdash; 2: registro para notificaciones de cambio de funcionalidad de marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="3f585-150">Code example 2&mdash;registering for timestamp capability change notifications</span></span>

<span data-ttu-id="3f585-151">En este ejemplo se muestra cómo la aplicación podría usar marcas de tiempo de un extremo a otro.</span><span class="sxs-lookup"><span data-stu-id="3f585-151">This example shows how your application could use timestamps end to end.</span></span>

```c
// main.cpp in a Console App project.

#include <stdlib.h>
#include <stdio.h>
#include <winsock2.h>
#include <mswsock.h>
#include <iphlpapi.h>
#include <mstcpip.h>
#pragma comment(lib, "Ws2_32")
#pragma comment(lib, "Iphlpapi")

// Globals and function declarations used by the application.
// The sample functions and skeletons demonstrate:
// - Checking timestamp configuration for an interface to determine if timestamping can be used
// - If timestamping is enabled, starts tracking changes in timestamp configuration
// - Performing correlation between hardware and system timestamps using cross timestamps
//   on a separate thread depending on the timestamp type configured
// - Receiving a packet and computing the latency between when the timestamp
//   was generated on packet reception, and when the packet was received by
//   the application through the socket
// The sample tries to demonstrate how an application could use timestamps. It is not thread safe 
// and does not do exhaustive error checking.
// Lot of the functions are provided as skeletons, or only declared and invoked
// but are not defined. It is up to
// the application to implement these suitably.

// An application could use the functions below by e.g.
// - Call InitializeTimestampingForInterface for the interface it wants to track for timestamping capability.
// - Call EstimateReceiveLatency to estimate the receive latency of a packet depending on the timestamp 
//   type configured for the interface.

enum SupportedTimestampType
{
    TimestampTypeNone = 0,
    TimestampTypeSoftware = 1,
    TimestampTypeHardware = 2
};

// interfaceBeingTracked is the interface the PTPv2 application
// intends to use for timestamping purpose.
wchar_t* interfaceBeingTracked;

// The active timestamping type determined for
// interfaceBeingTracked.
SupportedTimestampType timestampTypeEnabledForInterface;

HANDLE correlationThread;
HANDLE threadStopEvent;
HIFTIMESTAMPCHANGE TimestampChangeNotificationHandle = NULL;

// Function from sample above to check if an interface supports timestamping for PTPv2.
SupportedTimestampType CheckActiveTimestampCapabilitiesForPtpv2(NET_LUID interfaceLuid);

// Function from sample above to retrieve cross timestamps and process them further.
DWORD RetrieveAndProcessCrossTimestamp(NET_LUID interfaceLuid);

// Helper function which registers for timestamp configuration changes.
DWORD RegisterTimestampChangeNotifications();

// Callback function which is invoked when timestamp configuration changes
// for some network interface.
INTERFACE_TIMESTAMP_CONFIG_CHANGE_CALLBACK TimestampConfigChangeCallback;

// Function which does the correlation between hardware and system clock
// using mathematical techniques. It is periodically invoked and provided
// a sample of cross timestamp to compute a correlation.
void ComputeCorrelationOfHardwareAndSystemTimestamps(INTERFACE_HARDWARE_CROSSTIMESTAMP *crossTimestamp);

// Helper function which converts a hardware timestamp from the NIC clock
// to system timestamp (QPC) values. It is assumed that this works together
// with the ComputeCorrelationOfHardwareAndSystemTimestamps function
// to derive the correlation.
ULONG64 ConvertHardwareTimestampToQpc(ULONG64 HardwareTimestamp);

// Start function of thread which periodically samples
// cross timestamps to correlate hardware and software timestamps.
DWORD WINAPI CorrelateHardwareAndSystemTimestamps(LPVOID);

// Helper function which starts a new thread at CorrelateHardwareAndSystemTimestamps.
DWORD StartCorrelatingHardwareAndSytemTimestamps();

// Helper function which restarts correlation when some change is detected.
DWORD RestartCorrelatingHardwareAndSystemTimestamps();

// Stops the correlation thread.
DWORD StopCorrelatingHardwareAndSystemTimestamps();

DWORD
FindInterfaceFromFriendlyName(wchar_t* friendlyName, NET_LUID* interfaceLuid)
{
    DWORD result = 0;
    ULONG flags = 0;
    ULONG outBufLen = 0;
    PIP_ADAPTER_ADDRESSES pAddresses = NULL;
    PIP_ADAPTER_ADDRESSES currentAddresses = NULL;

    result = GetAdaptersAddresses(0,
        flags,
        NULL,
        pAddresses,
        &outBufLen);
    if (result == ERROR_BUFFER_OVERFLOW)
    {
        pAddresses = (PIP_ADAPTER_ADDRESSES)malloc(outBufLen);

        result = GetAdaptersAddresses(0,
            flags,
            NULL,
            pAddresses,
            &outBufLen);
        if (result != NO_ERROR)
        {
            goto Done;
        }
    }
    else if (result != NO_ERROR)
    {
        goto Done;
    }

    currentAddresses = pAddresses;
    while (currentAddresses != NULL)
    {
        if (wcscmp(friendlyName, currentAddresses->FriendlyName) == 0)
        {
            result = ConvertInterfaceIndexToLuid(currentAddresses->IfIndex, interfaceLuid);
            goto Done;
        }

        currentAddresses = currentAddresses->Next;
    }

    result = ERROR_NOT_FOUND;

Done:

    if (pAddresses != NULL)
    {
        free(pAddresses);
    }

    return result;
}

// This function checks if an interface is suitable for
// timestamping for PTPv2. If so, it registers for timestamp
// configuration changes and initializes some globals.
// If hardware  timestamping is enabled it also starts
// correlation thread.
DWORD
InitializeTimestampingForInterface(wchar_t* friendlyName)
{
    DWORD error;
    SupportedTimestampType supportedType = TimestampTypeNone;

    NET_LUID interfaceLuid;

    error = FindInterfaceFromFriendlyName(friendlyName, &interfaceLuid);
    if (error != 0)
    {
        return error;
    }

    supportedType = CheckActiveTimestampCapabilitiesForPtpv2(interfaceLuid);

    if (supportedType != TimestampTypeNone)
    {
        error = RegisterTimestampChangeNotifications();
        if (error != NO_ERROR)
        {
            return error;
        }

        if (supportedType == TimestampTypeHardware)
        {
            threadStopEvent = CreateEvent(
                NULL,
                FALSE,
                FALSE,
                NULL
            );
            if (threadStopEvent == NULL)
            {
                return GetLastError();
            }            

            error = StartCorrelatingHardwareAndSytemTimestamps();
            if (error != 0)
            {
                return error;
            }
        }

        interfaceBeingTracked = friendlyName;
        timestampTypeEnabledForInterface = supportedType;

        return error;
    }

    return ERROR_NOT_SUPPORTED;
}

DWORD
RegisterTimestampChangeNotifications()
{
    DWORD retcode = NO_ERROR;

    // Register with NULL context
    retcode = RegisterInterfaceTimestampConfigChange(TimestampConfigChangeCallback, NULL, &TimestampChangeNotificationHandle);
    if (retcode != NO_ERROR)
    {
        printf("Error when calling RegisterIfTimestampConfigChange %d\n", retcode);
    }

    return retcode;
}

// The callback invoked when change in some interface’s timestamping configuration
// happens. The callback takes appropriate action based on the new capability of the
// interface. The callback assumes that there is only 1 NIC. If multiple NICs are being
// tracked for timestamping then the application would need to check all of them.
VOID
WINAPI
TimestampConfigChangeCallback(
    _In_ PVOID /*CallerContext*/
    )
{
    SupportedTimestampType supportedType;

    NET_LUID interfaceLuid;
    DWORD error;

    error = FindInterfaceFromFriendlyName(interfaceBeingTracked, &interfaceLuid);
    if (error != NO_ERROR)
    {
        if (timestampTypeEnabledForInterface == TimestampTypeHardware)
        {
            StopCorrelatingHardwareAndSystemTimestamps();
            timestampTypeEnabledForInterface = TimestampTypeNone;
        }
        return;
    }

    supportedType = CheckActiveTimestampCapabilitiesForPtpv2(interfaceLuid);

    if ((supportedType == TimestampTypeHardware) &&
        (timestampTypeEnabledForInterface == TimestampTypeHardware))
    {
        // NIC could have been restarted, restart the correlation between hardware and 
        // system timestamps.
        RestartCorrelatingHardwareAndSystemTimestamps();
    }
    else if (supportedType == TimestampTypeHardware)
    {
        // Start thread correlating hardware and software timestamps
        StartCorrelatingHardwareAndSytemTimestamps();
    }
    else if (supportedType != TimestampTypeHardware)
    {
        // Hardware timestamps are not enabled, stop correlation
        StopCorrelatingHardwareAndSystemTimestamps();
    }

    timestampTypeEnabledForInterface = supportedType;
}

DWORD 
StartCorrelatingHardwareAndSytemTimestamps()
{
    // Create a new thread which starts at CorrelateHardwareAndSoftwareTimestamps
    correlationThread = CreateThread(
        NULL,
        0,
        CorrelateHardwareAndSystemTimestamps,
        NULL,
        0,
        NULL); 

    if (correlationThread == NULL)
    {
        return GetLastError();
    }
}

// Thread which periodically invokes functions to 
// sample cross timestamps and use them to compute
// correlation between hardware and system timestamps.
DWORD WINAPI
CorrelateHardwareAndSystemTimestamps(LPVOID /*lpParameter*/)
{
    DWORD error;
    NET_LUID interfaceLuid;
    DWORD result;

    result = FindInterfaceFromFriendlyName(interfaceBeingTracked, &interfaceLuid);
    if (result != 0)
    {
        return result;
    }

    while (TRUE)
    {
        error = RetrieveAndProcessCrossTimestamp(interfaceLuid);

        // Sleep and repeat till the thread gets a signal to stop
        result = WaitForSingleObject(threadStopEvent, 5000);
        if (result != WAIT_TIMEOUT)
        {
            if (result == WAIT_OBJECT_0)
            {
                return 0;
            }
            else if (result == WAIT_FAILED)            
            {
                return GetLastError();
            }

            return result;
        }
    }
}

DWORD
StopCorrelatingHardwareAndSystemTimestamps()
{
    SetEvent(threadStopEvent);
    return 0;
}

// Function which receives a packet and estimates the latency between the 
// point at which receive timestamp (of appropriate type) was generated
// and when the packet was received in the app through the socket.
// The sample assumes that there is only 1 NIC in the system. This is the NIC which is tracked through
// interfaceBeingTracked for correlation purpose, and through which packets are being
// received by the socket.
// The recvmsg parameter is of type LPFN_WSARECVMSG and an application can
// retrieve it by issuing WSAIoctl
// with SIO_GET_EXTENSION_FUNCTION_POINTER control
// and WSAID_WSARECVMSG. Please refer to msdn.
void EstimateReceiveLatency(SOCKET sock, LPFN_WSARECVMSG recvmsg)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT64))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    UINT64 socketTimestamp = 0;
    ULONG64 appLevelTimestamp;
    ULONG64 packetReceivedTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = NULL;
    wsaMsg.namelen = 0;
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure rx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.Flags |= TIMESTAMPING_FLAG_RX;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR)
    {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR)
    {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    if (timestampTypeEnabledForInterface != TimestampTypeNone)
    {
        // Capture system timestamp (QPC) upon message reception.
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;

        printf("received packet\n");

        // Look for socket rx timestamp returned via control message.
        BOOLEAN retrievedTimestamp = FALSE;
        PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
        while (cmsg != NULL)
        {
            if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP)
            {
                socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
                retrievedTimestamp = TRUE;
                break;
            }
            cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
        }

        if (retrievedTimestamp)
        {
            // Compute socket receive path latency.
            LARGE_INTEGER clockFrequency;
            ULONG64 elapsedMicroseconds;

            if (timestampTypeEnabledForInterface == TimestampTypeHardware)
            {
                packetReceivedTimestamp = ConvertHardwareTimestampToQpc(socketTimestamp);
            }
            else
            {
                packetReceivedTimestamp = socketTimestamp;
            }
        
            QueryPerformanceFrequency(&clockFrequency);

            // Compute socket receive path latency.
            elapsedMicroseconds = appLevelTimestamp - packetReceivedTimestamp;
            elapsedMicroseconds *= 1000000;
            elapsedMicroseconds /= clockFrequency.QuadPart;
            printf("RX latency estimation: %lld microseconds\n",
                 elapsedMicroseconds);
        }
        else
        {
            printf("failed to retrieve RX timestamp\n");
        }
    }
}

int main()
{
}
```
