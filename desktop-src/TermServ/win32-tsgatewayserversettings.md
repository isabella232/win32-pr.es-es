---
title: Win32_TSGatewayServerSettings (clase)
description: Proporciona métodos y propiedades para ver y configurar la configuración del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayServerSettings de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0fb9b93f75c47760da8778e4aef8bed7f4e022
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492706"
---
# <a name="win32_tsgatewayserversettings-class"></a><span data-ttu-id="eb9ed-105">\_Clase Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="eb9ed-105">Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="eb9ed-106">Proporciona métodos y propiedades para ver y configurar la configuración del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="eb9ed-106">Provides methods and properties to view and configure Remote Desktop Gateway (RD Gateway) server settings.</span></span> <span data-ttu-id="eb9ed-107">Un administrador puede utilizar esta clase para configurar un conjunto de protocolos, el conjunto de eventos que se escribirán en el registro de eventos y el número máximo de conexiones a través de la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-107">An administrator can use this class to configure a set of protocols, the set of events that will be written to the event log, and the maximum number of connections through RD Gateway.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9ed-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb9ed-108">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a><span data-ttu-id="eb9ed-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="eb9ed-109">Members</span></span>

<span data-ttu-id="eb9ed-110">La **clase \_ TSGatewayServerSettings de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eb9ed-110">The **Win32\_TSGatewayServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="eb9ed-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="eb9ed-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="eb9ed-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb9ed-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eb9ed-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="eb9ed-113">Methods</span></span>

<span data-ttu-id="eb9ed-114">La clase **Win32 \_ TSGatewayServerSettings** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-114">The **Win32\_TSGatewayServerSettings** class has these methods.</span></span>



| <span data-ttu-id="eb9ed-115">Método</span><span class="sxs-lookup"><span data-stu-id="eb9ed-115">Method</span></span>                                                                                                                                             | <span data-ttu-id="eb9ed-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb9ed-116">Description</span></span>                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb9ed-117">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-117">**Configure**</span></span>](configure-win32-tsgatewayserversettings.md)                                                                                       | <span data-ttu-id="eb9ed-118">Configura los valores de IIS y RPC requeridos por el servicio de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-118">Configures the IIS and RPC settings required by the RD Gateway service.</span></span><br/> <span data-ttu-id="eb9ed-119">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-119">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                               |
| [<span data-ttu-id="eb9ed-120">**EnableCentralCAP**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-120">**EnableCentralCAP**</span></span>](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="eb9ed-121">Habilita o deshabilita la propiedad **CentralCAPEnabled** , que controla si se usan los servidores de la Directiva de autorización de conexión (Cap) central escritorio remoto para controlar las directivas de autorización de conexión para este servidor.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-121">Enables or disables the **CentralCAPEnabled** property, which controls whether central Remote Desktop connection authorization policy (RD CAP) servers are used for controlling connection authorization policies for this server.</span></span><br/>                    |
| [<span data-ttu-id="eb9ed-122">**EnableLogEvent**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-122">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="eb9ed-123">Habilita o deshabilita el registro del tipo de evento especificado.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-123">Enables or disables logging of the specified event type.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="eb9ed-124">**EnableOnlyConsentCapableClients**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-124">**EnableOnlyConsentCapableClients**</span></span>](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | <span data-ttu-id="eb9ed-125">Establece la propiedad **OnlyConsentCapableClients** .</span><span class="sxs-lookup"><span data-stu-id="eb9ed-125">Sets the **OnlyConsentCapableClients** property.</span></span><br/> <span data-ttu-id="eb9ed-126">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-126">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="eb9ed-127">**EnableRequestSOH**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-127">**EnableRequestSOH**</span></span>](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | <span data-ttu-id="eb9ed-128">Este método no se admite a partir de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-128">This method is not supported starting with Windows Server 2016.</span></span><br/> <span data-ttu-id="eb9ed-129">**Windows server 2012 R2, Windows server 2012, Windows server 2008 R2 y Windows server 2008:** Habilita o deshabilita las solicitudes de un informe de mantenimiento (SoH).</span><span class="sxs-lookup"><span data-stu-id="eb9ed-129">**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:** Enables or disables requests for a Statement of Health (SoH).</span></span><br/> <br/> |
| [<span data-ttu-id="eb9ed-130">**EnableTransport**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-130">**EnableTransport**</span></span>](enabletransport-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="eb9ed-131">Habilita o deshabilita el transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-131">Enables or disables the specified transport.</span></span><br/> <span data-ttu-id="eb9ed-132">**Windows server 2008 R2 y Windows server 2008:** Este método no está disponible antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-132">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="eb9ed-133">**EnumAuthenticationPlugins**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-133">**EnumAuthenticationPlugins**</span></span>](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | <span data-ttu-id="eb9ed-134">Enumera todos los complementos de autenticación registrados.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-134">Enumerates all registered authentication plug-ins.</span></span><br/> <span data-ttu-id="eb9ed-135">**Windows Server 2008:** Este método no está disponible.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-135">**Windows Server 2008:** This method is not available.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="eb9ed-136">**EnumAuthorizationPlugins**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-136">**EnumAuthorizationPlugins**</span></span>](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="eb9ed-137">Enumera todos los complementos de autorización registrados.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-137">Enumerates all registered authorization plug-ins.</span></span><br/> <span data-ttu-id="eb9ed-138">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="eb9ed-139">**GetIPAndPort**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-139">**GetIPAndPort**</span></span>](getipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="eb9ed-140">Obtiene la dirección IP de escucha y el número de puerto para el transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-140">Obtains the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="eb9ed-141">**Windows server 2008 R2 y Windows server 2008:** Este método no está disponible antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-141">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                 |
| [<span data-ttu-id="eb9ed-142">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-142">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="eb9ed-143">Devuelve el nombre del evento de registro para el índice de eventos de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-143">Returns the log event name for the specified log event index.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="eb9ed-144">**GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-144">**GetProtocolName**</span></span>](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="eb9ed-145">Devuelve el nombre de protocolo para el índice de protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-145">Returns the protocol name for the specified protocol index.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="eb9ed-146">**IsLogEventEnabled**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-146">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="eb9ed-147">Indica si el tipo de registro de eventos especificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-147">Indicates whether the specified event log type is enabled.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="eb9ed-148">**IsTransportEnabled**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-148">**IsTransportEnabled**</span></span>](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="eb9ed-149">Determina si el transporte especificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-149">Determines whether the specified transport is enabled.</span></span><br/> <span data-ttu-id="eb9ed-150">**Windows server 2008 R2 y Windows server 2008:** Este método no está disponible antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-150">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                        |
| [<span data-ttu-id="eb9ed-151">**QueryCertContext**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-151">**QueryCertContext**</span></span>](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | <span data-ttu-id="eb9ed-152">Indica si el certificado especificado está instalado.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-152">Indicates whether the specified certificate is installed.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="eb9ed-153">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-153">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | <span data-ttu-id="eb9ed-154">Recicla los grupos de aplicaciones RPC en IIS.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-154">Recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="eb9ed-155">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-155">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="eb9ed-156">**RefreshCertContext**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-156">**RefreshCertContext**</span></span>](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | <span data-ttu-id="eb9ed-157">Actualiza el certificado usado por el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-157">Refreshes the certificate that is used by the RD Gateway server.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="eb9ed-158">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-158">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | <span data-ttu-id="eb9ed-159">Establece el complemento de autenticación actual para el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-159">Sets the current authentication plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="eb9ed-160">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-160">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="eb9ed-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span></span>](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | <span data-ttu-id="eb9ed-162">Establece el complemento de autenticación actual para el servidor de puerta de enlace de escritorio remoto y recicla los grupos de aplicaciones RPC en IIS.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-162">Sets the current authentication plug-in for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="eb9ed-163">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-163">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                      |
| [<span data-ttu-id="eb9ed-164">**SetAuthorizationPlugin**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-164">**SetAuthorizationPlugin**</span></span>](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | <span data-ttu-id="eb9ed-165">Establece el complemento de autorización actual para el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-165">Sets the current authorization plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="eb9ed-166">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-166">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                     |
| [<span data-ttu-id="eb9ed-167">**SetCertificate**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-167">**SetCertificate**</span></span>](setcertificate-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="eb9ed-168">Establece el hash del certificado para el enlace HTTPS en el puerto 443 en IIS.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-168">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span><br/> <span data-ttu-id="eb9ed-169">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                       |
| [<span data-ttu-id="eb9ed-170">**SetCertificateACL**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-170">**SetCertificateACL**</span></span>](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="eb9ed-171">Establece las listas de control de acceso (ACL) del certificado para este servidor.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-171">Sets the certificate access control lists (ACLs) for this server.</span></span><br/>                                                                                                                                                                                     |
| [<span data-ttu-id="eb9ed-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span></span>](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | <span data-ttu-id="eb9ed-173">Establece los complementos de autenticación y autorización actuales para el servidor de puerta de enlace de escritorio remoto y recicla los grupos de aplicaciones RPC en IIS.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-173">Sets the current authentication and authorization plug-ins for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="eb9ed-174">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-174">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                   |
| [<span data-ttu-id="eb9ed-175">**SetEnforceChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-175">**SetEnforceChannelBinding**</span></span>](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="eb9ed-176">Establece la propiedad **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="eb9ed-176">Sets the **EnforceChannelBinding** property.</span></span><br/> <span data-ttu-id="eb9ed-177">**Windows server 2008 R2 y Windows server 2008:** Este método no está disponible antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-177">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="eb9ed-178">**SetIPAndPort**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-178">**SetIPAndPort**</span></span>](setipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="eb9ed-179">Establece la dirección IP de escucha y el número de puerto para el transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-179">Sets the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="eb9ed-180">**Windows server 2008 R2 y Windows server 2008:** Este método no está disponible antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-180">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                    |
| [<span data-ttu-id="eb9ed-181">**SetMaxConnections**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-181">**SetMaxConnections**</span></span>](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="eb9ed-182">Establece el número máximo de conexiones permitidas a través de la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-182">Sets the maximum number of allowed connections through RD Gateway.</span></span> <span data-ttu-id="eb9ed-183">Este método cambia las propiedades **MaxConnections** y **UnlimitedConnections** .</span><span class="sxs-lookup"><span data-stu-id="eb9ed-183">This method changes the **MaxConnections** and **UnlimitedConnections** properties.</span></span><br/>                                                                                                |
| [<span data-ttu-id="eb9ed-184">**SetSslBridging**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-184">**SetSslBridging**</span></span>](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="eb9ed-185">Establece el tipo de protocolo de puente SSL que va a usar el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-185">Sets the type of SSL bridging to be used by the RD Gateway server.</span></span><br/> <span data-ttu-id="eb9ed-186">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-186">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="eb9ed-187">**TSGRemoveAdminMsg**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-187">**TSGRemoveAdminMsg**</span></span>](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="eb9ed-188">Quita el mensaje administrativo del servidor de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-188">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="eb9ed-189">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-189">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="eb9ed-190">**TSGRemoveConsentMsg**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-190">**TSGRemoveConsentMsg**</span></span>](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | <span data-ttu-id="eb9ed-191">Quita el mensaje administrativo del servidor de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-191">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="eb9ed-192">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-192">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="eb9ed-193">**TSGStoreAdminMsg**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-193">**TSGStoreAdminMsg**</span></span>](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="eb9ed-194">Actualiza el mensaje administrativo para el servidor de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-194">Updates the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="eb9ed-195">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-195">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="eb9ed-196">**TSGStoreConsentMsg**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-196">**TSGStoreConsentMsg**</span></span>](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="eb9ed-197">Actualiza el mensaje de consentimiento para el servidor de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-197">Updates the consent message for the gateway server.</span></span><br/> <span data-ttu-id="eb9ed-198">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-198">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="eb9ed-199">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb9ed-199">Properties</span></span>

<span data-ttu-id="eb9ed-200">La **clase \_ TSGatewayServerSettings de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-200">The **Win32\_TSGatewayServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb9ed-201">**adminMessageEndTime**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-201">**adminMessageEndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-204">La hora de finalización del mensaje administrativo.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-204">The administrative message end time.</span></span>

<span data-ttu-id="eb9ed-205">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-205">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-206">**adminMessageStartTime**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-206">**adminMessageStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-209">La hora de inicio del mensaje administrativo.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-209">The administrative message start time.</span></span>

<span data-ttu-id="eb9ed-210">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-210">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-211">**adminMessageText**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-211">**adminMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-212">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-214">El texto del mensaje administrativo.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-214">The administrative message text.</span></span>

<span data-ttu-id="eb9ed-215">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-215">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-216">**AuthenticationPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-216">**AuthenticationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-219">CLSID del complemento de autenticación actual.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-219">The CLSID of the current authentication plug-in.</span></span>

<span data-ttu-id="eb9ed-220">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-220">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-221">**AuthenticationPluginDescription**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-221">**AuthenticationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-224">La descripción del complemento de autenticación actual.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-224">The description of the current authentication plug-in.</span></span>

<span data-ttu-id="eb9ed-225">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-225">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-226">**AuthenticationPluginName**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-226">**AuthenticationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-229">Nombre del complemento de autenticación actual.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-229">The name of the current authentication plug-in.</span></span>

<span data-ttu-id="eb9ed-230">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-230">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-231">**AuthorizationPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-231">**AuthorizationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-234">CLSID del complemento de autorización actual.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-234">The CLSID of the current authorization plug-in.</span></span>

<span data-ttu-id="eb9ed-235">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-235">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-236">**AuthorizationPluginDescription**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-236">**AuthorizationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-239">La descripción del complemento de autorización actual.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-239">The description of the current authorization plug-in.</span></span>

<span data-ttu-id="eb9ed-240">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-240">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-241">**AuthorizationPluginName**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-241">**AuthorizationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-244">Nombre del complemento de autorización actual.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-244">The name of the current authorization plug-in.</span></span>

<span data-ttu-id="eb9ed-245">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-245">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-246">**CentralCAPEnabled**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-246">**CentralCAPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-247">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-249">Especifica si se usan los servidores de CAP de RD central para controlar este servidor.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-249">Specifies whether central RD CAP servers are used for controlling this server.</span></span> <span data-ttu-id="eb9ed-250">Esta propiedad se puede cambiar llamando al método [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="eb9ed-250">This property can be changed by calling the [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-251">**CertHash**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-251">**CertHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-252">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="eb9ed-252">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-254">Especifica el hash del certificado para el enlace HTTPS en el puerto 443 en IIS.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-254">Specifies the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

<span data-ttu-id="eb9ed-255">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-255">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-256">**consentMessageText**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-256">**consentMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-259">Texto del mensaje de consentimiento.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-259">The consent message text.</span></span>

<span data-ttu-id="eb9ed-260">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-260">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-261">**EnforceChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-261">**EnforceChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-262">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-264">Indica si se aplica el enlace de canal para el transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-264">Indicates if channel binding is enforced for the HTTP transport.</span></span> <span data-ttu-id="eb9ed-265">Este valor de propiedad se puede cambiar mediante el método [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="eb9ed-265">This property value can be changed by using the [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) method.</span></span>

<span data-ttu-id="eb9ed-266">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-266">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available before Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-267">**IsConfigured**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-267">**IsConfigured**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-268">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-270">Especifica si la configuración de IIS y RPC requerida por el servicio de puerta de enlace de escritorio remoto está configurada.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-270">Specifies if IIS and RPC settings required by the RD Gateway service are configured.</span></span>

<span data-ttu-id="eb9ed-271">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-271">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-272">**MaxConnections**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-272">**MaxConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-273">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-275">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb9ed-275">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-276">Devuelve el número máximo de conexiones permitidas a través de la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-276">Returns the maximum number of connections that are allowed through RD Gateway.</span></span> <span data-ttu-id="eb9ed-277">Esta propiedad se puede establecer mediante el método [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="eb9ed-277">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-278">**MaximumAllowedConnectionsBySku**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-278">**MaximumAllowedConnectionsBySku**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-279">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-281">Número máximo de conexiones que permite la unidad de almacén (SKU).</span><span class="sxs-lookup"><span data-stu-id="eb9ed-281">Maximum number of connections that the stock-keeping unit (SKU) allows.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-282">**MaxLogEvents**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-282">**MaxLogEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-283">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-285">Devuelve el número máximo de eventos de registro.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-285">Returns the maximum number of log events.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-286">**MaxProtocols**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-286">**MaxProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-287">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-289">Número de protocolos admitidos por la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-289">Number of protocols supported by RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-290">**OnlyConsentCapableClients**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-290">**OnlyConsentCapableClients**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-291">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-293">Especifica si solo se permite que los clientes con capacidad de consentimiento se conecten a la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-293">Specifies if only clients capable of consent messages are allowed to connect to the RD Gateway.</span></span>

<span data-ttu-id="eb9ed-294">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-294">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="eb9ed-295">distinto</span><span class="sxs-lookup"><span data-stu-id="eb9ed-295">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="eb9ed-296">Solo los clientes compatibles con mensajes de consentimiento pueden conectarse.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-296">Only consent message capable clients can connect.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-297">cero</span><span class="sxs-lookup"><span data-stu-id="eb9ed-297">zero</span></span>
</dt> <dd>

<span data-ttu-id="eb9ed-298">Los clientes que no son compatibles con los mensajes de consentimiento también pueden conectarse.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-298">Clients that are not consent message capable can also connect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb9ed-299">**RequestSOH**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-299">**RequestSOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-300">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-302">Esta propiedad no se admite a partir de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-302">This property is not supported starting with Windows Server 2016.</span></span>

<span data-ttu-id="eb9ed-303">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 y Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="eb9ed-303">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="eb9ed-304">Especifica si el servidor debe solicitar un informe de mantenimiento (SoH) del cliente.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-304">Specifies whether the server must request a Statement of Health (SoH) from the client.</span></span> <span data-ttu-id="eb9ed-305">Esta propiedad se puede cambiar mediante el método [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) .</span><span class="sxs-lookup"><span data-stu-id="eb9ed-305">This property can be changed by using the [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-306">**SkuName**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-306">**SkuName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-309">Nombre de la SKU.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-309">Name of the SKU.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-310">**SslBridging**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-310">**SslBridging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-311">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-313">Especifica el tipo de protocolo de puente SSL que va a usar el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-313">Specifies which type of SSL bridging to be used by the RD Gateway server.</span></span> <span data-ttu-id="eb9ed-314">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-314">This can be one of the following values.</span></span>

<span data-ttu-id="eb9ed-315">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-315">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="eb9ed-316">0</span><span class="sxs-lookup"><span data-stu-id="eb9ed-316">0</span></span>
</dt> <dd>

<span data-ttu-id="eb9ed-317">Sin puentes SSL.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-317">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-318">1</span><span class="sxs-lookup"><span data-stu-id="eb9ed-318">1</span></span>
</dt> <dd>

<span data-ttu-id="eb9ed-319">Puente de HTTPS a HTTP.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-319">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="eb9ed-320">2</span><span class="sxs-lookup"><span data-stu-id="eb9ed-320">2</span></span>
</dt> <dd>

<span data-ttu-id="eb9ed-321">Puente de HTTPS a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-321">HTTPS to HTTPS bridging.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb9ed-322">**UnlimitedConnections**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-322">**UnlimitedConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb9ed-323">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb9ed-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9ed-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb9ed-325">Indica si se permite un número ilimitado de conexiones a través de la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-325">Indicates whether an unlimited number of connections are allowed through RD Gateway.</span></span> <span data-ttu-id="eb9ed-326">Esta propiedad se puede establecer mediante el método [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="eb9ed-326">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb9ed-327">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb9ed-327">Remarks</span></span>

<span data-ttu-id="eb9ed-328">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-328">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="eb9ed-329">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="eb9ed-329">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eb9ed-330">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-330">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eb9ed-331">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-331">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eb9ed-332">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="eb9ed-332">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb9ed-333">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb9ed-333">Requirements</span></span>



| <span data-ttu-id="eb9ed-334">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb9ed-334">Requirement</span></span> | <span data-ttu-id="eb9ed-335">Value</span><span class="sxs-lookup"><span data-stu-id="eb9ed-335">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9ed-336">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb9ed-336">Minimum supported client</span></span><br/> | <span data-ttu-id="eb9ed-337">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="eb9ed-337">None supported</span></span><br/>                                                                |
| <span data-ttu-id="eb9ed-338">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb9ed-338">Minimum supported server</span></span><br/> | <span data-ttu-id="eb9ed-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb9ed-339">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="eb9ed-340">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb9ed-340">Namespace</span></span><br/>                | <span data-ttu-id="eb9ed-341">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="eb9ed-341">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="eb9ed-342">MOF</span><span class="sxs-lookup"><span data-stu-id="eb9ed-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb9ed-343"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb9ed-343"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb9ed-344">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb9ed-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb9ed-345"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb9ed-345"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="eb9ed-346">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb9ed-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9ed-347">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-347">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="eb9ed-348">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-348">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="eb9ed-349">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-349">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="eb9ed-350">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-350">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="eb9ed-351">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-351">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="eb9ed-352">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="eb9ed-352">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

