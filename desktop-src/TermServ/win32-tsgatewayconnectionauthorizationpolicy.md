---
title: Win32_TSGatewayConnectionAuthorizationPolicy (clase)
description: Describe una Escritorio remoto Directiva de autorización de conexión (RD \ 160; CAP). RD \ 160; Los Cap se usan para determinar si un usuario puede conectarse al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayConnectionAuthorizationPolicy de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27384ec3a5f17c3e41fe0ceccf0ee1f7f9d08044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905188"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="a4d02-106">\_Clase Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="a4d02-106">Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="a4d02-107">Describe una Escritorio remoto Directiva de autorización de conexión (CAP de RD).</span><span class="sxs-lookup"><span data-stu-id="a4d02-107">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="a4d02-108">Las Cap de RD se usan para determinar si un usuario puede conectarse al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="a4d02-108">RD CAPs are used to determine whether a user is allowed to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d02-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4d02-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a><span data-ttu-id="a4d02-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a4d02-110">Members</span></span>

<span data-ttu-id="a4d02-111">La **clase \_ TSGatewayConnectionAuthorizationPolicy de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a4d02-111">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="a4d02-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a4d02-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a4d02-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a4d02-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a4d02-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="a4d02-114">Methods</span></span>

<span data-ttu-id="a4d02-115">La clase **Win32 \_ TSGatewayConnectionAuthorizationPolicy** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a4d02-115">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="a4d02-116">Método</span><span class="sxs-lookup"><span data-stu-id="a4d02-116">Method</span></span>                                                                                                                | <span data-ttu-id="a4d02-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4d02-117">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4d02-118">**AddComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="a4d02-118">**AddComputerGroupNames**</span></span>](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="a4d02-119">Agrega los nombres de grupo de equipos especificados a la propiedad **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-119">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span><br/>                                                                                      |
| [<span data-ttu-id="a4d02-120">**AddUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="a4d02-120">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="a4d02-121">Agrega los nombres de grupos de usuarios especificados a la propiedad **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-121">Adds the specified user group names to the **UserGroupNames** property.</span></span><br/>                                                                                              |
| [<span data-ttu-id="a4d02-122">**A**</span><span class="sxs-lookup"><span data-stu-id="a4d02-122">**Create**</span></span>](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="a4d02-123">Crea una CAP de RD.</span><span class="sxs-lookup"><span data-stu-id="a4d02-123">Creates an RD CAP.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="a4d02-124">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="a4d02-124">**Delete**</span></span>](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="a4d02-125">Elimina la CAP de RD actual.</span><span class="sxs-lookup"><span data-stu-id="a4d02-125">Deletes the current RD CAP.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="a4d02-126">**DisableClipboard**</span><span class="sxs-lookup"><span data-stu-id="a4d02-126">**DisableClipboard**</span></span>](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | <span data-ttu-id="a4d02-127">Establece la propiedad **ClipboardDisabled** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-127">Sets the **ClipboardDisabled** property.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="a4d02-128">**DisableDiskDrives**</span><span class="sxs-lookup"><span data-stu-id="a4d02-128">**DisableDiskDrives**</span></span>](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="a4d02-129">Establece la propiedad **DiskDrivesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-129">Sets the **DiskDrivesDisabled** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="a4d02-130">**DisablePlugAndPlayDevices**</span><span class="sxs-lookup"><span data-stu-id="a4d02-130">**DisablePlugAndPlayDevices**</span></span>](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | <span data-ttu-id="a4d02-131">Establece la propiedad **PlugAndPlayDevicesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-131">Sets the **PlugAndPlayDevicesDisabled** property.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="a4d02-132">**DisablePrinters**</span><span class="sxs-lookup"><span data-stu-id="a4d02-132">**DisablePrinters**</span></span>](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | <span data-ttu-id="a4d02-133">Establece la propiedad **PrintersDisabled** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-133">Sets the **PrintersDisabled** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="a4d02-134">**DisableSerialPorts**</span><span class="sxs-lookup"><span data-stu-id="a4d02-134">**DisableSerialPorts**</span></span>](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="a4d02-135">Establece la propiedad **SerialPortsDisabled** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-135">Sets the **SerialPortsDisabled** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="a4d02-136">**EnableAllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="a4d02-136">**EnableAllowOnlySDRServers**</span></span>](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | <span data-ttu-id="a4d02-137">Se usa para alternar la propiedad **AllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="a4d02-137">Used to toggle the **AllowOnlySDRServers** property</span></span><br/> <span data-ttu-id="a4d02-138">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a4d02-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                  |
| [<span data-ttu-id="a4d02-139">**Bajar**</span><span class="sxs-lookup"><span data-stu-id="a4d02-139">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | <span data-ttu-id="a4d02-140">Mueve la CAP de RD actual una posición hacia abajo en la lista.</span><span class="sxs-lookup"><span data-stu-id="a4d02-140">Moves the current RD CAP one position down in the list.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="a4d02-141">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="a4d02-141">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="a4d02-142">Mueve la CAP de RD actual una posición hacia arriba en la lista.</span><span class="sxs-lookup"><span data-stu-id="a4d02-142">Moves the current RD CAP one position up in the list.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="a4d02-143">**RemoveComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="a4d02-143">**RemoveComputerGroupNames**</span></span>](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="a4d02-144">Quita los nombres de grupo de equipos especificados de la propiedad **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-144">Removes the specified computer group names from the **ComputerGroupNames** property.</span></span><br/>                                                                                 |
| [<span data-ttu-id="a4d02-145">**RemoveUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="a4d02-145">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | <span data-ttu-id="a4d02-146">Quita los nombres de grupos de usuarios especificados de la propiedad **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-146">Removes specified user group names from the **UserGroupNames** property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="a4d02-147">**SetComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="a4d02-147">**SetComputerGroupNames**</span></span>](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="a4d02-148">Establece la propiedad **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-148">Sets the **ComputerGroupNames** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="a4d02-149">**SetCookieAuthenticationAllowed**</span><span class="sxs-lookup"><span data-stu-id="a4d02-149">**SetCookieAuthenticationAllowed**</span></span>](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | <span data-ttu-id="a4d02-150">Establece la propiedad **CookieAuthenticationAllowed** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-150">Sets the **CookieAuthenticationAllowed** property.</span></span><br/> <span data-ttu-id="a4d02-151">**Windows Server 2008:** Este método no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a4d02-151">**Windows Server 2008:** This method is not available.</span></span><br/>                                                 |
| [<span data-ttu-id="a4d02-152">**SetDeviceRedirectionType**</span><span class="sxs-lookup"><span data-stu-id="a4d02-152">**SetDeviceRedirectionType**</span></span>](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="a4d02-153">Establece la propiedad **DeviceRedirectionType** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-153">Sets the **DeviceRedirectionType** property.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="a4d02-154">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="a4d02-154">**SetEnabled**</span></span>](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | <span data-ttu-id="a4d02-155">Habilita o deshabilita la CAP de RD actual.</span><span class="sxs-lookup"><span data-stu-id="a4d02-155">Enables or disables the current RD CAP.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="a4d02-156">**SetIdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="a4d02-156">**SetIdleTimeout**</span></span>](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | <span data-ttu-id="a4d02-157">Establece la propiedad **IdleTimeout** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-157">Sets the **IdleTimeout** property.</span></span><br/> <span data-ttu-id="a4d02-158">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a4d02-158">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                   |
| [<span data-ttu-id="a4d02-159">**SetName**</span><span class="sxs-lookup"><span data-stu-id="a4d02-159">**SetName**</span></span>](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | <span data-ttu-id="a4d02-160">Establece un nuevo nombre para esta CAP de RD.</span><span class="sxs-lookup"><span data-stu-id="a4d02-160">Sets a new name for this RD CAP.</span></span> <span data-ttu-id="a4d02-161">Este método garantiza que los nombres serán únicos.</span><span class="sxs-lookup"><span data-stu-id="a4d02-161">This method ensures that names will be unique.</span></span><br/>                                                                                      |
| [<span data-ttu-id="a4d02-162">**SetPasswordAllowed**</span><span class="sxs-lookup"><span data-stu-id="a4d02-162">**SetPasswordAllowed**</span></span>](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="a4d02-163">Establece la propiedad **PasswordAllowed** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-163">Sets the **PasswordAllowed** property.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="a4d02-164">**SetSecureIdAllowed**</span><span class="sxs-lookup"><span data-stu-id="a4d02-164">**SetSecureIdAllowed**</span></span>](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="a4d02-165">Establece la propiedad **SecureIdAllowed** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-165">Sets the **SecureIdAllowed** property.</span></span><br/> <span data-ttu-id="a4d02-166">**Windows Server 2008:** Este método se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a4d02-166">**Windows Server 2008:** This method is reserved for future use.</span></span><br/>                                                   |
| [<span data-ttu-id="a4d02-167">**SetSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="a4d02-167">**SetSessionTimeout**</span></span>](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="a4d02-168">Establece las propiedades **SessionTimeout** y **SessionTimeoutAction** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-168">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span><br/> <span data-ttu-id="a4d02-169">**Windows Server 2008:** Este método no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a4d02-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/> |
| [<span data-ttu-id="a4d02-170">**SetSmartcardAllowed**</span><span class="sxs-lookup"><span data-stu-id="a4d02-170">**SetSmartcardAllowed**</span></span>](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | <span data-ttu-id="a4d02-171">Establece la propiedad **SmartcardAllowed** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-171">Sets the **SmartcardAllowed** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="a4d02-172">**SetUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="a4d02-172">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="a4d02-173">Establece la propiedad **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="a4d02-173">Sets the **UserGroupNames** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="a4d02-174">**Update**</span><span class="sxs-lookup"><span data-stu-id="a4d02-174">**Update**</span></span>](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="a4d02-175">Actualiza la CAP de RD actual.</span><span class="sxs-lookup"><span data-stu-id="a4d02-175">Updates the current RD CAP.</span></span><br/>                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="a4d02-176">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a4d02-176">Properties</span></span>

<span data-ttu-id="a4d02-177">La **clase \_ TSGatewayConnectionAuthorizationPolicy de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a4d02-177">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4d02-178">**AllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="a4d02-178">**AllowOnlySDRServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-179">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-181">Indica si las conexiones solo se permiten para los servidores RDS de redirección de dispositivos (SDR).</span><span class="sxs-lookup"><span data-stu-id="a4d02-181">Indicates whether connections allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="a4d02-182">Esta propiedad se puede establecer mediante el método [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) .</span><span class="sxs-lookup"><span data-stu-id="a4d02-182">This property can be set using the [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) method.</span></span>

<span data-ttu-id="a4d02-183">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a4d02-183">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-184">**ClipboardDisabled**</span><span class="sxs-lookup"><span data-stu-id="a4d02-184">**ClipboardDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-185">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-187">Indica si se deshabilitará la redirección del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="a4d02-187">Indicates if clipboard redirection will be disabled.</span></span> <span data-ttu-id="a4d02-188">Esta propiedad solo tiene efecto si la propiedad **DeviceRedirectionType** tiene un valor de "2".</span><span class="sxs-lookup"><span data-stu-id="a4d02-188">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-189">**ComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="a4d02-189">**ComputerGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a4d02-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-192">Lista de nombres de grupos de equipos separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="a4d02-192">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="a4d02-193">Este valor puede estar vacío.</span><span class="sxs-lookup"><span data-stu-id="a4d02-193">This value can be empty.</span></span> <span data-ttu-id="a4d02-194">Los nombres tienen el formato *dominio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="a4d02-194">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="a4d02-195">Si se especifica un valor, el equipo cliente debe pertenecer a uno de estos grupos de equipos para que el usuario tenga acceso al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a4d02-195">If a value is specified, then the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-196">**CookieAuthenticationAllowed**</span><span class="sxs-lookup"><span data-stu-id="a4d02-196">**CookieAuthenticationAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-197">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-199">Indica si se puede usar la autenticación de cookies para conectarse al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a4d02-199">Indicates if cookie authentication can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="a4d02-200">Esta propiedad se puede establecer mediante el método [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="a4d02-200">This property can be set by using the [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="a4d02-201">**Windows Server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a4d02-201">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-202">**DeviceRedirectionType**</span><span class="sxs-lookup"><span data-stu-id="a4d02-202">**DeviceRedirectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-203">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4d02-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-205">Especifica los dispositivos que se redirigirán.</span><span class="sxs-lookup"><span data-stu-id="a4d02-205">Specifies which devices will be redirected.</span></span>

<dt>

<span data-ttu-id="a4d02-206">0</span><span class="sxs-lookup"><span data-stu-id="a4d02-206">0</span></span>
</dt> <dd>

<span data-ttu-id="a4d02-207">Se redirigirán todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a4d02-207">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-208">1</span><span class="sxs-lookup"><span data-stu-id="a4d02-208">1</span></span>
</dt> <dd>

<span data-ttu-id="a4d02-209">No se redirigirá ningún dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4d02-209">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-210">2</span><span class="sxs-lookup"><span data-stu-id="a4d02-210">2</span></span>
</dt> <dd>

<span data-ttu-id="a4d02-211">Los dispositivos especificados no se redirigirán.</span><span class="sxs-lookup"><span data-stu-id="a4d02-211">Specified devices will not be redirected.</span></span> <span data-ttu-id="a4d02-212">Las propiedades **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** y **PlugAndPlayDevicesDisabled** controlan qué dispositivos no se redirigirán.</span><span class="sxs-lookup"><span data-stu-id="a4d02-212">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a4d02-213">**DiskDrivesDisabled**</span><span class="sxs-lookup"><span data-stu-id="a4d02-213">**DiskDrivesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-214">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-216">Indica si se deshabilitará la redirección de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="a4d02-216">Indicates if disk drive redirection will be disabled.</span></span> <span data-ttu-id="a4d02-217">Esta propiedad solo tiene efecto si la propiedad **DeviceRedirectionType** tiene un valor de "2".</span><span class="sxs-lookup"><span data-stu-id="a4d02-217">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-218">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="a4d02-218">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-219">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-221">Indica si se usará esta CAP de RD para evaluar la autorización de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a4d02-221">Indicates whether this RD CAP will be used to evaluate a user for authorization.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-222">**HasNapAttributes**</span><span class="sxs-lookup"><span data-stu-id="a4d02-222">**HasNapAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-223">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-225">Indica si la CAP de RD usa atributos de protección de acceso a redes (NAP).</span><span class="sxs-lookup"><span data-stu-id="a4d02-225">Indicates if the RD CAP uses Network Access Protection (NAP) attributes.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-226">**IdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="a4d02-226">**IdleTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-227">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4d02-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-229">Valor de tiempo de espera de inactividad, en minutos.</span><span class="sxs-lookup"><span data-stu-id="a4d02-229">The idle timeout value, in minutes.</span></span> <span data-ttu-id="a4d02-230">Un valor de 0 significa que no hay tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="a4d02-230">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="a4d02-231">Esta propiedad se puede establecer mediante el método [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="a4d02-231">This property can be set by using the [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="a4d02-232">**Windows Server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a4d02-232">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-233">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a4d02-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-234">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a4d02-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-236">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a4d02-236">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-237">Nombre de la CAP de RD.</span><span class="sxs-lookup"><span data-stu-id="a4d02-237">Name of the RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-238">**Pedido**</span><span class="sxs-lookup"><span data-stu-id="a4d02-238">**Order**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-239">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4d02-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-241">Orden de evaluación de la CAP de RD.</span><span class="sxs-lookup"><span data-stu-id="a4d02-241">Evaluation order of the RD CAP.</span></span> <span data-ttu-id="a4d02-242">La primera CAP de RD evaluada tiene un valor de "1".</span><span class="sxs-lookup"><span data-stu-id="a4d02-242">The first RD CAP evaluated has a value of "1".</span></span> <span data-ttu-id="a4d02-243">La propiedad **Order** se puede cambiar cuando se llama a los métodos [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**moveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)o [**moveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="a4d02-243">The **Order** property can be changed when the [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md), or [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-244">**PasswordAllowed**</span><span class="sxs-lookup"><span data-stu-id="a4d02-244">**PasswordAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-245">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-247">Indica si se puede usar una contraseña para conectarse al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a4d02-247">Indicates if a password can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="a4d02-248">Esta propiedad se puede cambiar mediante el método [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="a4d02-248">This property can be changed by using the [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-249">**PlugAndPlayDevicesDisabled**</span><span class="sxs-lookup"><span data-stu-id="a4d02-249">**PlugAndPlayDevicesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-250">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-252">Indica si se deshabilitará la redirección de Plug and Play dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a4d02-252">Indicates if redirection of Plug and Play devices will be disabled.</span></span> <span data-ttu-id="a4d02-253">Esta propiedad solo tiene efecto si la propiedad **DeviceRedirectionType** tiene un valor de "2".</span><span class="sxs-lookup"><span data-stu-id="a4d02-253">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-254">**PrintersDisabled**</span><span class="sxs-lookup"><span data-stu-id="a4d02-254">**PrintersDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-255">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-257">Indica si se deshabilitará la redirección de la impresora.</span><span class="sxs-lookup"><span data-stu-id="a4d02-257">Indicates if printer redirection will be disabled.</span></span> <span data-ttu-id="a4d02-258">Esta propiedad solo tiene efecto si la propiedad **DeviceRedirectionType** tiene un valor de "2".</span><span class="sxs-lookup"><span data-stu-id="a4d02-258">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-259">**SecureIdAllowed**</span><span class="sxs-lookup"><span data-stu-id="a4d02-259">**SecureIdAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-260">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-260">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-262">Indica si se puede usar un identificador seguro para conectarse al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a4d02-262">Indicates if a secure identifier can be used to connect to the RD Gateway server.</span></span>

<span data-ttu-id="a4d02-263">**Windows Server 2008:** Esta propiedad no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a4d02-263">**Windows Server 2008:** This property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-264">**SerialPortsDisabled**</span><span class="sxs-lookup"><span data-stu-id="a4d02-264">**SerialPortsDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-265">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-267">Indica si se deshabilitará la redirección de puertos serie.</span><span class="sxs-lookup"><span data-stu-id="a4d02-267">Indicates if serial port redirection will be disabled.</span></span> <span data-ttu-id="a4d02-268">Esta propiedad solo tiene efecto si la propiedad **DeviceRedirectionType** tiene un valor de "2".</span><span class="sxs-lookup"><span data-stu-id="a4d02-268">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-269">**SessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="a4d02-269">**SessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-270">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4d02-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-272">El valor de tiempo de espera de la sesión, en minutos.</span><span class="sxs-lookup"><span data-stu-id="a4d02-272">The session timeout value, in minutes.</span></span> <span data-ttu-id="a4d02-273">Un valor de 0 significa que no hay tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="a4d02-273">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="a4d02-274">Esta propiedad se puede establecer mediante el método [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="a4d02-274">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="a4d02-275">**Windows Server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a4d02-275">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-276">**SessionTimeoutAction**</span><span class="sxs-lookup"><span data-stu-id="a4d02-276">**SessionTimeoutAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-277">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4d02-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-279">Especifica la acción que se va a realizar en caso de que se agote el tiempo de espera de una sesión.</span><span class="sxs-lookup"><span data-stu-id="a4d02-279">Specifies the action to be taken in the case of a session timeout.</span></span> <span data-ttu-id="a4d02-280">Esta propiedad se puede establecer mediante el método [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="a4d02-280">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="a4d02-281">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a4d02-281">This can be one of the following values.</span></span>

<span data-ttu-id="a4d02-282">**Windows Server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a4d02-282">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="a4d02-283">0</span><span class="sxs-lookup"><span data-stu-id="a4d02-283">0</span></span>
</dt> <dd>

<span data-ttu-id="a4d02-284">Desconecte la sesión.</span><span class="sxs-lookup"><span data-stu-id="a4d02-284">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-285">1</span><span class="sxs-lookup"><span data-stu-id="a4d02-285">1</span></span>
</dt> <dd>

<span data-ttu-id="a4d02-286">Intente volver a autorizar la sesión.</span><span class="sxs-lookup"><span data-stu-id="a4d02-286">Attempt to re-authorize the session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a4d02-287">**SmartcardAllowed**</span><span class="sxs-lookup"><span data-stu-id="a4d02-287">**SmartcardAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-288">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a4d02-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-290">Indica si se puede usar una tarjeta inteligente para conectarse al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a4d02-290">Indicates if a smart card can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="a4d02-291">Esta propiedad se puede cambiar mediante el método [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="a4d02-291">This property can be changed by using the [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="a4d02-292">**UserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="a4d02-292">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d02-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a4d02-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4d02-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a4d02-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d02-295">Lista de nombres de grupos de usuarios separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="a4d02-295">List of semicolon-separated user group names.</span></span> <span data-ttu-id="a4d02-296">Los nombres tienen el formato *dominio \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="a4d02-296">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="a4d02-297">Si el usuario pertenece a alguno de estos grupos de usuarios, se le permitirá el acceso al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a4d02-297">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4d02-298">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4d02-298">Remarks</span></span>

<span data-ttu-id="a4d02-299">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="a4d02-299">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="a4d02-300">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a4d02-300">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a4d02-301">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a4d02-301">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a4d02-302">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a4d02-302">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a4d02-303">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a4d02-303">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4d02-304">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4d02-304">Requirements</span></span>



| <span data-ttu-id="a4d02-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4d02-305">Requirement</span></span> | <span data-ttu-id="a4d02-306">Value</span><span class="sxs-lookup"><span data-stu-id="a4d02-306">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d02-307">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4d02-307">Minimum supported client</span></span><br/> | <span data-ttu-id="a4d02-308">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a4d02-308">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a4d02-309">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4d02-309">Minimum supported server</span></span><br/> | <span data-ttu-id="a4d02-310">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4d02-310">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a4d02-311">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a4d02-311">Namespace</span></span><br/>                | <span data-ttu-id="a4d02-312">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a4d02-312">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a4d02-313">MOF</span><span class="sxs-lookup"><span data-stu-id="a4d02-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4d02-314"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4d02-314"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4d02-315">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a4d02-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4d02-316"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4d02-316"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a4d02-317">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4d02-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d02-318">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="a4d02-318">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="a4d02-319">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="a4d02-319">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="a4d02-320">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="a4d02-320">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="a4d02-321">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="a4d02-321">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="a4d02-322">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="a4d02-322">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="a4d02-323">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="a4d02-323">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

