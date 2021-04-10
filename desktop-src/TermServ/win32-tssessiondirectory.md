---
title: Win32_TSSessionDirectory (clase)
description: Define los valores de configuración del agente de Conexión a Escritorio remoto (agente de conexión a escritorio remoto) para la \_ clase TSSessionDirectorySetting de Win32.
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectory clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSSessionDirectory de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996244"
---
# <a name="win32_tssessiondirectory-class"></a><span data-ttu-id="d15da-105">\_Clase Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="d15da-105">Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="d15da-106">Define los valores de configuración del agente de Conexión a Escritorio remoto (agente de conexión a escritorio remoto) para la clase [**\_ TSSessionDirectorySetting de Win32**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="d15da-106">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="d15da-107">En Windows Server 2008 R2, el nombre de Terminal Services agente de sesión (agente de sesiones de TS) se cambió al agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="d15da-108">Estas propiedades se aplican a todos los sistemas operativos compatibles a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="d15da-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

<span data-ttu-id="d15da-109">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="d15da-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="d15da-110">Para obtener información de referencia acerca de los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="d15da-110">For reference information about methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="d15da-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d15da-111">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a><span data-ttu-id="d15da-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="d15da-112">Members</span></span>

<span data-ttu-id="d15da-113">La **clase \_ TSSessionDirectory de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d15da-113">The **Win32\_TSSessionDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="d15da-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d15da-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d15da-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d15da-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d15da-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="d15da-116">Methods</span></span>

<span data-ttu-id="d15da-117">La clase **Win32 \_ TSSessionDirectory** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d15da-117">The **Win32\_TSSessionDirectory** class has these methods.</span></span>



| <span data-ttu-id="d15da-118">Método</span><span class="sxs-lookup"><span data-stu-id="d15da-118">Method</span></span>                                                                                                  | <span data-ttu-id="d15da-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d15da-119">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d15da-120">**CreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="d15da-120">**CreateUserDiskTemplate**</span></span>](createuserdisktemplate-win32-tssessiondirectory.md)                       | <span data-ttu-id="d15da-121">Crea una plantilla de disco de usuario.</span><span class="sxs-lookup"><span data-stu-id="d15da-121">Creates a user disk template.</span></span><br/>                                                                     |
| [<span data-ttu-id="d15da-122">**DisableUserVhd**</span><span class="sxs-lookup"><span data-stu-id="d15da-122">**DisableUserVhd**</span></span>](disableuservhd-win32-tssessiondirectory.md)                                       | <span data-ttu-id="d15da-123">Deshabilita un VHD de Perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="d15da-123">Disables a user profile VHD.</span></span><br/>                                                                      |
| [<span data-ttu-id="d15da-124">**EnableUserVhd**</span><span class="sxs-lookup"><span data-stu-id="d15da-124">**EnableUserVhd**</span></span>](enableuservhd-win32-tssessiondirectory.md)                                         | <span data-ttu-id="d15da-125">Habilita un VHD de Perfil de usuario en un servidor RDSH.</span><span class="sxs-lookup"><span data-stu-id="d15da-125">Enables a user profile VHD on an RDSH server.</span></span><br/>                                                     |
| [<span data-ttu-id="d15da-126">**GetCurrentRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="d15da-126">**GetCurrentRedirectableAddresses**</span></span>](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="d15da-127">Obtiene la lista configurada actualmente de direcciones válidas de DNS y el tipo de redirección.</span><span class="sxs-lookup"><span data-stu-id="d15da-127">Obtains the currently configured list of DNS eligible addresses, and the redirection type.</span></span><br/>        |
| [<span data-ttu-id="d15da-128">**GetRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="d15da-128">**GetRedirectableAddresses**</span></span>](getredirectableaddresses-win32-tssessiondirectory.md)                   | <span data-ttu-id="d15da-129">Obtiene la lista completa de direcciones DNS válidas.</span><span class="sxs-lookup"><span data-stu-id="d15da-129">Obtains the entire list of DNS eligible addresses.</span></span><br/>                                                |
| [<span data-ttu-id="d15da-130">**PingSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="d15da-130">**PingSessionDirectory**</span></span>](pingsessiondirectory-win32-tssessiondirectory.md)                           | <span data-ttu-id="d15da-131">Comprueba si el servidor de agente de conexión a escritorio remoto está disponible.</span><span class="sxs-lookup"><span data-stu-id="d15da-131">Checks whether the RD Connection Broker server is available.</span></span><br/>                                      |
| [<span data-ttu-id="d15da-132">**SetCurrentRedirectableAddresses**</span><span class="sxs-lookup"><span data-stu-id="d15da-132">**SetCurrentRedirectableAddresses**</span></span>](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="d15da-133">Establece la lista configurada de direcciones válidas de DNS y el tipo de redirección.</span><span class="sxs-lookup"><span data-stu-id="d15da-133">Sets the configured list of DNS eligible addresses, and the redirection type.</span></span><br/>                     |
| [<span data-ttu-id="d15da-134">**SetLoadBalancingState**</span><span class="sxs-lookup"><span data-stu-id="d15da-134">**SetLoadBalancingState**</span></span>](setloadbalancingstate-win32-tssessiondirectory.md)                         | <span data-ttu-id="d15da-135">Establece el valor para indicar si el servidor participará en el equilibrio de carga del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-135">Sets the value to indicate if the server will participate in RD Connection Broker load balancing.</span></span><br/> |
| [<span data-ttu-id="d15da-136">**SetServerWeight**</span><span class="sxs-lookup"><span data-stu-id="d15da-136">**SetServerWeight**</span></span>](setserverweight-win32-tssessiondirectory.md)                                     | <span data-ttu-id="d15da-137">Establece el valor de peso del servidor para el equilibrio de carga del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-137">Sets the server weight value for RD Connection Broker load balancing.</span></span><br/>                             |
| [<span data-ttu-id="d15da-138">**SetSessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="d15da-138">**SetSessionDirectoryActive**</span></span>](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | <span data-ttu-id="d15da-139">Deshabilita y habilita el agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-139">Disables and enables the RD Connection Broker.</span></span><br/>                                                    |
| [<span data-ttu-id="d15da-140">**SetSessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="d15da-140">**SetSessionDirectoryExposeServerIP**</span></span>](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | <span data-ttu-id="d15da-141">Establece la propiedad **SessionDirectoryExposeServerIP** .</span><span class="sxs-lookup"><span data-stu-id="d15da-141">Sets the **SessionDirectoryExposeServerIP** property.</span></span><br/>                                             |
| [<span data-ttu-id="d15da-142">**SetSessionDirectoryProperty**</span><span class="sxs-lookup"><span data-stu-id="d15da-142">**SetSessionDirectoryProperty**</span></span>](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | <span data-ttu-id="d15da-143">Establece la propiedad **SessionDirectoryLocation** o la propiedad **SessionDirectoryClusterName** .</span><span class="sxs-lookup"><span data-stu-id="d15da-143">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property.</span></span><br/>   |
| [<span data-ttu-id="d15da-144">**SetTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="d15da-144">**SetTSRedirectorMode**</span></span>](settsredirectormode-win32-tssessiondirectory.md)                             | <span data-ttu-id="d15da-145">Este método no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d15da-145">This method is not available.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="d15da-146">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d15da-146">Properties</span></span>

<span data-ttu-id="d15da-147">La **clase \_ TSSessionDirectory de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d15da-147">The **Win32\_TSSessionDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d15da-148">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d15da-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d15da-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d15da-151">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d15da-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d15da-152">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="d15da-152">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d15da-153">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d15da-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d15da-154">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d15da-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d15da-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-157">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d15da-157">Description of the object.</span></span>

<span data-ttu-id="d15da-158">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d15da-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d15da-159">**GetLoadBalancingState**</span><span class="sxs-lookup"><span data-stu-id="d15da-159">**GetLoadBalancingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-160">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15da-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-162">Indica si el servidor está configurado para participar en el equilibrio de carga del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-162">Indicates if the server is configured to participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="d15da-163">0</span><span class="sxs-lookup"><span data-stu-id="d15da-163">0</span></span>
</dt> <dd>

<span data-ttu-id="d15da-164">El servidor no está configurado para participar en el equilibrio de carga del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-164">The server is not configured to participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-165">1</span><span class="sxs-lookup"><span data-stu-id="d15da-165">1</span></span>
</dt> <dd>

<span data-ttu-id="d15da-166">El servidor está configurado para participar en el equilibrio de carga del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-166">The server is configured to participate in RD Connection Broker load balancing.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d15da-167">**GetServerWeight**</span><span class="sxs-lookup"><span data-stu-id="d15da-167">**GetServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-168">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15da-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-170">Recupera el valor de peso del servidor que se usa en el equilibrio de carga del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-170">Retrieves the server weight value that is used in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-171">**GetTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="d15da-171">**GetTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-172">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15da-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-174">Indica si el servidor está configurado para actuar como redirector de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-174">Indicates if the server is configured to act as a Remote Desktop Services redirector.</span></span>

<dt>

<span data-ttu-id="d15da-175">0</span><span class="sxs-lookup"><span data-stu-id="d15da-175">0</span></span>
</dt> <dd>

<span data-ttu-id="d15da-176">El servidor está configurado para actuar como redirector de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-176">The server is configured to act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-177">1</span><span class="sxs-lookup"><span data-stu-id="d15da-177">1</span></span>
</dt> <dd>

<span data-ttu-id="d15da-178">El servidor no está configurado para actuar como redirector de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-178">The server is not configured to act as a Remote Desktop Services redirector.</span></span>

</dd> </dl>

<span data-ttu-id="d15da-179">**Windows Server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d15da-179">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-180">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d15da-180">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-181">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d15da-181">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d15da-183">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="d15da-183">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d15da-184">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="d15da-184">The date the object was installed.</span></span> <span data-ttu-id="d15da-185">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="d15da-185">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d15da-186">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d15da-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d15da-187">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d15da-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d15da-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-190">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="d15da-190">The name of the object.</span></span>

<span data-ttu-id="d15da-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d15da-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d15da-192">**PolicySourceLoadBalancing**</span><span class="sxs-lookup"><span data-stu-id="d15da-192">**PolicySourceLoadBalancing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-193">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15da-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-195">Indica si la propiedad **GetLoadBalancingState** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d15da-195">Indicates if the **GetLoadBalancingState** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="d15da-196">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="d15da-196">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-197">Servidor</span><span class="sxs-lookup"><span data-stu-id="d15da-197">Server</span></span>

</dd> <dt>

<span data-ttu-id="d15da-198">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d15da-198">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-199">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="d15da-199">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d15da-200">**PolicySourceSessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="d15da-200">**PolicySourceSessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-201">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15da-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-203">Indica si la propiedad **SessionDirectoryActive** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d15da-203">Indicates if the **SessionDirectoryActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="d15da-204">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="d15da-204">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-205">Servidor</span><span class="sxs-lookup"><span data-stu-id="d15da-205">Server</span></span>

</dd> <dt>

<span data-ttu-id="d15da-206">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d15da-206">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-207">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="d15da-207">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d15da-208">**PolicySourceSessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="d15da-208">**PolicySourceSessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-209">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15da-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-211">Indica si la propiedad **SessionDirectoryClusterName** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d15da-211">Indicates if the **SessionDirectoryClusterName** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="d15da-212">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="d15da-212">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-213">Servidor</span><span class="sxs-lookup"><span data-stu-id="d15da-213">Server</span></span>

</dd> <dt>

<span data-ttu-id="d15da-214">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d15da-214">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-215">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="d15da-215">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d15da-216">**PolicySourceSessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="d15da-216">**PolicySourceSessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-217">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15da-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-219">Indica si la propiedad **SessionDirectoryExposeServerIP** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d15da-219">Indicates if the **SessionDirectoryExposeServerIP** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="d15da-220">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="d15da-220">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-221">Servidor</span><span class="sxs-lookup"><span data-stu-id="d15da-221">Server</span></span>

</dd> <dt>

<span data-ttu-id="d15da-222">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d15da-222">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-223">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="d15da-223">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d15da-224">**PolicySourceSessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="d15da-224">**PolicySourceSessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-225">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15da-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-227">Indica si la propiedad **SessionDirectoryLocation** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d15da-227">Indicates if the **SessionDirectoryLocation** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="d15da-228">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="d15da-228">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-229">Servidor</span><span class="sxs-lookup"><span data-stu-id="d15da-229">Server</span></span>

</dd> <dt>

<span data-ttu-id="d15da-230">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d15da-230">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-231">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="d15da-231">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d15da-232">**PolicySourceTSRedirectorMode**</span><span class="sxs-lookup"><span data-stu-id="d15da-232">**PolicySourceTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-233">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15da-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-235">Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d15da-235">This property is not available.</span></span>

<span data-ttu-id="d15da-236">**Windows Server 2008 R2:** Indica si la propiedad **GetTSRedirectorMode** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d15da-236">**Windows Server 2008 R2:** Indicates if the **GetTSRedirectorMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="d15da-237">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="d15da-237">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-238">Servidor</span><span class="sxs-lookup"><span data-stu-id="d15da-238">Server</span></span>

</dd> <dt>

<span data-ttu-id="d15da-239">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d15da-239">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d15da-240">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="d15da-240">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d15da-241">**SessionDirectoryActive**</span><span class="sxs-lookup"><span data-stu-id="d15da-241">**SessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-242">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15da-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d15da-244">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d15da-244">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d15da-245">Especifica si Servicios de Escritorio remoto participa en el agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-245">Specifies if Remote Desktop Services participates in the RD Connection Broker.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="d15da-246"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="d15da-246"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d15da-247">Servicios de Escritorio remoto la participación en el agente de conexión a escritorio remoto está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="d15da-247">Remote Desktop Services participation in the RD Connection Broker is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="d15da-248"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="d15da-248"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d15da-249">Servicios de Escritorio remoto la participación en el agente de conexión a escritorio remoto está habilitada.</span><span class="sxs-lookup"><span data-stu-id="d15da-249">Remote Desktop Services participation in the RD Connection Broker is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d15da-250">**SessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="d15da-250">**SessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d15da-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-253">La dirección IP virtual del clúster al que pertenece el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-253">The virtual IP address of the cluster to which the RD Session Host server belongs.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-254">**SessionDirectoryExposeServerIP**</span><span class="sxs-lookup"><span data-stu-id="d15da-254">**SessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-255">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15da-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-257">Especifica si se permite la recuperación de la dirección IP del agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-257">Specifies if retrieval of the IP address of the RD Connection Broker is allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="d15da-258"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="d15da-258"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d15da-259">Se denegó la recuperación.</span><span class="sxs-lookup"><span data-stu-id="d15da-259">Retrieval is denied.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="d15da-260"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="d15da-260"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d15da-261">Se permite la recuperación.</span><span class="sxs-lookup"><span data-stu-id="d15da-261">Retrieval is allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d15da-262">**SessionDirectoryIPAddress**</span><span class="sxs-lookup"><span data-stu-id="d15da-262">**SessionDirectoryIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-263">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d15da-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-264">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d15da-264">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d15da-265">La dirección IP del adaptador de LAN que usa el directorio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d15da-265">The IP address of the LAN adapter used by the session directory.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-266">**SessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="d15da-266">**SessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-267">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d15da-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15da-269">El nombre DNS de red o la dirección IP del servidor en el que se está ejecutando el servicio agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d15da-269">The network DNS name or IP address of the server where the RD Connection Broker service is running.</span></span>

</dd> <dt>

<span data-ttu-id="d15da-270">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d15da-270">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15da-271">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d15da-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d15da-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d15da-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d15da-273">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="d15da-273">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d15da-274">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d15da-274">Current status of the object.</span></span> <span data-ttu-id="d15da-275">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="d15da-275">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d15da-276">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d15da-276">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d15da-277">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="d15da-277">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d15da-278">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d15da-278">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d15da-279">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="d15da-279">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d15da-280">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d15da-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d15da-281">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="d15da-281">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d15da-282">("Error")</span><span class="sxs-lookup"><span data-stu-id="d15da-282">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d15da-283">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="d15da-283">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d15da-284">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="d15da-284">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d15da-285">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="d15da-285">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d15da-286">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="d15da-286">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d15da-287">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="d15da-287">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d15da-288">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="d15da-288">("Service")</span></span>


<span data-ttu-id="d15da-289"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d15da-289"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d15da-290">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d15da-290">Remarks</span></span>

<span data-ttu-id="d15da-291">Para conectarse al \\ \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d15da-291">To connect to the \\\\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="d15da-292">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="d15da-292">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="d15da-293">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de seis.</span><span class="sxs-lookup"><span data-stu-id="d15da-293">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="d15da-294">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d15da-294">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="d15da-295">En Windows Server 2008, el nombre de la característica Terminal Services directorio de sesión se ha cambiado a Terminal Services agente de sesiones.</span><span class="sxs-lookup"><span data-stu-id="d15da-295">In Windows Server 2008, the name of the Terminal Services Session Directory feature was changed to Terminal Services Session Broker.</span></span>

<span data-ttu-id="d15da-296">En Windows Server 2008 R2, el nombre de la característica agente de sesión de Terminal Services se ha cambiado a Conexión a Escritorio remoto Broker.</span><span class="sxs-lookup"><span data-stu-id="d15da-296">In Windows Server 2008 R2, the name of the Terminal Services Session Broker feature was changed to Remote Desktop Connection Broker.</span></span>

<span data-ttu-id="d15da-297">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d15da-297">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d15da-298">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d15da-298">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d15da-299">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d15da-299">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d15da-300">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d15da-300">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d15da-301">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d15da-301">Requirements</span></span>



| <span data-ttu-id="d15da-302">Requisito</span><span class="sxs-lookup"><span data-stu-id="d15da-302">Requirement</span></span> | <span data-ttu-id="d15da-303">Value</span><span class="sxs-lookup"><span data-stu-id="d15da-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d15da-304">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d15da-304">Minimum supported client</span></span><br/> | <span data-ttu-id="d15da-305">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d15da-305">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d15da-306">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d15da-306">Minimum supported server</span></span><br/> | <span data-ttu-id="d15da-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d15da-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d15da-308">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d15da-308">Namespace</span></span><br/>                | <span data-ttu-id="d15da-309">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d15da-309">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d15da-310">MOF</span><span class="sxs-lookup"><span data-stu-id="d15da-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d15da-311"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d15da-311"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d15da-312">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d15da-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d15da-313"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d15da-313"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d15da-314">Vea también</span><span class="sxs-lookup"><span data-stu-id="d15da-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d15da-315">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="d15da-315">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="d15da-316">**Win32 \_ TSSessionDirectorySetting**</span><span class="sxs-lookup"><span data-stu-id="d15da-316">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

