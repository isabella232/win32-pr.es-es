---
title: Servicios de Escritorio remoto funciones de la API
description: Las siguientes funciones se usan con Servicios de Escritorio remoto.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792135"
---
# <a name="remote-desktop-services-api-functions"></a><span data-ttu-id="840ad-103">Servicios de Escritorio remoto funciones de la API</span><span class="sxs-lookup"><span data-stu-id="840ad-103">Remote Desktop Services API Functions</span></span>

<span data-ttu-id="840ad-104">Las siguientes funciones se usan con Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-104">The following functions are used with Remote Desktop Services.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="840ad-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="840ad-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="840ad-106">**ProcessIdToSessionId**</span><span class="sxs-lookup"><span data-stu-id="840ad-106">**ProcessIdToSessionId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

<span data-ttu-id="840ad-107">Recupera la sesión de Servicios de Escritorio remoto asociada a un proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-107">Retrieves the Remote Desktop Services session associated with a specified process.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-108">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="840ad-108">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dd>

<span data-ttu-id="840ad-109">Abre un identificador del servidor de licencias de Escritorio remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-109">Opens a handle to the specified Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-110">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="840ad-110">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> <dd>

<span data-ttu-id="840ad-111">Cierra un identificador abierto a un servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-111">Closes an open handle to a Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-112">**TLSGetServerCertificate**</span><span class="sxs-lookup"><span data-stu-id="840ad-112">**TLSGetServerCertificate**</span></span>](tlsgetservercertificate.md)
</dt> <dd>

<span data-ttu-id="840ad-113">Devuelve el certificado del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-113">Returns the certificate of the Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-114">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="840ad-114">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dd>

<span data-ttu-id="840ad-115">Comienza la enumeración a través de todos los paquetes de claves instalados en un servidor de licencias de Escritorio remoto basado en criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="840ad-115">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-116">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="840ad-116">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> <dd>

<span data-ttu-id="840ad-117">Continúa desde una llamada anterior a la función [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) y finaliza la enumeración.</span><span class="sxs-lookup"><span data-stu-id="840ad-117">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-118">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="840ad-118">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dd>

<span data-ttu-id="840ad-119">Continúa desde una llamada anterior a la función [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) y devuelve el siguiente paquete de claves que está instalado en un servidor de licencias escritorio remoto que coincida con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="840ad-119">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-120">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="840ad-120">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dd>

<span data-ttu-id="840ad-121">Comienza la enumeración de licencias emitidas por el servidor de licencias de Escritorio remoto basado en criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="840ad-121">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-122">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="840ad-122">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> <dd>

<span data-ttu-id="840ad-123">Continúa desde una llamada anterior a la función [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) y finaliza la enumeración.</span><span class="sxs-lookup"><span data-stu-id="840ad-123">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-124">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="840ad-124">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dd>

<span data-ttu-id="840ad-125">Continúa desde una llamada anterior a la función [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) y devuelve la siguiente licencia que se instala en un servidor de licencias escritorio remoto que coincide con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="840ad-125">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-126">**VirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="840ad-126">**VirtualChannelClose**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

<span data-ttu-id="840ad-127">Cierra el cliente final de un canal virtual.</span><span class="sxs-lookup"><span data-stu-id="840ad-127">Closes the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-128">**VirtualChannelEntry**</span><span class="sxs-lookup"><span data-stu-id="840ad-128">**VirtualChannelEntry**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

<span data-ttu-id="840ad-129">Un punto de entrada definido por la aplicación para el archivo DLL del lado cliente de una aplicación que usa Servicios de Escritorio remoto canales virtuales.</span><span class="sxs-lookup"><span data-stu-id="840ad-129">An application-defined entry point for the client-side DLL of an application that uses Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-130">**VirtualChannelInit**</span><span class="sxs-lookup"><span data-stu-id="840ad-130">**VirtualChannelInit**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

<span data-ttu-id="840ad-131">Inicializa el acceso de un archivo DLL de cliente para Servicios de Escritorio remoto canales virtuales.</span><span class="sxs-lookup"><span data-stu-id="840ad-131">Initializes a client DLL's access to Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-132">*VirtualChannelInitEvent*</span><span class="sxs-lookup"><span data-stu-id="840ad-132">*VirtualChannelInitEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

<span data-ttu-id="840ad-133">Función de devolución de llamada definida por la aplicación que Servicios de Escritorio remoto llamadas para notificar a la DLL de cliente los eventos de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="840ad-133">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of virtual channel events.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-134">**VirtualChannelOpen**</span><span class="sxs-lookup"><span data-stu-id="840ad-134">**VirtualChannelOpen**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

<span data-ttu-id="840ad-135">Abre el cliente final de un canal virtual.</span><span class="sxs-lookup"><span data-stu-id="840ad-135">Opens the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-136">*VirtualChannelOpenEvent*</span><span class="sxs-lookup"><span data-stu-id="840ad-136">*VirtualChannelOpenEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

<span data-ttu-id="840ad-137">Función de devolución de llamada definida por la aplicación que Servicios de Escritorio remoto llamadas para notificar a la DLL del cliente los eventos de un canal virtual concreto.</span><span class="sxs-lookup"><span data-stu-id="840ad-137">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of events for a specific virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-138">**VirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="840ad-138">**VirtualChannelWrite**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

<span data-ttu-id="840ad-139">Envía datos del extremo de cliente de un canal virtual a una aplicación de socio en el extremo del servidor.</span><span class="sxs-lookup"><span data-stu-id="840ad-139">Sends data from the client end of a virtual channel to a partner application on the server end.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-140">**WTSCloseServer**</span><span class="sxs-lookup"><span data-stu-id="840ad-140">**WTSCloseServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

<span data-ttu-id="840ad-141">Cierra un identificador abierto a un servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="840ad-141">Closes an open handle to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-142">**WTSConnectSession**</span><span class="sxs-lookup"><span data-stu-id="840ad-142">**WTSConnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

<span data-ttu-id="840ad-143">Conecta una sesión de Servicios de Escritorio remoto a una sesión existente en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="840ad-143">Connects a Remote Desktop Services session to an existing session on the local computer.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-144">**WTSCreateListener**</span><span class="sxs-lookup"><span data-stu-id="840ad-144">**WTSCreateListener**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

<span data-ttu-id="840ad-145">Crea un nuevo agente de escucha de Servicios de Escritorio remoto o configura un agente de escucha existente.</span><span class="sxs-lookup"><span data-stu-id="840ad-145">Creates a new Remote Desktop Services listener or configures an existing listener.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-146">**WTSDisconnectSession**</span><span class="sxs-lookup"><span data-stu-id="840ad-146">**WTSDisconnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

<span data-ttu-id="840ad-147">Desconecta el usuario que ha iniciado sesión de la sesión de Servicios de Escritorio remoto especificada sin cerrar la sesión.</span><span class="sxs-lookup"><span data-stu-id="840ad-147">Disconnects the logged-on user from the specified Remote Desktop Services session without closing the session.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-148">**WTSEnableChildSessions**</span><span class="sxs-lookup"><span data-stu-id="840ad-148">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

<span data-ttu-id="840ad-149">Habilita o deshabilita las [sesiones secundarias](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="840ad-149">Enables or disables [Child Sessions](child-sessions.md).</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-150">**WTSEnumerateListeners**</span><span class="sxs-lookup"><span data-stu-id="840ad-150">**WTSEnumerateListeners**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

<span data-ttu-id="840ad-151">Enumera todos los agentes de escucha de Servicios de Escritorio remoto en un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-151">Enumerates all the Remote Desktop Services listeners on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-152">**WTSEnumerateProcesses**</span><span class="sxs-lookup"><span data-stu-id="840ad-152">**WTSEnumerateProcesses**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

<span data-ttu-id="840ad-153">Recupera información sobre los procesos activos en un servidor host de sesión de escritorio remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-153">Retrieves information about the active processes on a specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-154">**WTSEnumerateProcessesEx**</span><span class="sxs-lookup"><span data-stu-id="840ad-154">**WTSEnumerateProcessesEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

<span data-ttu-id="840ad-155">Recupera información sobre los procesos activos en el servidor host de sesión de escritorio remoto especificado o en el servidor de Host de virtualización de Escritorio remoto (host de virtualización de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="840ad-155">Retrieves information about the active processes on the specified RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-156">**WTSEnumerateServers**</span><span class="sxs-lookup"><span data-stu-id="840ad-156">**WTSEnumerateServers**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

<span data-ttu-id="840ad-157">Devuelve una lista de todos los servidores host de sesión de escritorio remoto dentro del dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-157">Returns a list of all RD Session Host servers within the specified domain.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-158">**WTSEnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="840ad-158">**WTSEnumerateSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

<span data-ttu-id="840ad-159">Recupera una lista de sesiones en un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-159">Retrieves a list of sessions on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-160">**WTSEnumerateSessionsEx**</span><span class="sxs-lookup"><span data-stu-id="840ad-160">**WTSEnumerateSessionsEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

<span data-ttu-id="840ad-161">Recupera una lista de sesiones en un servidor host de sesión de escritorio remoto o en un servidor host de virtualización de escritorio remoto especificados.</span><span class="sxs-lookup"><span data-stu-id="840ad-161">Retrieves a list of sessions on a specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-162">**WTSFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="840ad-162">**WTSFreeMemory**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

<span data-ttu-id="840ad-163">Libera memoria asignada por una función Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-163">Frees memory allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-164">**WTSFreeMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="840ad-164">**WTSFreeMemoryEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

<span data-ttu-id="840ad-165">Libera memoria que contiene las estructuras de [**información del proceso de WTS \_ \_ \_ ex**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) o de la información de sesión de WTS asignada por una función servicios de escritorio remoto. [**\_ \_ \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)</span><span class="sxs-lookup"><span data-stu-id="840ad-165">Frees memory that contains [**WTS\_PROCESS\_INFO\_EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) or [**WTS\_SESSION\_INFO\_1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) structures allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-166">**WTSGetActiveConsoleSessionId**</span><span class="sxs-lookup"><span data-stu-id="840ad-166">**WTSGetActiveConsoleSessionId**</span></span>](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

<span data-ttu-id="840ad-167">Recupera el identificador de sesión de la sesión de consola.</span><span class="sxs-lookup"><span data-stu-id="840ad-167">Retrieves the session identifier of the console session.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-168">**WTSGetChildSessionId**</span><span class="sxs-lookup"><span data-stu-id="840ad-168">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

<span data-ttu-id="840ad-169">Recupera el identificador de la sesión secundaria, si está presente.</span><span class="sxs-lookup"><span data-stu-id="840ad-169">Retrieves the child session identifier, if present.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-170">**WTSGetListenerSecurity**</span><span class="sxs-lookup"><span data-stu-id="840ad-170">**WTSGetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="840ad-171">Recupera el descriptor de seguridad de un agente de escucha de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-171">Retrieves the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-172">**WTSIsChildSessionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="840ad-172">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

<span data-ttu-id="840ad-173">Determina si las sesiones secundarias están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="840ad-173">Determines whether child sessions are enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-174">**WTSLogoffSession**</span><span class="sxs-lookup"><span data-stu-id="840ad-174">**WTSLogoffSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

<span data-ttu-id="840ad-175">Cierra una sesión de Servicios de Escritorio remoto especificada.</span><span class="sxs-lookup"><span data-stu-id="840ad-175">Logs off a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-176">**WTSOpenServer**</span><span class="sxs-lookup"><span data-stu-id="840ad-176">**WTSOpenServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

<span data-ttu-id="840ad-177">Abre un identificador para el servidor host de sesión de escritorio remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-177">Opens a handle to the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-178">**WTSOpenServerEx**</span><span class="sxs-lookup"><span data-stu-id="840ad-178">**WTSOpenServerEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

<span data-ttu-id="840ad-179">Abre un identificador para el servidor host de sesión de escritorio remoto especificado o el servidor host de virtualización de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-179">Opens a handle to the specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-180">**WTSQueryListenerConfig**</span><span class="sxs-lookup"><span data-stu-id="840ad-180">**WTSQueryListenerConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

<span data-ttu-id="840ad-181">Recupera la información de configuración de un agente de escucha de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-181">Retrieves configuration information for a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-182">**WTSQuerySessionInformation**</span><span class="sxs-lookup"><span data-stu-id="840ad-182">**WTSQuerySessionInformation**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

<span data-ttu-id="840ad-183">Recupera información de sesión para la sesión especificada en el servidor host de sesión de escritorio remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-183">Retrieves session information for the specified session on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-184">**WTSQueryUserConfig**</span><span class="sxs-lookup"><span data-stu-id="840ad-184">**WTSQueryUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

<span data-ttu-id="840ad-185">Recupera información de configuración para el usuario especificado en el controlador de dominio especificado o en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-185">Retrieves configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-186">**WTSQueryUserToken**</span><span class="sxs-lookup"><span data-stu-id="840ad-186">**WTSQueryUserToken**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

<span data-ttu-id="840ad-187">Obtiene el token de acceso principal del usuario que ha iniciado sesión especificado por el identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="840ad-187">Obtains the primary access token of the logged-on user specified by the session ID.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-188">**WTSRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="840ad-188">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

<span data-ttu-id="840ad-189">Registra la ventana especificada para recibir notificaciones de cambio de sesión.</span><span class="sxs-lookup"><span data-stu-id="840ad-189">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-190">**WTSRegisterSessionNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="840ad-190">**WTSRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="840ad-191">Registra la ventana especificada para recibir notificaciones de cambio de sesión.</span><span class="sxs-lookup"><span data-stu-id="840ad-191">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-192">**WTSSendMessage**</span><span class="sxs-lookup"><span data-stu-id="840ad-192">**WTSSendMessage**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

<span data-ttu-id="840ad-193">Muestra un cuadro de mensaje en el escritorio de cliente de una sesión de Servicios de Escritorio remoto especificada.</span><span class="sxs-lookup"><span data-stu-id="840ad-193">Displays a message box on the client desktop of a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-194">**WTSSetListenerSecurity**</span><span class="sxs-lookup"><span data-stu-id="840ad-194">**WTSSetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="840ad-195">Configura el descriptor de seguridad de un agente de escucha de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-195">Configures the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-196">**WTSSetUserConfig**</span><span class="sxs-lookup"><span data-stu-id="840ad-196">**WTSSetUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

<span data-ttu-id="840ad-197">Modifica la información de configuración del usuario especificado en el controlador de dominio especificado o en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-197">Modifies configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-198">**WTSShutdownSystem**</span><span class="sxs-lookup"><span data-stu-id="840ad-198">**WTSShutdownSystem**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

<span data-ttu-id="840ad-199">Cierra (y, opcionalmente, se reinicia) el servidor host de sesión de escritorio remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-199">Shuts down (and optionally restarts) the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-200">**WTSStartRemoteControlSession**</span><span class="sxs-lookup"><span data-stu-id="840ad-200">**WTSStartRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

<span data-ttu-id="840ad-201">Inicia el control remoto de otra sesión de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-201">Starts the remote control of another Remote Desktop Services session.</span></span> <span data-ttu-id="840ad-202">Debe llamar a esta función desde una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="840ad-202">You must call this function from a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-203">**WTSStopRemoteControlSession**</span><span class="sxs-lookup"><span data-stu-id="840ad-203">**WTSStopRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

<span data-ttu-id="840ad-204">Detiene una sesión de control remoto.</span><span class="sxs-lookup"><span data-stu-id="840ad-204">Stops a remote control session.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-205">**WTSTerminateProcess**</span><span class="sxs-lookup"><span data-stu-id="840ad-205">**WTSTerminateProcess**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

<span data-ttu-id="840ad-206">Finaliza el proceso especificado en el servidor host de sesión de escritorio remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-206">Terminates the specified process on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-207">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="840ad-207">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

<span data-ttu-id="840ad-208">Anula el registro de la ventana especificada para que no reciba más notificaciones de cambio de sesión.</span><span class="sxs-lookup"><span data-stu-id="840ad-208">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-209">**WTSUnRegisterSessionNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="840ad-209">**WTSUnRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="840ad-210">Anula el registro de la ventana especificada para que no reciba más notificaciones de cambio de sesión.</span><span class="sxs-lookup"><span data-stu-id="840ad-210">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-211">**WTSVirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="840ad-211">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="840ad-212">Cierra un identificador de canal virtual abierto.</span><span class="sxs-lookup"><span data-stu-id="840ad-212">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-213">**WTSVirtualChannelOpen**</span><span class="sxs-lookup"><span data-stu-id="840ad-213">**WTSVirtualChannelOpen**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

<span data-ttu-id="840ad-214">Abre un identificador del extremo del servidor de un canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-214">Opens a handle to the server end of a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-215">**WTSVirtualChannelOpenEx**</span><span class="sxs-lookup"><span data-stu-id="840ad-215">**WTSVirtualChannelOpenEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

<span data-ttu-id="840ad-216">Crea un canal virtual de forma similar a [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span><span class="sxs-lookup"><span data-stu-id="840ad-216">Creates a virtual channel in a manner similar to [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-217">**WTSVirtualChannelPurgeInput**</span><span class="sxs-lookup"><span data-stu-id="840ad-217">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="840ad-218">Elimina todos los datos de entrada en cola enviados del cliente al servidor en un canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-218">Deletes all queued input data sent from the client to the server on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-219">**WTSVirtualChannelPurgeOutput**</span><span class="sxs-lookup"><span data-stu-id="840ad-219">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="840ad-220">Elimina todos los datos de salida en cola enviados desde el servidor al cliente en un canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-220">Deletes all queued output data sent from the server to the client on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-221">**WTSVirtualChannelQuery**</span><span class="sxs-lookup"><span data-stu-id="840ad-221">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="840ad-222">Devuelve información sobre un canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="840ad-222">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-223">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="840ad-223">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="840ad-224">Lee los datos del extremo del servidor de un canal virtual.</span><span class="sxs-lookup"><span data-stu-id="840ad-224">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-225">**WTSVirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="840ad-225">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="840ad-226">Escribe datos en el extremo del servidor de un canal virtual.</span><span class="sxs-lookup"><span data-stu-id="840ad-226">Writes data to the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="840ad-227">**WTSWaitSystemEvent**</span><span class="sxs-lookup"><span data-stu-id="840ad-227">**WTSWaitSystemEvent**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

<span data-ttu-id="840ad-228">Espera un evento Servicios de Escritorio remoto antes de volver al llamador.</span><span class="sxs-lookup"><span data-stu-id="840ad-228">Waits for a Remote Desktop Services event before returning to the caller.</span></span>

</dd> </dl>

 

 