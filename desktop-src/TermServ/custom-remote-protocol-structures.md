---
title: Estructuras de proveedor de Protocolo de escritorio remoto
description: La API de protocolo remoto personalizada admite las siguientes estructuras.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a626db328ede3bac9422a9a47ebe55f05953a22d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676105"
---
# <a name="remote-desktop-protocol-provider-structures"></a><span data-ttu-id="6c09d-103">Estructuras de proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="6c09d-103">Remote Desktop Protocol Provider Structures</span></span>

<span data-ttu-id="6c09d-104">La API de protocolo remoto personalizada admite las siguientes estructuras.</span><span class="sxs-lookup"><span data-stu-id="6c09d-104">The custom remote protocol API supports the following structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6c09d-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6c09d-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="6c09d-106">**TSMF \_ admiten \_ datos \_ en**</span><span class="sxs-lookup"><span data-stu-id="6c09d-106">**TSMF\_SUPPORT\_DATA\_IN**</span></span>](tsmf-support-data-in.md)
</dt> <dd>

<span data-ttu-id="6c09d-107">Contiene información acerca de los formatos de medios.</span><span class="sxs-lookup"><span data-stu-id="6c09d-107">Contains information about media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-108">**TSMF \_ admiten \_ datos de \_ salida**</span><span class="sxs-lookup"><span data-stu-id="6c09d-108">**TSMF\_SUPPORT\_DATA\_OUT**</span></span>](tsmf-support-data-out.md)
</dt> <dd>

<span data-ttu-id="6c09d-109">Contiene información acerca de los formatos de medios.</span><span class="sxs-lookup"><span data-stu-id="6c09d-109">Contains information about media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-110">**TSMF \_ admite \_ NODEDATA \_ en**</span><span class="sxs-lookup"><span data-stu-id="6c09d-110">**TSMF\_SUPPORT\_NODEDATA\_IN**</span></span>](tsmf-support-nodedata-in.md)
</dt> <dd>

<span data-ttu-id="6c09d-111">Se utiliza dentro de los [**\_ \_ datos \_ de soporte de TSMF en**](tsmf-support-data-in.md) la estructura para contener información acerca de los formatos multimedia admitidos.</span><span class="sxs-lookup"><span data-stu-id="6c09d-111">Used inside the [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure to contain information about supported media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-112">**\_compatibilidad con TSMF \_ NODEDATA \_ out**</span><span class="sxs-lookup"><span data-stu-id="6c09d-112">**TSMF\_SUPPORT\_NODEDATA\_OUT**</span></span>](tsmf-support-nodedata-out.md)
</dt> <dd>

<span data-ttu-id="6c09d-113">Se usa dentro de la estructura de salida de datos de soporte de TSMF para contener información acerca de los formatos multimedia admitidos. [**\_ \_ \_**](tsmf-support-data-out.md)</span><span class="sxs-lookup"><span data-stu-id="6c09d-113">Used inside the [**TSMF\_SUPPORT\_DATA\_OUT**](tsmf-support-data-out.md) structure to contain information about supported media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-114">**\_configuración de conexión de Wrds \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-114">**WRDS\_CONNECTION\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

<span data-ttu-id="6c09d-115">Contiene información de configuración de conexión para una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="6c09d-115">Contains connection setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-116">**Configuración de conexión de WRDS \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6c09d-116">**WRDS\_CONNECTION\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

<span data-ttu-id="6c09d-117">Contiene información de configuración de conexión para una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="6c09d-117">Contains connection setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-118">**WRDS \_ \_ información de \_ zona \_ horaria dinámica**</span><span class="sxs-lookup"><span data-stu-id="6c09d-118">**WRDS\_DYNAMIC\_TIME\_ZONE\_INFORMATION**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

<span data-ttu-id="6c09d-119">Contiene información de zona horaria dinámica.</span><span class="sxs-lookup"><span data-stu-id="6c09d-119">Contains dynamic time zone information.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-120">**\_configuración del agente de escucha de Wrds \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-120">**WRDS\_LISTENER\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

<span data-ttu-id="6c09d-121">Contiene información de configuración del agente de escucha para una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="6c09d-121">Contains listener setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-122">**Configuración del agente de escucha de WRDS \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6c09d-122">**WRDS\_LISTENER\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

<span data-ttu-id="6c09d-123">Contiene la configuración del agente de escucha para una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="6c09d-123">Contains listener settings for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-124">**configuración de WRDS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-124">**WRDS\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

<span data-ttu-id="6c09d-125">Contiene información de configuración relacionada con la Directiva para una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="6c09d-125">Contains policy-related setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-126">**Configuración de WRDS \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6c09d-126">**WRDS\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

<span data-ttu-id="6c09d-127">Contiene la configuración relacionada con la Directiva para una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="6c09d-127">Contains policy-related settings for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-128">**\_estadísticas de caché de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-128">**WTS\_CACHE\_STATS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

<span data-ttu-id="6c09d-129">Contiene estadísticas de caché del protocolo.</span><span class="sxs-lookup"><span data-stu-id="6c09d-129">Contains protocol cache statistics.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-130">**\_Ver \_ ioctl de WTS**</span><span class="sxs-lookup"><span data-stu-id="6c09d-130">**WTS\_DISPLAY\_IOCTL**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

<span data-ttu-id="6c09d-131">Contiene información acerca de la presentación del cliente.</span><span class="sxs-lookup"><span data-stu-id="6c09d-131">Contains information about the client display.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-132">**\_datos de cliente de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-132">**WTS\_CLIENT\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

<span data-ttu-id="6c09d-133">Contiene información acerca de la conexión de cliente.</span><span class="sxs-lookup"><span data-stu-id="6c09d-133">Contains information about the client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-134">**\_funcionalidades de licencia de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-134">**WTS\_LICENSE\_CAPABILITIES**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

<span data-ttu-id="6c09d-135">Contiene información sobre las capacidades de licencia del cliente.</span><span class="sxs-lookup"><span data-stu-id="6c09d-135">Contains information about the licensing capabilities of the client.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-136">**\_datos de directiva de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-136">**WTS\_POLICY\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

<span data-ttu-id="6c09d-137">Contiene información de directiva que pasa el servicio Servicios de Escritorio remoto al Protocolo.</span><span class="sxs-lookup"><span data-stu-id="6c09d-137">Contains policy information that is passed by the Remote Desktop Services service to the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-138">**\_valor de propiedad de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-138">**WTS\_PROPERTY\_VALUE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

<span data-ttu-id="6c09d-139">Contiene información sobre un valor de propiedad que se va a recuperar del protocolo.</span><span class="sxs-lookup"><span data-stu-id="6c09d-139">Contains information about a property value to retrieve from the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-140">**\_caché del protocolo WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-140">**WTS\_PROTOCOL\_CACHE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

<span data-ttu-id="6c09d-141">Contiene el número de lecturas de caché y aciertos de caché.</span><span class="sxs-lookup"><span data-stu-id="6c09d-141">Contains the number of cache reads and cache hits.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-142">**\_contadores del protocolo WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-142">**WTS\_PROTOCOL\_COUNTERS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

<span data-ttu-id="6c09d-143">Contiene contadores de rendimiento del protocolo.</span><span class="sxs-lookup"><span data-stu-id="6c09d-143">Contains protocol performance counters.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-144">**\_Estado del Protocolo de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-144">**WTS\_PROTOCOL\_STATUS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

<span data-ttu-id="6c09d-145">Contiene información sobre el estado del protocolo.</span><span class="sxs-lookup"><span data-stu-id="6c09d-145">Contains information about the status of the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-146">**\_Estado del servicio de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-146">**WTS\_SERVICE\_STATE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

<span data-ttu-id="6c09d-147">Contiene información sobre los cambios en el estado del servicio Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="6c09d-147">Contains information about changes in the state of the Remote Desktop Services service.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-148">**\_ID. de sesión de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-148">**WTS\_SESSION\_ID**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

<span data-ttu-id="6c09d-149">Contiene un **GUID** que identifica de forma única una sesión.</span><span class="sxs-lookup"><span data-stu-id="6c09d-149">Contains a **GUID** that uniquely identifies a session.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-150">**\_rectángulo pequeño de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-150">**WTS\_SMALL\_RECT**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

<span data-ttu-id="6c09d-151">Contiene las coordenadas de la ventana de cliente.</span><span class="sxs-lookup"><span data-stu-id="6c09d-151">Contains client window coordinates.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-152">**SOCKADDR de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-152">**WTS\_SOCKADDR**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

<span data-ttu-id="6c09d-153">Contiene una dirección de socket.</span><span class="sxs-lookup"><span data-stu-id="6c09d-153">Contains a socket address.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-154">**SYSTEMTIME de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-154">**WTS\_SYSTEMTIME**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

<span data-ttu-id="6c09d-155">Especifica la información de fecha y hora para las transiciones entre la hora estándar y el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="6c09d-155">Specifies date and time information for transitions between standard time and daylight saving time.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-156">**\_información de \_ zona \_ horaria de WTS**</span><span class="sxs-lookup"><span data-stu-id="6c09d-156">**WTS\_TIME\_ZONE\_INFORMATION**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

<span data-ttu-id="6c09d-157">Contiene información de zona horaria del cliente.</span><span class="sxs-lookup"><span data-stu-id="6c09d-157">Contains client time zone information.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-158">**\_credencial de usuario de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-158">**WTS\_USER\_CREDENTIAL**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

<span data-ttu-id="6c09d-159">Contiene información de credenciales para un usuario.</span><span class="sxs-lookup"><span data-stu-id="6c09d-159">Contains credential information for a user.</span></span>

</dd> <dt>

[<span data-ttu-id="6c09d-160">**\_datos de usuario de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="6c09d-160">**WTS\_USER\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

<span data-ttu-id="6c09d-161">Contiene los valores de propiedad Select Client.</span><span class="sxs-lookup"><span data-stu-id="6c09d-161">Contains select client property values.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="6c09d-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c09d-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c09d-163">Referencia del proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="6c09d-163">Remote Desktop Protocol Provider Reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dt>

[<span data-ttu-id="6c09d-164">Enumeraciones de proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="6c09d-164">Remote Desktop Protocol Provider Enumerations</span></span>](custom-remote-protocol-enumerations.md)
</dt> <dt>

[<span data-ttu-id="6c09d-165">Interfaces de proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="6c09d-165">Remote Desktop Protocol Provider Interfaces</span></span>](custom-remote-protocol-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6c09d-166">Uniones de proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="6c09d-166">Remote Desktop Protocol Provider Unions</span></span>](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




