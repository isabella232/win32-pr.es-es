---
title: Administración de capturas y notificaciones
description: La aplicación WinSNMP debe registrarse para recibir capturas y notificaciones mediante una llamada a la función SnmpRegister con SNMPAPI \_ en. La aplicación puede anular el registro y deshabilitar las capturas y notificaciones mediante una llamada a la función con SNMPAPI \_ OFF.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903718"
---
# <a name="managing-traps-and-notifications"></a><span data-ttu-id="9f392-104">Administración de capturas y notificaciones</span><span class="sxs-lookup"><span data-stu-id="9f392-104">Managing Traps and Notifications</span></span>

<span data-ttu-id="9f392-105">La aplicación WinSNMP debe registrarse para recibir capturas y notificaciones mediante una llamada a la función [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) con snmpapi \_ en.</span><span class="sxs-lookup"><span data-stu-id="9f392-105">The WinSNMP application must register to receive traps and notifications by calling the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) function with SNMPAPI\_ON.</span></span> <span data-ttu-id="9f392-106">La aplicación puede anular el registro y deshabilitar las capturas y notificaciones mediante una llamada a la función con SNMPAPI \_ OFF.</span><span class="sxs-lookup"><span data-stu-id="9f392-106">The application can unregister and disable traps and notifications by calling the function with SNMPAPI\_OFF.</span></span>

<span data-ttu-id="9f392-107">Hay varias opciones disponibles cuando la aplicación llama a **SnmpRegister**.</span><span class="sxs-lookup"><span data-stu-id="9f392-107">Several options are available when the application calls **SnmpRegister**.</span></span> <span data-ttu-id="9f392-108">La aplicación se puede registrar o anular el registro para las siguientes capturas y notificaciones:</span><span class="sxs-lookup"><span data-stu-id="9f392-108">The application can register or unregister for the following traps and notifications:</span></span>

-   <span data-ttu-id="9f392-109">Un tipo de captura o notificación</span><span class="sxs-lookup"><span data-stu-id="9f392-109">One type of trap or notification</span></span>
-   <span data-ttu-id="9f392-110">Todas las capturas y notificaciones</span><span class="sxs-lookup"><span data-stu-id="9f392-110">All traps and notifications</span></span>
-   <span data-ttu-id="9f392-111">Todos los orígenes de solicitudes de captura y notificación</span><span class="sxs-lookup"><span data-stu-id="9f392-111">All sources of trap and notification requests</span></span>
-   <span data-ttu-id="9f392-112">Capturas y notificaciones de todas las entidades de administración</span><span class="sxs-lookup"><span data-stu-id="9f392-112">Traps and notifications from all management entities</span></span>
-   <span data-ttu-id="9f392-113">Capturas y notificaciones para todos los contextos</span><span class="sxs-lookup"><span data-stu-id="9f392-113">Traps and notifications for every context</span></span>

<span data-ttu-id="9f392-114">Para registrar y recibir un tipo de notificación o de captura predefinido, la aplicación debe definir un identificador de objeto (una estructura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ) para cada tipo predefinido.</span><span class="sxs-lookup"><span data-stu-id="9f392-114">To register and receive a predefined trap or notification type, the application must define an object identifier (an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure) for each predefined type.</span></span> <span data-ttu-id="9f392-115">La estructura debe contener una secuencia de coincidencia de patrones para el tipo de captura o notificación.</span><span class="sxs-lookup"><span data-stu-id="9f392-115">The structure must contain a pattern-matching sequence for the type of trap or notification.</span></span> <span data-ttu-id="9f392-116">RFC 1907, "base de información de administración para la versión 2 del Protocolo simple de administración de redes (SNMPv2)", define los identificadores de objetos de captura y notificación.</span><span class="sxs-lookup"><span data-stu-id="9f392-116">RFC 1907, "Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)," defines trap and notification object identifiers.</span></span>

<span data-ttu-id="9f392-117">Para recuperar los datos de captura pendientes y las notificaciones de una sesión WinSNMP, una aplicación WinSNMP debe llamar a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) con el identificador de sesión devuelto por la función [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .</span><span class="sxs-lookup"><span data-stu-id="9f392-117">To retrieve outstanding trap data and notifications for a WinSNMP session, a WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function with the session handle returned by the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span>

<span data-ttu-id="9f392-118">Para obtener más información, consulte [envío de mensajes SNMP](sending-snmp-messages.md) y [recepción de mensajes SNMP](receiving-snmp-messages.md).</span><span class="sxs-lookup"><span data-stu-id="9f392-118">For more information, see [Sending SNMP Messages](sending-snmp-messages.md) and [Receiving SNMP Messages](receiving-snmp-messages.md).</span></span> <span data-ttu-id="9f392-119">Para obtener información adicional acerca de la asignación y desasignación de recursos para capturas y notificaciones, consulte [asignación de objetos de memoria WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9f392-119">For additional information about allocation and deallocation of resources for traps and notifications, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




