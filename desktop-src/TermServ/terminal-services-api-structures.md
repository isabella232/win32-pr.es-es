---
title: Servicios de Escritorio remoto estructuras de API
description: Muestra las estructuras que se usan con Servicios de Escritorio remoto API.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fb8de65f7f234f85eb8071cc66743c9c26cc9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149298"
---
# <a name="remote-desktop-services-api-structures"></a><span data-ttu-id="99446-103">Servicios de Escritorio remoto estructuras de API</span><span class="sxs-lookup"><span data-stu-id="99446-103">Remote Desktop Services API Structures</span></span>

<span data-ttu-id="99446-104">Las siguientes estructuras se usan con la API de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="99446-104">The following structures are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="99446-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="99446-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="99446-106">**DEF. de canal \_**</span><span class="sxs-lookup"><span data-stu-id="99446-106">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

<span data-ttu-id="99446-107">Contiene el nombre y las opciones de un canal virtual Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="99446-107">Contains the name and options of a Remote Desktop Services virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-108">**\_puntos de entrada de canal \_**</span><span class="sxs-lookup"><span data-stu-id="99446-108">**CHANNEL\_ENTRY\_POINTS**</span></span>](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

<span data-ttu-id="99446-109">Contiene punteros a las funciones a las que llama un archivo DLL del lado cliente para tener acceso a los canales virtuales.</span><span class="sxs-lookup"><span data-stu-id="99446-109">Contains pointers to the functions called by a client-side DLL to access virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-110">**\_encabezado de PDU de canal \_**</span><span class="sxs-lookup"><span data-stu-id="99446-110">**CHANNEL\_PDU\_HEADER**</span></span>](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

<span data-ttu-id="99446-111">Contiene información sobre un bloque de datos que recibe el servidor de un canal virtual.</span><span class="sxs-lookup"><span data-stu-id="99446-111">Contains information about a data block being received by the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-112">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="99446-112">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dd>

<span data-ttu-id="99446-113">Contiene información sobre un paquete de claves de licencias de Servicios de Escritorio remoto específico.</span><span class="sxs-lookup"><span data-stu-id="99446-113">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-114">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="99446-114">**LSLicense**</span></span>](lslicense.md)
</dt> <dd>

<span data-ttu-id="99446-115">Contiene información acerca de una licencia de Servicios de Escritorio remoto específica.</span><span class="sxs-lookup"><span data-stu-id="99446-115">Contains information about a specific Remote Desktop Services license.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-116">**WTSCLIENT**</span><span class="sxs-lookup"><span data-stu-id="99446-116">**WTSCLIENT**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

<span data-ttu-id="99446-117">Contiene información sobre un cliente de Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="99446-117">Contains information about a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-118">**WTSCONFIGINFO**</span><span class="sxs-lookup"><span data-stu-id="99446-118">**WTSCONFIGINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

<span data-ttu-id="99446-119">Contiene información sobre una sesión de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="99446-119">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-120">**WTSINFO**</span><span class="sxs-lookup"><span data-stu-id="99446-120">**WTSINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

<span data-ttu-id="99446-121">Contiene información sobre una sesión de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="99446-121">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-122">**WTSINFOEX**</span><span class="sxs-lookup"><span data-stu-id="99446-122">**WTSINFOEX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

<span data-ttu-id="99446-123">Contiene una Unión de [**\_ nivel WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) que contiene información extendida sobre una sesión de servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="99446-123">Contains a [**WTSINFOEX\_LEVEL**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) union that contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-124">**WTSINFOEX \_ Level1**</span><span class="sxs-lookup"><span data-stu-id="99446-124">**WTSINFOEX\_LEVEL1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

<span data-ttu-id="99446-125">Contiene información extendida sobre una sesión de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="99446-125">Contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-126">**WTSLISTENERCONFIG**</span><span class="sxs-lookup"><span data-stu-id="99446-126">**WTSLISTENERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

<span data-ttu-id="99446-127">Contiene información sobre un agente de escucha de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="99446-127">Contains information about a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-128">**\_dirección IP de WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="99446-128">**WTSSBX\_IP\_ADDRESS**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

<span data-ttu-id="99446-129">Contiene información acerca de la dirección IP de un recurso de red.</span><span class="sxs-lookup"><span data-stu-id="99446-129">Contains information about the IP address of a network resource.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-130">**información de conexión a la \_ máquina WTSSBX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99446-130">**WTSSBX\_MACHINE\_CONNECT\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

<span data-ttu-id="99446-131">Contiene información acerca de un equipo que acepta conexiones remotas.</span><span class="sxs-lookup"><span data-stu-id="99446-131">Contains information about a computer that is accepting remote connections.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-132">**información de la \_ máquina WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="99446-132">**WTSSBX\_MACHINE\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

<span data-ttu-id="99446-133">Contiene información acerca de un equipo y su estado actual.</span><span class="sxs-lookup"><span data-stu-id="99446-133">Contains information about a computer and its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-134">**\_información de sesión de WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="99446-134">**WTSSBX\_SESSION\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

<span data-ttu-id="99446-135">Contiene información sobre las sesiones que están disponibles para el agente de Conexión a Escritorio remoto (agente de conexión a escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="99446-135">Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="99446-136">**\_notificación WTSSESSION**</span><span class="sxs-lookup"><span data-stu-id="99446-136">**WTSSESSION\_NOTIFICATION**</span></span>](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

<span data-ttu-id="99446-137">Proporciona información sobre la notificación de cambio de sesión.</span><span class="sxs-lookup"><span data-stu-id="99446-137">Provides information about the session change notification.</span></span> <span data-ttu-id="99446-138">Un servicio recibe esta estructura en su función [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) en respuesta a un evento de cambio de sesión.</span><span class="sxs-lookup"><span data-stu-id="99446-138">A service receives this structure in its [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function in response to a session change event.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-139">**WTSUSERCONFIG**</span><span class="sxs-lookup"><span data-stu-id="99446-139">**WTSUSERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

<span data-ttu-id="99446-140">Contiene información de configuración para un usuario en un controlador de dominio o un servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="99446-140">Contains configuration information for a user on a domain controller or Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-141">**\_dirección de cliente de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="99446-141">**WTS\_CLIENT\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

<span data-ttu-id="99446-142">Contiene la dirección de red de cliente de una sesión de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="99446-142">Contains the client network address of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-143">**\_pantalla de cliente de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="99446-143">**WTS\_CLIENT\_DISPLAY**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

<span data-ttu-id="99446-144">Contiene información acerca de la presentación de un cliente de Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="99446-144">Contains information about the display of a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-145">**\_información del proceso de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="99446-145">**WTS\_PROCESS\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

<span data-ttu-id="99446-146">Contiene información sobre un proceso que se ejecuta en un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="99446-146">Contains information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-147">**información del proceso de WTS \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="99446-147">**WTS\_PROCESS\_INFO\_EX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

<span data-ttu-id="99446-148">Contiene información extendida sobre un proceso que se ejecuta en un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="99446-148">Contains extended information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="99446-149">[**\_información del producto de WTS \_**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="99446-149">[**WTS\_PRODUCT\_INFO**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span></span>
</dt> <dd>

<span data-ttu-id="99446-150">Los detalles de la licencia de producto necesarios para conectarse a un servidor de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="99446-150">The details of the product license that is required to connect to a terminal server.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-151">**\_información del servidor de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="99446-151">**WTS\_SERVER\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

<span data-ttu-id="99446-152">Contiene información acerca de un servidor de Servicios de Escritorio remoto específico.</span><span class="sxs-lookup"><span data-stu-id="99446-152">Contains information about a specific Remote Desktop Services server.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-153">**\_dirección de sesión de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="99446-153">**WTS\_SESSION\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

<span data-ttu-id="99446-154">Contiene la dirección IP virtual asignada a una sesión.</span><span class="sxs-lookup"><span data-stu-id="99446-154">Contains the virtual IP address assigned to a session.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-155">**\_información de sesión de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="99446-155">**WTS\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

<span data-ttu-id="99446-156">Contiene información sobre una sesión de cliente en un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="99446-156">Contains information about a client session on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="99446-157">**Información de sesión de WTS \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="99446-157">**WTS\_SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

<span data-ttu-id="99446-158">Contiene información extendida sobre una sesión de cliente en un servidor host de sesión de escritorio remoto o en un servidor de Host de virtualización de Escritorio remoto (host de virtualización de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="99446-158">Contains extended information about a client session on a RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> </dl>

 

 