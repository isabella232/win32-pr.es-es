---
title: Win32_TerminalServiceSetting (clase)
description: Representa la configuración de un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 4cd047db-921f-4ccb-946b-d2c7b8d6beea
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TerminalServiceSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting.Caption
- Win32_TerminalServiceSetting.Description
- Win32_TerminalServiceSetting.InstallDate
- Win32_TerminalServiceSetting.Name
- Win32_TerminalServiceSetting.Status
- Win32_TerminalServiceSetting.ServerName
- Win32_TerminalServiceSetting.TerminalServerMode
- Win32_TerminalServiceSetting.GetCapabilitiesID
- Win32_TerminalServiceSetting.LicensingType
- Win32_TerminalServiceSetting.PolicySourceLicensingType
- Win32_TerminalServiceSetting.PossibleLicensingTypes
- Win32_TerminalServiceSetting.LicensingName
- Win32_TerminalServiceSetting.LicensingDescription
- Win32_TerminalServiceSetting.ActiveDesktop
- Win32_TerminalServiceSetting.UserPermission
- Win32_TerminalServiceSetting.DeleteTempFolders
- Win32_TerminalServiceSetting.PolicySourceDeleteTempFolders
- Win32_TerminalServiceSetting.UseTempFolders
- Win32_TerminalServiceSetting.PolicySourceUseTempFolders
- Win32_TerminalServiceSetting.AllowTSConnections
- Win32_TerminalServiceSetting.PolicySourceAllowTSConnections
- Win32_TerminalServiceSetting.SingleSession
- Win32_TerminalServiceSetting.PolicySourceSingleSession
- Win32_TerminalServiceSetting.ProfilePath
- Win32_TerminalServiceSetting.PolicySourceProfilePath
- Win32_TerminalServiceSetting.HomeDirectory
- Win32_TerminalServiceSetting.PolicySourceHomeDirectory
- Win32_TerminalServiceSetting.TimeZoneRedirection
- Win32_TerminalServiceSetting.PolicySourceTimeZoneRedirection
- Win32_TerminalServiceSetting.Logons
- Win32_TerminalServiceSetting.DirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceDirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceConfiguredLicenseServers
- Win32_TerminalServiceSetting.DisableForcibleLogoff
- Win32_TerminalServiceSetting.PolicySourceDisableForcibleLogoff
- Win32_TerminalServiceSetting.FallbackPrintDriverType
- Win32_TerminalServiceSetting.PolicySourceFallbackPrintDriverType
- Win32_TerminalServiceSetting.SessionBrokerDrainMode
- Win32_TerminalServiceSetting.LimitedUserSessions
- Win32_TerminalServiceSetting.EnableDFSS
- Win32_TerminalServiceSetting.PolicySourceEnableDFSS
- Win32_TerminalServiceSetting.EnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.PolicySourceEnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.EnableAutomaticReconnection
- Win32_TerminalServiceSetting.PolicySourceEnableAutomaticReconnection
- Win32_TerminalServiceSetting.UseRDEasyPrintDriver
- Win32_TerminalServiceSetting.PolicySourceUseRDEasyPrintDriver
- Win32_TerminalServiceSetting.RedirectSmartCards
- Win32_TerminalServiceSetting.PolicySourceRedirectSmartCards
- Win32_TerminalServiceSetting.EnableDiskFSS
- Win32_TerminalServiceSetting.EnableNetworkFSS
- Win32_TerminalServiceSetting.NetworkFSSUserSessionWeight
- Win32_TerminalServiceSetting.NetworkFSSLocalSystemWeight
- Win32_TerminalServiceSetting.NetworkFSSCatchAllWeight
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f02028a331a3688152a1ce8c57ada7269d07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359821"
---
# <a name="win32_terminalservicesetting-class"></a><span data-ttu-id="4d5b9-105">\_Clase Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="4d5b9-105">Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="4d5b9-106">La clase WMI **\_ TerminalServiceSetting de Win32** representa la configuración de un servidor host de sesión de escritorio remoto (host escritorio remoto de sesión de RD).</span><span class="sxs-lookup"><span data-stu-id="4d5b9-106">The **Win32\_TerminalServiceSetting** WMI class represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="4d5b9-107">La configuración incluye capacidades como el modo de servidor host de sesión de escritorio remoto, licencias, Active Desktop, permisos, eliminación de carpetas temporales y directorios temporales para las sesiones.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-107">Settings include capabilities such as RD Session Host server mode, licensing, Active Desktop, permissions, deletion of temporary folders, and temporary directories for sessions.</span></span>

<span data-ttu-id="4d5b9-108">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-108">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="4d5b9-109">Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-109">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d5b9-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d5b9-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICESETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   ServerName;
  uint32   TerminalServerMode;
  uint32   GetCapabilitiesID;
  uint32   LicensingType;
  uint32   PolicySourceLicensingType;
  uint32   PossibleLicensingTypes;
  string   LicensingName;
  string   LicensingDescription;
  uint32   ActiveDesktop;
  uint32   UserPermission;
  uint32   DeleteTempFolders;
  uint32   PolicySourceDeleteTempFolders;
  uint32   UseTempFolders;
  uint32   PolicySourceUseTempFolders;
  uint32   AllowTSConnections;
  uint32   PolicySourceAllowTSConnections;
  uint32   SingleSession;
  uint32   PolicySourceSingleSession;
  string   ProfilePath;
  uint32   PolicySourceProfilePath;
  string   HomeDirectory;
  uint32   PolicySourceHomeDirectory;
  uint32   TimeZoneRedirection;
  uint32   PolicySourceTimeZoneRedirection;
  string   Logons;
  string   DirectConnectLicenseServers;
  uint32   PolicySourceDirectConnectLicenseServers;
  uint32   PolicySourceConfiguredLicenseServers;
  uint32   DisableForcibleLogoff;
  uint32   PolicySourceDisableForcibleLogoff;
  uint32   FallbackPrintDriverType;
  uint32   PolicySourceFallbackPrintDriverType;
  uint32   SessionBrokerDrainMode;
  uint32   LimitedUserSessions;
  uint32   EnableDFSS;
  uint32   PolicySourceEnableDFSS;
  uint32   EnableRemoteDesktopMSI;
  uint32   PolicySourceEnableRemoteDesktopMSI;
  uint32   EnableAutomaticReconnection;
  uint32   PolicySourceEnableAutomaticReconnection;
  uint32   UseRDEasyPrintDriver;
  uint32   PolicySourceUseRDEasyPrintDriver;
  uint32   RedirectSmartCards;
  uint32   PolicySourceRedirectSmartCards;
  uint32   EnableDiskFSS;
  uint32   EnableNetworkFSS;
  uint32   NetworkFSSUserSessionWeight;
  uint32   NetworkFSSLocalSystemWeight;
  uint32   NetworkFSSCatchAllWeight;
};
```

## <a name="members"></a><span data-ttu-id="4d5b9-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d5b9-111">Members</span></span>

<span data-ttu-id="4d5b9-112">La **clase \_ TerminalServiceSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4d5b9-112">The **Win32\_TerminalServiceSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="4d5b9-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d5b9-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="4d5b9-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d5b9-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4d5b9-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d5b9-115">Methods</span></span>

<span data-ttu-id="4d5b9-116">La clase **Win32 \_ TerminalServiceSetting** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-116">The **Win32\_TerminalServiceSetting** class has these methods.</span></span>



| <span data-ttu-id="4d5b9-117">Método</span><span class="sxs-lookup"><span data-stu-id="4d5b9-117">Method</span></span>                                                                                                                | <span data-ttu-id="4d5b9-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d5b9-118">Description</span></span>                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d5b9-119">**AddDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-119">**AddDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | <span data-ttu-id="4d5b9-120">Configura un nuevo servidor de licencias en la empresa.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-120">Configures a new license server in the enterprise.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="4d5b9-121">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-121">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | <span data-ttu-id="4d5b9-122">Agrega el servidor de licencias especificado al final de la lista de servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-122">Adds the given license server to the end of the list of specified license servers.</span></span><br/>                                                                                  |
| [<span data-ttu-id="4d5b9-123">**CanAccessLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-123">**CanAccessLicenseServer**</span></span>](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | <span data-ttu-id="4d5b9-124">Determina si el servidor host de sesión de escritorio remoto tiene permiso para solicitar Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS) desde un servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-124">Determines whether the RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="4d5b9-125">**ChangeMode**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-125">**ChangeMode**</span></span>](win32-terminalservicesetting-changemode.md)                                                         | <span data-ttu-id="4d5b9-126">Establece el tipo de licencia del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-126">Sets the licensing type of the Remote Desktop license server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="4d5b9-127">**CreateWinstation**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-127">**CreateWinstation**</span></span>](createwinstation-win32-terminalservicesetting.md)                                             | <span data-ttu-id="4d5b9-128">Crea una nueva pila de agentes de escucha basada en la combinación única de nombre del agente de escucha y NIC.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-128">Creates a new listener stack based on the unique combination of listener name and NIC.</span></span><br/>                                                                              |
| [<span data-ttu-id="4d5b9-129">**DeleteDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-129">**DeleteDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | <span data-ttu-id="4d5b9-130">Elimina el servidor de licencias especificado de la empresa.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-130">Deletes the specified license server from the enterprise.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="4d5b9-131">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | <span data-ttu-id="4d5b9-132">Quita todos los servidores de licencias de la lista de servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-132">Removes all license servers from the list of specified license servers.</span></span><br/>                                                                                             |
| [<span data-ttu-id="4d5b9-133">**FindLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-133">**FindLicenseServers**</span></span>](findlicenseservers-win32-terminalservicesetting.md)                                         | <span data-ttu-id="4d5b9-134">Enumera todos los servidores de licencias de Escritorio remoto y el método de detección.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-134">Enumerates all of the Remote Desktop license servers and the method of discovery.</span></span><br/>                                                                                   |
| [<span data-ttu-id="4d5b9-135">**GetDomain**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-135">**GetDomain**</span></span>](getdomain-win32-terminalservicesetting.md)                                                           | <span data-ttu-id="4d5b9-136">Recupera el nombre del dominio del que es miembro el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-136">Retrieves the name of the domain that the RD Session Host server is a member of.</span></span><br/>                                                                                    |
| [<span data-ttu-id="4d5b9-137">**GetGracePeriodDays**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-137">**GetGracePeriodDays**</span></span>](getgraceperioddays-win32-terminalservicesetting.md)                                         | <span data-ttu-id="4d5b9-138">Recupera el número de días que quedan en el período de gracia de la licencia de escritorio remoto para un servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-138">Retrieves the number of days that are remaining in the RD Licensing grace period for an RD Session Host server.</span></span><br/>                                                     |
| [<span data-ttu-id="4d5b9-139">**GetRegisteredLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-139">**GetRegisteredLicenseServerList**</span></span>](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | <span data-ttu-id="4d5b9-140">Obtiene la lista de servidores de licencias registrados.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-140">Gets the list of registered license servers.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="4d5b9-141">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-141">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="4d5b9-142">Recupera la lista de servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-142">Retrieves the list of specified license servers.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="4d5b9-143">**GetTSLanaIds**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-143">**GetTSLanaIds**</span></span>](gettslanaids-win32-terminalservicesetting.md)                                                     | <span data-ttu-id="4d5b9-144">Obtiene los identificadores y descripciones de Servicios de Escritorio remoto adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-144">Gets the IDs and descriptions of Remote Desktop Services network adapters.</span></span><br/>                                                                                          |
| [<span data-ttu-id="4d5b9-145">**GetTStoLSConnectivityStatus**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-145">**GetTStoLSConnectivityStatus**</span></span>](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | <span data-ttu-id="4d5b9-146">Determina el estado de conectividad entre Servicios de Escritorio remoto y un servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-146">Determines the connectivity status between Remote Desktop Services and a license server.</span></span><br/>                                                                            |
| [<span data-ttu-id="4d5b9-147">**GetWinstationDriverNames**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-147">**GetWinstationDriverNames**</span></span>](getwinstationdrivernames-win32-terminalservicesetting.md)                             | <span data-ttu-id="4d5b9-148">Recupera una lista de los nombres de controlador de la estación de la.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-148">Retrieves a list of Winstation driver names.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="4d5b9-149">**PingLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-149">**PingLicenseServer**</span></span>](pinglicenseserver-win32-terminalservicesetting.md)                                           | <span data-ttu-id="4d5b9-150">Hace ping en el servidor de licencias para determinar si se trata de un servidor de licencias válido.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-150">Pings the license server to determine whether it is a valid license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="4d5b9-151">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-151">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | <span data-ttu-id="4d5b9-152">Quita el servidor de licencias dado de la lista de servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-152">Removes the given license server from the list of specified license servers.</span></span><br/>                                                                                        |
| [<span data-ttu-id="4d5b9-153">**SetAllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-153">**SetAllowTSConnections**</span></span>](win32-terminalservicesetting-setallowtsconnections.md)                                   | <span data-ttu-id="4d5b9-154">Establece la propiedad **AllowTSConnections** .</span><span class="sxs-lookup"><span data-stu-id="4d5b9-154">Sets the **AllowTSConnections** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="4d5b9-155">**SetDisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-155">**SetDisableForcibleLogoff**</span></span>](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | <span data-ttu-id="4d5b9-156">Establece la propiedad **DisableForcibleLogoff** .</span><span class="sxs-lookup"><span data-stu-id="4d5b9-156">Sets the **DisableForcibleLogoff** property.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="4d5b9-157">**SetFallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-157">**SetFallbackPrintDriverType**</span></span>](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | <span data-ttu-id="4d5b9-158">Establece la propiedad **FallbackPrintDriverType** .</span><span class="sxs-lookup"><span data-stu-id="4d5b9-158">Sets the **FallbackPrintDriverType** property.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="4d5b9-159">**SetHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-159">**SetHomeDirectory**</span></span>](win32-terminalservicesetting-sethomedirectory.md)                                             | <span data-ttu-id="4d5b9-160">Establece la propiedad **HomeDirectory** .</span><span class="sxs-lookup"><span data-stu-id="4d5b9-160">Sets the **HomeDirectory** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="4d5b9-161">**SetPolicyPropertyName**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-161">**SetPolicyPropertyName**</span></span>](win32-terminalservicesetting-setpolicypropertyname.md)                                   | <span data-ttu-id="4d5b9-162">Establece una de las propiedades siguientes: **DeleteTempFolders** o **UseTempFolders**.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-162">Sets one of the following properties: **DeleteTempFolders** or **UseTempFolders**.</span></span><br/>                                                                                  |
| [<span data-ttu-id="4d5b9-163">**SetPrimaryLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-163">**SetPrimaryLicenseServer**</span></span>](setprimarylicenseserver-win32-terminalservicesetting.md)                               | <span data-ttu-id="4d5b9-164">Establece el servidor de licencias dado como la primera entrada de la lista de servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-164">Sets the given license server as the first entry in the list of specified license servers.</span></span><br/>                                                                          |
| [<span data-ttu-id="4d5b9-165">**SetProfilePath**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-165">**SetProfilePath**</span></span>](win32-terminalservicesetting-setprofilepath.md)                                                 | <span data-ttu-id="4d5b9-166">Establece la propiedad **ProfilePath** .</span><span class="sxs-lookup"><span data-stu-id="4d5b9-166">Sets the **ProfilePath** property.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="4d5b9-167">**SetSingleSession**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-167">**SetSingleSession**</span></span>](win32-terminalservicesetting-setsinglesession.md)                                             | <span data-ttu-id="4d5b9-168">Establece la propiedad **SingleSession** .</span><span class="sxs-lookup"><span data-stu-id="4d5b9-168">Sets the **SingleSession** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="4d5b9-169">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-169">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="4d5b9-170">Actualiza la lista de servidores de licencias especificados, reemplazando los servidores de licencias especificados.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-170">Updates the list of specified license servers, replacing any existing specified license servers.</span></span><br/>                                                                    |
| [<span data-ttu-id="4d5b9-171">**SetTimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-171">**SetTimeZoneRedirection**</span></span>](win32-terminalservicesetting-settimezoneredirection.md)                                 | <span data-ttu-id="4d5b9-172">Establece la propiedad **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="4d5b9-172">Sets the **TimeZoneRedirection** property.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="4d5b9-173">**UpdateDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-173">**UpdateDirectConnectLicenseServer**</span></span>](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | <span data-ttu-id="4d5b9-174">Actualiza la lista de servidores de licencias de detección.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-174">Updates the list of discovery license servers.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="4d5b9-175">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d5b9-175">Properties</span></span>

<span data-ttu-id="4d5b9-176">La **clase \_ TerminalServiceSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-176">The **Win32\_TerminalServiceSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d5b9-177">**ActiveDesktop**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-177">**ActiveDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-178">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-179">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-180">Especifica si se permite Active Desktop en cada sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-180">Specifies whether Active Desktop is allowed in each user session.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="4d5b9-181"><span id="TRUE"></span><span id="true"></span>**True** (0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-181"><span id="TRUE"></span><span id="true"></span>**TRUE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-182">Active Desktop no se permite en cada sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-182">Active Desktop is not allowed in each user session.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="4d5b9-183"><span id="FALSE"></span><span id="false"></span>**False** (1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-183"><span id="FALSE"></span><span id="false"></span>**FALSE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-184">Active Desktop se permite en cada sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-184">Active Desktop is allowed in each user session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-185">**AllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-185">**AllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-186">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-188">Especifica si se permiten nuevas conexiones Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-188">Specifies whether new Remote Desktop Services connections are allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="4d5b9-189"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-189"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-190">No se permiten nuevas conexiones.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-190">New connections are not allowed.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="4d5b9-191"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-191"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-192">Se permiten nuevas conexiones.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-192">New connections are allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-193">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-196">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-197">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-197">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="4d5b9-198">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d5b9-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-199">**DeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-199">**DeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-200">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-202">Especifica si los directorios temporales se eliminan al salir.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-202">Specifies whether temporary directories are deleted on exit.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="4d5b9-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-204">La eliminación de directorios temporales está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-204">Deletion of temporary directories is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="4d5b9-205"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-206">La eliminación de directorios temporales está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-206">Deletion of temporary directories is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-207">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-210">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-210">Description of the object.</span></span>

<span data-ttu-id="4d5b9-211">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d5b9-211">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-212">**DirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-212">**DirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-215">Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-215">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-216">Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-216">This property is not available.</span></span>

<span data-ttu-id="4d5b9-217">**Windows Server 2008:** Enumera la lista de servidores de licencias.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-217">**Windows Server 2008:** Enumerates the list of license servers.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-218">**DisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-218">**DisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-219">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-219">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-221">Determina si un administrador que ha iniciado sesión en la consola de se puede cerrar la sesión forzosamente.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-221">Determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span data-ttu-id="4d5b9-222">0</span><span class="sxs-lookup"><span data-stu-id="4d5b9-222">0</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-223">El administrador puede cerrar la sesión con fuerza.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-223">Administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-224">1</span><span class="sxs-lookup"><span data-stu-id="4d5b9-224">1</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-225">No se puede cerrar la sesión del administrador forzosamente.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-225">Administrator cannot be forcibly logged off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-226">**EnableAutomaticReconnection**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-226">**EnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-227">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-228">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-229">Especifica si se permite que los clientes de conexión de Escritorio remoto se vuelvan a conectar automáticamente a las sesiones de un servidor host de sesión de escritorio remoto si el vínculo de red se pierde temporalmente.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-229">Specifies whether to allow Remote Desktop connection clients to automatically reconnect to sessions on an RD Session Host server if the network link is temporarily lost.</span></span>

<dt>

<span data-ttu-id="4d5b9-230">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-230">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-231">La reconexión automática está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-231">Automatic reconnection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-232">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-232">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-233">La reconexión automática está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-233">Automatic reconnection is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="4d5b9-234">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-234">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-235">**EnableDFSS**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-235">**EnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-236">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-237">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-238">Indica si la programación dinámica de recursos compartidos (DFSS) está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-238">Indicates whether dynamic fair-share scheduling (DFSS) is enabled or disabled.</span></span> <span data-ttu-id="4d5b9-239">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-239">This can be one of the following values.</span></span>

<span data-ttu-id="4d5b9-240">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-240">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="4d5b9-241">0</span><span class="sxs-lookup"><span data-stu-id="4d5b9-241">0</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-242">DFSS está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-242">DFSS is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-243">1</span><span class="sxs-lookup"><span data-stu-id="4d5b9-243">1</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-244">DFSS está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-244">DFSS is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-245">**EnableDiskFSS**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-245">**EnableDiskFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-246">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-247">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-247">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-248">Especifica si está habilitada la programación de recursos compartidos de disco.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-248">Specifies if disk fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="4d5b9-249">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-249">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-250">La programación de la cuota de disco equilibrada está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-250">Disk fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-251">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-251">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-252">Está habilitada la programación de recursos compartidos de disco.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-252">Disk fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="4d5b9-253">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-253">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-254">**EnableNetworkFSS**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-254">**EnableNetworkFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-255">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-256">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-256">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-257">Especifica si está habilitada la programación de recursos compartidos de red.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-257">Specifies if network fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="4d5b9-258">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-258">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-259">La programación de proporcionalidad equilibrada de red está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-259">Network fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-260">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-260">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-261">La programación de proporcionalidad equilibrada de red está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-261">Network fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="4d5b9-262">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-262">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-263">**EnableRemoteDesktopMSI**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-263">**EnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-264">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-265">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-266">Indica si la Escritorio remoto MSI está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-266">Indicates whether the Remote Desktop MSI is enabled or disabled.</span></span>

<dt>

<span data-ttu-id="4d5b9-267">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-267">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-268">Disabled</span><span class="sxs-lookup"><span data-stu-id="4d5b9-268">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-269">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-269">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-270">habilitado</span><span class="sxs-lookup"><span data-stu-id="4d5b9-270">Enabled</span></span>

</dd> </dl>

<span data-ttu-id="4d5b9-271">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-271">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-272">**FallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-272">**FallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-273">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-275">Especifica el controlador de impresora al que se va a retrasar.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-275">Specifies which printer driver to fallback to.</span></span>

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span data-ttu-id="4d5b9-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**No dirvers de reserva = 0** (0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**No fallback dirvers=0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-277">No hay controladores de reserva.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-277">No fallback drivers.</span></span>

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span data-ttu-id="4d5b9-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Mejor estimación = 1** (1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Best guess=1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-279">Mejor aproximación.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-279">Best guess.</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span data-ttu-id="4d5b9-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Mejor estimación, si no se encuentra ninguna coincidencia, reserva a PCL = 2** (2)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Best guess, if no match is found fallback to PCL=2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-281">Mejor aproximación.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-281">Best guess.</span></span> <span data-ttu-id="4d5b9-282">Si no se encuentra ninguna coincidencia, retroceder a Hewlett-Packard el lenguaje de control de impresoras (PCL).</span><span class="sxs-lookup"><span data-stu-id="4d5b9-282">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span data-ttu-id="4d5b9-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Mejor estimación, si no se encuentra ninguna coincidencia, reserva a PS = 3** (3)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Best guess, if no match is found fallback to PS=3** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-284">Mejor aproximación.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-284">Best guess.</span></span> <span data-ttu-id="4d5b9-285">Si no se encuentra ninguna coincidencia, retroceder a PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="4d5b9-285">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span data-ttu-id="4d5b9-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Mejor suposición, si no se encuentra ninguna coincidencia, mostrar los controladores PCL y PS = 4** (4)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Best guess, if no match is found show both PCL and PS drivers=4** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-287">Mejor aproximación.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-287">Best guess.</span></span> <span data-ttu-id="4d5b9-288">Si no se encuentra ninguna coincidencia, muestre los controladores PS y PCL.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-288">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-289">**GetCapabilitiesID**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-289">**GetCapabilitiesID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-290">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-292">IDENTIFICADOR de funcionalidad del proveedor.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-292">Capabilities ID for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-293">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-293">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-294">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-296">Directorio raíz del equipo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-296">The root directory for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-298">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-300">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="4d5b9-300">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-301">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-301">The date the object was installed.</span></span> <span data-ttu-id="4d5b9-302">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-302">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4d5b9-303">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d5b9-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-304">**LicensingDescription**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-304">**LicensingDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-305">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-307">Breve descripción del modo de licencia.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-307">A brief description of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-308">**LicensingName**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-308">**LicensingName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-311">Nombre del modo de licencia.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-311">The name of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-312">**LicensingType**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-312">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-313">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-315">El tipo de licencia para el modo de servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-315">The licensing type for the specified server mode.</span></span>

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span data-ttu-id="4d5b9-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Terminal Server personal** (0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Personal Terminal Server** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-317">Servidor host de sesión de escritorio remoto personal.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-317">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span data-ttu-id="4d5b9-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Escritorio remoto para la administración** (1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Remote Desktop for Administration** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-319">Escritorio remoto para la administración.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-319">Remote Desktop for Administration.</span></span>

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="4d5b9-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Por dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Per Device** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-321">Por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-321">Per Device.</span></span> <span data-ttu-id="4d5b9-322">Válido para los servidores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-322">Valid for application servers.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="4d5b9-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuario** (3)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-324">Por usuario.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-324">Per User.</span></span> <span data-ttu-id="4d5b9-325">Válido para los servidores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-325">Valid for application servers.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="4d5b9-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (4)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-327">No configurado.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-327">Not Configured.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-328">**LimitedUserSessions**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-328">**LimitedUserSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-329">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-330">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-330">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-331">Indica si la característica para limitar el número de sesiones activas e inactivas que se permiten en un servidor host de sesión de escritorio remoto está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-331">Indicates whether the feature to limit the number of both active and inactive sessions that are allowed on an RD Session Host server is enabled.</span></span> <span data-ttu-id="4d5b9-332">Por ejemplo, puede que desee establecer **LimitedUserSessions** para garantizar el cumplimiento de las licencias para una aplicación concreta que está instalada en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-332">For example, you may want to set **LimitedUserSessions** to guarantee license compliance for a particular application that is installed on the RD Session Host server.</span></span> <span data-ttu-id="4d5b9-333">O bien, puede que desee limitar el número máximo de sesiones en un servidor host de sesión de escritorio remoto en una granja de servidores con equilibrio de carga, de modo que el servidor no se sobrecargue si se produce un error en otro servidor de la granja.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-333">Or, you may want to limit the maximum number of sessions on an RD Session Host server in a load-balanced farm so that the server will not be overloaded if another server in the farm fails.</span></span>

> [!Note]
>
> <span data-ttu-id="4d5b9-334">La sesión que se usa para conectarse al servidor con fines administrativos no se ve afectada por **LimitedUserSessions**.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-334">The session that is used to connect to the server for administrative purposes is not affected by **LimitedUserSessions**.</span></span>
>
> <span data-ttu-id="4d5b9-335">En una granja de servidores host de sesión de escritorio remoto, si un usuario supera el límite de sesión, la sesión se dirigirá a otro servidor mediante el equilibrio de carga del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-335">In an RD Session Host server farm, if a user exceeds the session limit, the session will be directed to another server by RD Connection Broker load balancing.</span></span> <span data-ttu-id="4d5b9-336">Si el servidor es un servidor independiente, el usuario no podrá conectarse.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-336">If the server is a stand-alone server, the user will not be able to connect.</span></span>
>
> <span data-ttu-id="4d5b9-337">Debido a la sesión que se usa para conectarse al servidor con fines administrativos, y a la temporización de la aplicación del número de sesiones durante el ciclo de inicio de sesión, se recomienda establecer **LimitedUserSessions** en un valor que sea ligeramente inferior al límite físico para el número de sesiones en un servidor.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-337">Because of the session that is used to connect to the server for administrative purposes, and the timing of the enforcement of the number of sessions during the logon cycle, it is recommended that you set **LimitedUserSessions** to a value that is slightly lower that the physical limit for the number of sessions on a server.</span></span>
>
> <span data-ttu-id="4d5b9-338">La propiedad **LimitedUserSessions** solo es válida si está instalado el servicio de rol host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-338">The **LimitedUserSessions** property is only valid if the RD Session Host role service is installed.</span></span>

 

<dt>

<span data-ttu-id="4d5b9-339">0</span><span class="sxs-lookup"><span data-stu-id="4d5b9-339">0</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-340">Esta función está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-340">The feature is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-341">1 o superior</span><span class="sxs-lookup"><span data-stu-id="4d5b9-341">1 or greater</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-342">Un valor de uno o más representa el número máximo de sesiones (activas e inactivas) que se permiten en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-342">A value of one or greater represents the maximum number of sessions (both active and inactive) that are allowed on the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-343">**Inicios**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-343">**Logons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-344">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-345">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-345">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-346">Especifica si se permiten las nuevas sesiones.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-346">Specifies whether new sessions are allowed.</span></span> <span data-ttu-id="4d5b9-347">Esta configuración no afecta a la configuración existente.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-347">This setting does not affect existing settings.</span></span>

<dt>

<span data-ttu-id="4d5b9-348">0</span><span class="sxs-lookup"><span data-stu-id="4d5b9-348">0</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-349">Se permiten nuevas sesiones.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-349">New sessions are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-350">1</span><span class="sxs-lookup"><span data-stu-id="4d5b9-350">1</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-351">No se permiten nuevas sesiones.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-351">New sessions are not allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-352">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-355">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-355">The name of the object.</span></span>

<span data-ttu-id="4d5b9-356">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d5b9-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-357">**NetworkFSSCatchAllWeight**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-357">**NetworkFSSCatchAllWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-358">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-359">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-359">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-360">Especifica el peso de la cuota equitativa predeterminada de red para el tráfico de red comodín.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-360">Specifies the default network fair share weight for catch-all network traffic.</span></span> <span data-ttu-id="4d5b9-361">Los valores válidos son de 1 a 9.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-361">Valid values are 1 to 9.</span></span>

<span data-ttu-id="4d5b9-362">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-362">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-363">**NetworkFSSLocalSystemWeight**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-363">**NetworkFSSLocalSystemWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-364">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-365">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-365">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-366">Especifica el peso de la cuota equitativa predeterminada de red para un proceso del sistema local.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-366">Specifies the default network fair share weight for a local system processes.</span></span> <span data-ttu-id="4d5b9-367">Los valores válidos son de 1 a 9.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-367">Valid values are 1 to 9.</span></span>

<span data-ttu-id="4d5b9-368">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-368">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-369">**NetworkFSSUserSessionWeight**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-369">**NetworkFSSUserSessionWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-370">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-371">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-371">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-372">Especifica el peso de la cuota equitativa predeterminada de red para una sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-372">Specifies the default network fair share weight for a user session.</span></span> <span data-ttu-id="4d5b9-373">Los valores válidos son de 1 a 9.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-373">Valid values are 1 to 9.</span></span>

<span data-ttu-id="4d5b9-374">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-374">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-375">**PolicySourceAllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-375">**PolicySourceAllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-376">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-378">Indica si la propiedad **AllowTSConnections** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-378">Indicates whether the **AllowTSConnections** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-379">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-379">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-380">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-380">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-381">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-381">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-382">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-382">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-383">**PolicySourceConfiguredLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-383">**PolicySourceConfiguredLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-384">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-384">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-386">Indica si los servidores de licencias devueltos por el método [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) están configurados por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-386">Indicates whether the license servers returned by the [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) method are configured by the server or by group policy.</span></span>

<span data-ttu-id="4d5b9-387">**Windows Server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-387">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="4d5b9-388">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-388">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-389">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-389">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-390">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-390">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-391">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-391">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-392">**PolicySourceDeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-392">**PolicySourceDeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-393">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-395">Indica si la propiedad **DeleteTempFolders** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-395">Indicates whether the **DeleteTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-396">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-396">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-397">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-397">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-398">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-398">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-399">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-399">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-400">**PolicySourceDirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-400">**PolicySourceDirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-401">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-401">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-403">Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-403">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-404">Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-404">This property is not available.</span></span>

<span data-ttu-id="4d5b9-405">**Windows Server 2008:** Indica si la propiedad **DirectConnectLicenseServers** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-405">**Windows Server 2008:** Indicates whether the **DirectConnectLicenseServers** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-406">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-406">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-407">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-407">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-408">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-408">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-409">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-409">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-410">**PolicySourceDisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-410">**PolicySourceDisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-411">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-412">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-413">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-413">This property is not supported.</span></span>

<span data-ttu-id="4d5b9-414">**Windows Server 2008:** Determina si la propiedad **DisableForcibleLogoff** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-414">**Windows Server 2008:** Determines whether the **DisableForcibleLogoff** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-415">0</span><span class="sxs-lookup"><span data-stu-id="4d5b9-415">0</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-416">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-416">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-417">1</span><span class="sxs-lookup"><span data-stu-id="4d5b9-417">1</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-418">Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-418">Group Policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-419">**PolicySourceEnableAutomaticReconnection**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-419">**PolicySourceEnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-420">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-422">Indica si la propiedad **EnableAutomaticReconnection** está configurada por el servidor o la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-422">Indicates whether the **EnableAutomaticReconnection** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-423">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-424">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-426">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-426">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="4d5b9-427">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-427">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-428">**PolicySourceEnableDFSS**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-428">**PolicySourceEnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-429">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-431">Indica si la propiedad **EnableDFSS** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-431">Indicates whether the **EnableDFSS** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-432">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-432">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-433">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-433">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-434">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-434">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-435">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-435">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="4d5b9-436">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-436">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-437">**PolicySourceEnableRemoteDesktopMSI**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-437">**PolicySourceEnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-438">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-439">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-440">Indica si la propiedad **EnableRemoteDesktopMSI** está configurada por el servidor o la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-440">Indicates whether the **EnableRemoteDesktopMSI** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-441">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-441">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-442">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-442">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-443">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-443">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-444">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-444">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="4d5b9-445">**Windows Server 2008:** Esta propiedad no está disponible antes de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-445">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-446">**PolicySourceFallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-446">**PolicySourceFallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-447">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-447">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-448">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-449">Indica si la propiedad **FallbackPrintDriverType** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-449">Indicates whether the **FallbackPrintDriverType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-450">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-450">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-451">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-451">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-452">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-452">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-453">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-453">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-454">**PolicySourceHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-454">**PolicySourceHomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-455">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-455">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-456">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-457">Indica si la propiedad **HomeDirectory** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-457">Indicates whether the **HomeDirectory** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-458">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-458">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-459">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-459">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-460">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-460">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-461">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-461">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-462">**PolicySourceLicensingType**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-462">**PolicySourceLicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-463">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-464">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-465">Indica si la propiedad **LicensingType** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-465">Indicates whether the **LicensingType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-466">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-466">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-467">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-467">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-468">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-468">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-469">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-469">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-470">**PolicySourceProfilePath**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-470">**PolicySourceProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-471">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-473">Indica si la propiedad **ProfilePath** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-473">Indicates whether the **ProfilePath** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-474">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-474">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-475">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-475">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-476">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-476">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-477">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-477">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-478">**PolicySourceRedirectSmartCards**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-478">**PolicySourceRedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-479">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-479">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-480">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-481">Indica si la propiedad **RedirectSmartCards** está configurada por el servidor o la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-481">Indicates whether the **RedirectSmartCards** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-482">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-482">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-483">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-483">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-484">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-484">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-485">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-485">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="4d5b9-486">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-486">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-487">**PolicySourceSingleSession**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-487">**PolicySourceSingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-488">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-489">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-490">Indica si la propiedad **SingleSession** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-490">Indicates whether the property **SingleSession** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-491">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-491">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-492">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-492">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-493">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-493">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-494">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-494">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-495">**PolicySourceTimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-495">**PolicySourceTimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-496">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-497">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-498">Indica si la propiedad **TimeZoneRedirection** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-498">Indicates whether the property **TimeZoneRedirection** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-499">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-499">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-500">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-500">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-501">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-501">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-502">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-502">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-503">**PolicySourceUseRDEasyPrintDriver**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-503">**PolicySourceUseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-504">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-505">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-506">Indica si la propiedad **UseRDEasyPrintDriver** está configurada por el servidor o la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-506">Indicates whether the **UseRDEasyPrintDriver** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-507">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-507">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-508">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-508">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-509">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-509">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-510">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-510">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="4d5b9-511">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-511">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-512">**PolicySourceUseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-512">**PolicySourceUseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-513">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-514">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-515">Indica si la propiedad **UseTempFolders** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-515">Indicates whether the **UseTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="4d5b9-516">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-516">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-517">Servidor</span><span class="sxs-lookup"><span data-stu-id="4d5b9-517">Server</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-518">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-518">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-519">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4d5b9-519">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-520">**PossibleLicensingTypes**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-520">**PossibleLicensingTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-521">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-522">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-523">Calificadores: [**mapa de bits**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("personal Terminal Server", "escritorio remoto para administración", "por dispositivo", "por usuario", "sin configurar")</span><span class="sxs-lookup"><span data-stu-id="4d5b9-523">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Personal Terminal Server", "Remote Desktop for Administration", "Per Device", "Per User", "Not Configured")</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-524">Máscara de máscara que especifica los tipos de licencia que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-524">A bitmask that specifies the licensing types that are available.</span></span> <span data-ttu-id="4d5b9-525">Puede ser una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-525">This can be a combination of one or more of the following values.</span></span>

<dt>

<span data-ttu-id="4d5b9-526">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-526">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-527">Se admiten licencias de servidor host de sesión de escritorio remoto personal.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-527">Personal RD Session Host server licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-528">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-528">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-529">Se admiten Escritorio remoto licencias.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-529">Remote Desktop licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-530">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-530">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-531">Se admiten licencias por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-531">Per device licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-532">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-532">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-533">Se admiten licencias por usuario.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-533">Per user licenses are supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-534">**ProfilePath**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-534">**ProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-535">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-536">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-537">Ruta de acceso del perfil para el equipo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-537">Profile path for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-538">**RedirectSmartCards**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-538">**RedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-539">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-540">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-540">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-541">Especifica si se permite la redirección de dispositivos de tarjeta inteligente en una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-541">Specifies if redirection of smart card devices is allowed in a remote session.</span></span>

<dt>

<span data-ttu-id="4d5b9-542">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-542">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-543">No se permite la redirección de dispositivos de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-543">Smart card device redirection is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-544">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-544">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-545">Se permite el redireccionamiento de dispositivos de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-545">Smart card device redirection is allowed.</span></span>

</dd> </dl>

<span data-ttu-id="4d5b9-546">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-546">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-547">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-547">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-548">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-549">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-550">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-550">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-551">Nombre del servidor host de sesión de escritorio remoto cuyas propiedades son de interés.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-551">Name of the RD Session Host server whose properties are of interest.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-552">**SessionBrokerDrainMode**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-552">**SessionBrokerDrainMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-553">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-553">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-554">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-555">El modo de inicio de sesión de usuario del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-555">The RD Connection Broker user logon mode.</span></span>

<dt>

<span data-ttu-id="4d5b9-556">0</span><span class="sxs-lookup"><span data-stu-id="4d5b9-556">0</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-557">Permitir todas las conexiones.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-557">Allow all connections.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-558">1</span><span class="sxs-lookup"><span data-stu-id="4d5b9-558">1</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-559">Permitir las reconexiones, pero impedir nuevos inicios de sesión hasta que se reinicie el servidor.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-559">Allow reconnections, but prevent new logons until the server is restarted.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-560">2</span><span class="sxs-lookup"><span data-stu-id="4d5b9-560">2</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-561">Permitir las reconexiones, pero impedir nuevos inicios de sesión.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-561">Allow reconnections, but prevent new logons.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-562">**SingleSession**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-562">**SingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-563">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-564">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-565">Especifica si se permiten una o varias sesiones de Servicios de Escritorio remoto por usuario.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-565">Specifies whether one or more Remote Desktop Services sessions are allowed per user.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="4d5b9-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-567">Se permite más de una sesión por usuario.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-567">More than one session is allowed per user.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="4d5b9-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-569">Solo se permite una sesión por usuario.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-569">Only one session is allowed per user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-570">**Estado**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-570">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-571">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-572">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-573">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-573">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-574">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-574">Current status of the object.</span></span> <span data-ttu-id="4d5b9-575">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-575">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4d5b9-576">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="4d5b9-576">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4d5b9-577">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="4d5b9-577">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4d5b9-578">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-578">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4d5b9-579">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-579">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4d5b9-580">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4d5b9-580">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="4d5b9-581">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="4d5b9-581">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d5b9-582">("Error")</span><span class="sxs-lookup"><span data-stu-id="4d5b9-582">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d5b9-583">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="4d5b9-583">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d5b9-584">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="4d5b9-584">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d5b9-585">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="4d5b9-585">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d5b9-586">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="4d5b9-586">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d5b9-587">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="4d5b9-587">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4d5b9-588">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="4d5b9-588">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-589">**TerminalServerMode**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-589">**TerminalServerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-590">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-591">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-592">Modo de funcionamiento del servidor host de sesión de escritorio remoto del servicio Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-592">The RD Session Host server operating mode of the Remote Desktop Services service.</span></span> <span data-ttu-id="4d5b9-593">Este modo controla las directivas de licencias que son aplicables y si están habilitadas las características de compatibilidad de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-593">This mode controls the licensing policies that are applicable as well as whether application-compatibility features are enabled.</span></span>

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span data-ttu-id="4d5b9-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-595">El servidor funciona como un servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-595">The server operates as an application server.</span></span>

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span data-ttu-id="4d5b9-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-597">La sesión se administra de forma remota.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-597">The session is administered remotely.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-598">**TimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-598">**TimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-599">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-599">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-600">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-600">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-601">Especifica si el equipo cliente puede redirigir su configuración de zona horaria a la sesión de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-601">Specifies whether the client computer can redirect its time zone settings to the Remote Desktop Services session.</span></span>

<dt>

<span data-ttu-id="4d5b9-602">0</span><span class="sxs-lookup"><span data-stu-id="4d5b9-602">0</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-603">La redirección está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-603">Redirection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-604">1</span><span class="sxs-lookup"><span data-stu-id="4d5b9-604">1</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-605">La redirección está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-605">Redirection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-606">**UseRDEasyPrintDriver**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-606">**UseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-607">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-607">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-608">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-608">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-609">Especifica si el controlador de impresora Easy Print de Escritorio remoto se utiliza en primer lugar para instalar todas las impresoras de cliente.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-609">Specifies whether the Remote Desktop Easy Print printer driver is used first to install all client printers.</span></span>

<dt>

<span data-ttu-id="4d5b9-610">0</span><span class="sxs-lookup"><span data-stu-id="4d5b9-610">0</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-611">El servidor host de sesión de escritorio remoto intenta encontrar un controlador de impresora adecuado para instalar la impresora de cliente.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-611">The RD Session Host server tries to find a suitable printer driver to install the client printer.</span></span> <span data-ttu-id="4d5b9-612">Si el servidor host de sesión de escritorio remoto no tiene un controlador de impresora que coincida con la impresora de cliente, el servidor intenta usar el controlador de Easy Print de Escritorio remoto para instalar la impresora de cliente.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-612">If the RD Session Host server does not have a printer driver that matches the client printer, the server tries to use the Remote Desktop Easy Print driver to install the client printer.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-613">1</span><span class="sxs-lookup"><span data-stu-id="4d5b9-613">1</span></span>
</dt> <dd>

<span data-ttu-id="4d5b9-614">El servidor host de sesión de escritorio remoto primero intenta usar el controlador de impresora Easy Print de Escritorio remoto para instalar todas las impresoras cliente.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-614">The RD Session Host server first tries to use the Remote Desktop Easy Print printer driver to install all client printers.</span></span> <span data-ttu-id="4d5b9-615">Si por alguna razón no se puede usar el controlador de impresora Easy Print de Escritorio remoto, se usa un controlador de impresora en el servidor host de sesión de escritorio remoto que coincida con la impresora cliente.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-615">If for any reason the Remote Desktop Easy Print printer driver cannot be used, a printer driver on the RD Session Host server that matches the client printer is used.</span></span>

</dd> </dl>

<span data-ttu-id="4d5b9-616">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-616">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4d5b9-617">**UserPermission**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-617">**UserPermission**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-618">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-618">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-619">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-619">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-620">Especifica si cada sesión de usuario tiene una seguridad estricta o relajada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-620">Specifies if each user session has tight or relaxed security.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="4d5b9-621"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-621"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-622">La seguridad es estrecha.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-622">Security is tight.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="4d5b9-623"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-623"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-624">La seguridad es relajada.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-624">Security is relaxed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4d5b9-625">**UseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-625">**UseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d5b9-626">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-626">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d5b9-627">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d5b9-627">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d5b9-628">Especifica si los directorios temporales se crean y se eliminan por sesión.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-628">Specifies whether temporary directories are created and deleted on a per-session basis.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="4d5b9-629"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-629"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-630">Los directorios temporales no se crean y eliminan para cada sesión.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-630">Temporary directories are not created and deleted for each session.</span></span> <span data-ttu-id="4d5b9-631">Se crea uno para la primera sesión y nunca se elimina.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-631">One is created for the first session and never deleted.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="4d5b9-632"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="4d5b9-632"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d5b9-633">Los directorios temporales se crean y se eliminan para cada sesión.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-633">Temporary directories are created and deleted for each session.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d5b9-634">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d5b9-634">Remarks</span></span>

<span data-ttu-id="4d5b9-635">**Win32 \_ TerminalServiceSetting** está asociado a [**Win32 \_ TerminalService**](win32-terminalservice.md) como la propiedad **Setting** de la [**Asociación \_ TerminalServiceToSetting de Win32**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="4d5b9-635">**Win32\_TerminalServiceSetting** is associated to [**Win32\_TerminalService**](win32-terminalservice.md) as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="4d5b9-636">[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) está asociado al [**\_ terminal de Win32**](win32-terminal.md) como la propiedad de **configuración** de la Asociación [**\_ TerminalTerminalSetting de Win32**](win32-terminalterminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="4d5b9-636">[**Win32\_TerminalSetting**](win32-terminalsetting.md) is associated to [**Win32\_Terminal**](win32-terminal.md) as the **Setting** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="4d5b9-637">Para conectarse al espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-637">To connect to the Root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="4d5b9-638">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-638">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="4d5b9-639">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de seis.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-639">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="4d5b9-640">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-640">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="4d5b9-641">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4d5b9-641">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4d5b9-642">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-642">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4d5b9-643">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="4d5b9-643">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4d5b9-644">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4d5b9-644">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d5b9-645">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d5b9-645">Requirements</span></span>



| <span data-ttu-id="4d5b9-646">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d5b9-646">Requirement</span></span> | <span data-ttu-id="4d5b9-647">Value</span><span class="sxs-lookup"><span data-stu-id="4d5b9-647">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d5b9-648">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d5b9-648">Minimum supported client</span></span><br/> | <span data-ttu-id="4d5b9-649">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4d5b9-649">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4d5b9-650">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d5b9-650">Minimum supported server</span></span><br/> | <span data-ttu-id="4d5b9-651">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d5b9-651">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d5b9-652">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d5b9-652">Namespace</span></span><br/>                | <span data-ttu-id="4d5b9-653">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4d5b9-653">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4d5b9-654">MOF</span><span class="sxs-lookup"><span data-stu-id="4d5b9-654">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d5b9-655"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d5b9-655"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d5b9-656">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d5b9-656">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d5b9-657"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d5b9-657"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d5b9-658">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d5b9-658">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d5b9-659">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-659">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="4d5b9-660">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-660">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="4d5b9-661">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-661">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="4d5b9-662">**Win32 \_ TerminalServiceToSetting**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-662">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="4d5b9-663">**Win32 \_ TerminalTerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-663">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dt>

[<span data-ttu-id="4d5b9-664">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="4d5b9-664">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

