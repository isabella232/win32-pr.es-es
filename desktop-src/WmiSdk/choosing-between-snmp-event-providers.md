---
description: Los proveedores de eventos SNMP reciben paquetes de eventos SNMP de la pila WINSNMP y traducen la información incluida en los paquetes en eventos de WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Elección entre proveedores de eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716623"
---
# <a name="choosing-between-snmp-event-providers"></a><span data-ttu-id="5867e-103">Elección entre proveedores de eventos SNMP</span><span class="sxs-lookup"><span data-stu-id="5867e-103">Choosing Between SNMP Event Providers</span></span>

<span data-ttu-id="5867e-104">Los proveedores de eventos SNMP reciben paquetes de eventos SNMP de la pila WINSNMP y traducen la información incluida en los paquetes en eventos de WMI.</span><span class="sxs-lookup"><span data-stu-id="5867e-104">SNMP event providers receive SNMP event packets from the WINSNMP stack and translate the information included in the packets into WMI events.</span></span>

<span data-ttu-id="5867e-105">WMI incluye los dos proveedores de eventos SNMP siguientes:</span><span class="sxs-lookup"><span data-stu-id="5867e-105">WMI includes the following two SNMP event providers:</span></span>

-   <span data-ttu-id="5867e-106">Proveedor de eventos encapsulados SNMP (SEEP)</span><span class="sxs-lookup"><span data-stu-id="5867e-106">SNMP Encapsulated Event provider (SEEP)</span></span>

    <span data-ttu-id="5867e-107">La aprovisionamiento encapsulado significa que la instancia de evento tiene propiedades simples que describen la información asignada directamente desde la captura de SNMP.</span><span class="sxs-lookup"><span data-stu-id="5867e-107">Encapsulated provision means that the event instance has simple properties describing the information mapped directly from the SNMP trap.</span></span>

-   <span data-ttu-id="5867e-108">Proveedor de eventos de SNMP referente (SREP)</span><span class="sxs-lookup"><span data-stu-id="5867e-108">SNMP Referent Event provider (SREP)</span></span>

    <span data-ttu-id="5867e-109">El aprovisionamiento referente abstrae la información presente dentro de la captura de SNMP para que las propiedades que comparten la misma clase e instancia se presenten como objetos incrustados.</span><span class="sxs-lookup"><span data-stu-id="5867e-109">Referent provision abstracts the information present within the SNMP trap so that properties which share the same class and instance are presented as embedded objects.</span></span> <span data-ttu-id="5867e-110">Esto permite que la instancia única, a la que está asociada la captura, se recupere después de la recepción del evento, mediante SNMP \_ \_ RELPATH.</span><span class="sxs-lookup"><span data-stu-id="5867e-110">This allows for the unique instance, with which the trap is associated, to be retrieved after the receipt of the event, using the SNMP \_\_RELPATH.</span></span>

> [!Note]  
> <span data-ttu-id="5867e-111">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="5867e-111">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="5867e-112">Independientemente de si el evento SNMP es una captura de SNMPv1 o una notificación de SNMPv2C, la pila lo notifica como una notificación de SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="5867e-112">Regardless of whether the SNMP event is an SNMPv1 trap or an SNMPv2C notification, the stack reports it as an SNMPv2 notification.</span></span> <span data-ttu-id="5867e-113">Por lo tanto, los proveedores de eventos procesan todos los eventos SNMP como notificaciones de SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="5867e-113">Therefore, the event providers process all SNMP events as SNMPv2 notifications.</span></span>

<span data-ttu-id="5867e-114">Para describir los eventos SNMP a los consumidores de WMI, cada proveedor de eventos admite una jerarquía de clases que deriva de la clase del sistema [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) .</span><span class="sxs-lookup"><span data-stu-id="5867e-114">To describe the SNMP events to WMI consumers, each event provider supports a hierarchy of classes that derives from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) system class.</span></span> <span data-ttu-id="5867e-115">La clase [SNMPNotification](snmpnotification.md) es la clase principal de la jerarquía SEEP; la clase [SNMPExtendedNotification](snmpextendednotification.md) es la clase principal de la jerarquía SREP.</span><span class="sxs-lookup"><span data-stu-id="5867e-115">The [SNMPNotification](snmpnotification.md) class is the parent class for the SEEP hierarchy; the [SNMPExtendedNotification](snmpextendednotification.md) class is the parent class for the SREP hierarchy.</span></span>

 

 



