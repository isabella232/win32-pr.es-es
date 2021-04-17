---
title: Win32_TSSessionSetting (clase)
description: Define los valores de configuración para la clase de terminal Win32, como los \_ límites de tiempo, y las acciones de desconexión y reconexión.
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSSessionSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e780cdedee0fe447499bed5013dadc2ba9b448b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535362"
---
# <a name="win32_tssessionsetting-class"></a><span data-ttu-id="613b8-105">\_Clase Win32 TSSessionSetting</span><span class="sxs-lookup"><span data-stu-id="613b8-105">Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="613b8-106">La clase WMI **\_ TSSessionSetting de Win32** define los valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) , como los límites de tiempo, y las acciones de desconexión y reconexión.</span><span class="sxs-lookup"><span data-stu-id="613b8-106">The **Win32\_TSSessionSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

<span data-ttu-id="613b8-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="613b8-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="613b8-108">Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="613b8-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="613b8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="613b8-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a><span data-ttu-id="613b8-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="613b8-110">Members</span></span>

<span data-ttu-id="613b8-111">La **clase \_ TSSessionSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="613b8-111">The **Win32\_TSSessionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="613b8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="613b8-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="613b8-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="613b8-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="613b8-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="613b8-114">Methods</span></span>

<span data-ttu-id="613b8-115">La clase **Win32 \_ TSSessionSetting** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="613b8-115">The **Win32\_TSSessionSetting** class has these methods.</span></span>



| <span data-ttu-id="613b8-116">Método</span><span class="sxs-lookup"><span data-stu-id="613b8-116">Method</span></span>                                                              | <span data-ttu-id="613b8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="613b8-117">Description</span></span>                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="613b8-118">**BrokenConnection**</span><span class="sxs-lookup"><span data-stu-id="613b8-118">**BrokenConnection**</span></span>](win32-tssessionsetting-brokenconnection.md) | <span data-ttu-id="613b8-119">Establece las propiedades de conexión interrumpidas incluidas en esta clase.</span><span class="sxs-lookup"><span data-stu-id="613b8-119">Sets the broken connection properties included in this class.</span></span><br/> |
| [<span data-ttu-id="613b8-120">**TimeLimit**</span><span class="sxs-lookup"><span data-stu-id="613b8-120">**TimeLimit**</span></span>](win32-tssessionsetting-timelimit.md)               | <span data-ttu-id="613b8-121">Establece las propiedades de límite de tiempo incluidas en esta clase.</span><span class="sxs-lookup"><span data-stu-id="613b8-121">Sets the time-limit properties included in this class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="613b8-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="613b8-122">Properties</span></span>

<span data-ttu-id="613b8-123">La **clase \_ TSSessionSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="613b8-123">The **Win32\_TSSessionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="613b8-124">**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="613b8-124">**ActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-125">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-127">Cantidad máxima de tiempo, en milisegundos, que se asigna a una sesión activa.</span><span class="sxs-lookup"><span data-stu-id="613b8-127">The maximum amount of time, in milliseconds, allocated to an active session.</span></span> <span data-ttu-id="613b8-128">Un valor de 0 especifica una cantidad de tiempo infinita.</span><span class="sxs-lookup"><span data-stu-id="613b8-128">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="613b8-129">**BrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="613b8-129">**BrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-132">La acción que realiza el servidor en la sesión cuando se ha interrumpido una conexión debido a una pérdida de la red o a que se han superado los límites de tiempo.</span><span class="sxs-lookup"><span data-stu-id="613b8-132">The action the server takes on the session when a connection has been broken due to network loss or exceeded time-limits.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="613b8-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Desconectar** (0)</span><span class="sxs-lookup"><span data-stu-id="613b8-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="613b8-134">El usuario se desconecta de la sesión.</span><span class="sxs-lookup"><span data-stu-id="613b8-134">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="613b8-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Finalizar** (1)</span><span class="sxs-lookup"><span data-stu-id="613b8-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="613b8-136">La sesión se elimina permanentemente del servidor.</span><span class="sxs-lookup"><span data-stu-id="613b8-136">The session is permanently deleted from the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="613b8-137">**BrokenConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="613b8-137">**BrokenConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-138">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613b8-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="613b8-140">La Directiva que el servidor usa para determinar cuándo interrumpir una conexión debido a la pérdida de la red o a superar los límites de tiempo.</span><span class="sxs-lookup"><span data-stu-id="613b8-140">The policy the server uses to determine when to break a connection because of network loss or exceeded time-limits.</span></span>

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="613b8-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Invalidación de servidor** (1)</span><span class="sxs-lookup"><span data-stu-id="613b8-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="613b8-142">El servidor invalida la configuración de la Directiva de desconexión del usuario.</span><span class="sxs-lookup"><span data-stu-id="613b8-142">The user's disconnection policy settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="613b8-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuario** (0)</span><span class="sxs-lookup"><span data-stu-id="613b8-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="613b8-144">La configuración de la Directiva de desconexión del usuario está en vigor.</span><span class="sxs-lookup"><span data-stu-id="613b8-144">The user's disconnection policy settings are in effect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="613b8-145">**Caption**</span><span class="sxs-lookup"><span data-stu-id="613b8-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613b8-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613b8-148">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="613b8-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="613b8-149">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="613b8-149">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="613b8-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="613b8-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="613b8-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="613b8-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613b8-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-154">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="613b8-154">Description of the object.</span></span>

<span data-ttu-id="613b8-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="613b8-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="613b8-156">**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="613b8-156">**DisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-159">El intervalo de tiempo, en milisegundos, después del cual finaliza una sesión desconectada.</span><span class="sxs-lookup"><span data-stu-id="613b8-159">The time interval, in milliseconds, after which a disconnected session is terminated.</span></span> <span data-ttu-id="613b8-160">Un valor de 0 especifica una cantidad de tiempo infinita.</span><span class="sxs-lookup"><span data-stu-id="613b8-160">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="613b8-161">**EnableTimeoutWarning**</span><span class="sxs-lookup"><span data-stu-id="613b8-161">**EnableTimeoutWarning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613b8-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="613b8-164">Habilita la advertencia de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="613b8-164">Enables the timeout warning.</span></span>

<span data-ttu-id="613b8-165">**Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:** Esta propiedad no está disponible.</span><span class="sxs-lookup"><span data-stu-id="613b8-165">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="613b8-166">**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="613b8-166">**IdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-167">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-169">El intervalo de tiempo, en milisegundos, después del cual finaliza una sesión inactiva.</span><span class="sxs-lookup"><span data-stu-id="613b8-169">The time interval, in milliseconds, after which an idle session is terminated.</span></span> <span data-ttu-id="613b8-170">Un valor de 0 especifica una cantidad de tiempo infinita.</span><span class="sxs-lookup"><span data-stu-id="613b8-170">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="613b8-171">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="613b8-171">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-172">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="613b8-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613b8-174">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="613b8-174">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="613b8-175">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="613b8-175">The date the object was installed.</span></span> <span data-ttu-id="613b8-176">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="613b8-176">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="613b8-177">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="613b8-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="613b8-178">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="613b8-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613b8-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-181">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="613b8-181">The name of the object.</span></span>

<span data-ttu-id="613b8-182">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="613b8-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="613b8-183">**PolicySourceActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="613b8-183">**PolicySourceActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-184">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-186">Indica si la propiedad **ActiveSessionLimit** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="613b8-186">Indicates whether the **ActiveSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="613b8-187">0</span><span class="sxs-lookup"><span data-stu-id="613b8-187">0</span></span>
</dt> <dd>

<span data-ttu-id="613b8-188">Servidor</span><span class="sxs-lookup"><span data-stu-id="613b8-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="613b8-189">1</span><span class="sxs-lookup"><span data-stu-id="613b8-189">1</span></span>
</dt> <dd>

<span data-ttu-id="613b8-190">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="613b8-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="613b8-191">2</span><span class="sxs-lookup"><span data-stu-id="613b8-191">2</span></span>
</dt> <dd>

<span data-ttu-id="613b8-192">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="613b8-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="613b8-193">**PolicySourceBrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="613b8-193">**PolicySourceBrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-194">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-196">Indica si la propiedad **BrokenConnectionAction** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="613b8-196">Indicates whether the **BrokenConnectionAction** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="613b8-197">0</span><span class="sxs-lookup"><span data-stu-id="613b8-197">0</span></span>
</dt> <dd>

<span data-ttu-id="613b8-198">Servidor</span><span class="sxs-lookup"><span data-stu-id="613b8-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="613b8-199">1</span><span class="sxs-lookup"><span data-stu-id="613b8-199">1</span></span>
</dt> <dd>

<span data-ttu-id="613b8-200">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="613b8-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="613b8-201">2</span><span class="sxs-lookup"><span data-stu-id="613b8-201">2</span></span>
</dt> <dd>

<span data-ttu-id="613b8-202">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="613b8-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="613b8-203">**PolicySourceDisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="613b8-203">**PolicySourceDisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-204">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-206">Indica si la propiedad **DisconnectedSessionLimit** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="613b8-206">Indicates whether the **DisconnectedSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="613b8-207">0</span><span class="sxs-lookup"><span data-stu-id="613b8-207">0</span></span>
</dt> <dd>

<span data-ttu-id="613b8-208">Servidor</span><span class="sxs-lookup"><span data-stu-id="613b8-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="613b8-209">1</span><span class="sxs-lookup"><span data-stu-id="613b8-209">1</span></span>
</dt> <dd>

<span data-ttu-id="613b8-210">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="613b8-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="613b8-211">2</span><span class="sxs-lookup"><span data-stu-id="613b8-211">2</span></span>
</dt> <dd>

<span data-ttu-id="613b8-212">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="613b8-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="613b8-213">**PolicySourceIdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="613b8-213">**PolicySourceIdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-214">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-216">Indica si la propiedad **IdleSessionLimit** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="613b8-216">Indicates whether the **IdleSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="613b8-217">0</span><span class="sxs-lookup"><span data-stu-id="613b8-217">0</span></span>
</dt> <dd>

<span data-ttu-id="613b8-218">Servidor</span><span class="sxs-lookup"><span data-stu-id="613b8-218">Server</span></span>

</dd> <dt>

<span data-ttu-id="613b8-219">1</span><span class="sxs-lookup"><span data-stu-id="613b8-219">1</span></span>
</dt> <dd>

<span data-ttu-id="613b8-220">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="613b8-220">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="613b8-221">2</span><span class="sxs-lookup"><span data-stu-id="613b8-221">2</span></span>
</dt> <dd>

<span data-ttu-id="613b8-222">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="613b8-222">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="613b8-223">**PolicySourceReconnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="613b8-223">**PolicySourceReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-224">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-226">Indica si la propiedad **ReconnectPolicy** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="613b8-226">Indicates whether the **ReconnectPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="613b8-227">0</span><span class="sxs-lookup"><span data-stu-id="613b8-227">0</span></span>
</dt> <dd>

<span data-ttu-id="613b8-228">Servidor</span><span class="sxs-lookup"><span data-stu-id="613b8-228">Server</span></span>

</dd> <dt>

<span data-ttu-id="613b8-229">1</span><span class="sxs-lookup"><span data-stu-id="613b8-229">1</span></span>
</dt> <dd>

<span data-ttu-id="613b8-230">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="613b8-230">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="613b8-231">2</span><span class="sxs-lookup"><span data-stu-id="613b8-231">2</span></span>
</dt> <dd>

<span data-ttu-id="613b8-232">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="613b8-232">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="613b8-233">**ReconnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="613b8-233">**ReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-234">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-235">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613b8-235">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="613b8-236">Especifica si un usuario debe utilizar el cliente anterior para volver a conectarse a una sesión desconectada.</span><span class="sxs-lookup"><span data-stu-id="613b8-236">Specifies whether a user must use the previous client to reconnect to a disconnected session.</span></span>

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span data-ttu-id="613b8-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Cualquier cliente** (0)</span><span class="sxs-lookup"><span data-stu-id="613b8-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Any Client** (0)</span></span>


</dt> <dd>

<span data-ttu-id="613b8-238">Cualquier cliente se usará para volver a conectarse.</span><span class="sxs-lookup"><span data-stu-id="613b8-238">Any client will be used to reconnect.</span></span>

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span data-ttu-id="613b8-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Cliente anterior** (1)</span><span class="sxs-lookup"><span data-stu-id="613b8-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Previous Client** (1)</span></span>


</dt> <dd>

<span data-ttu-id="613b8-240">El cliente anterior usado en una conexión se usará para volver a conectarse.</span><span class="sxs-lookup"><span data-stu-id="613b8-240">The previous client used in a connection will be used to reconnect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="613b8-241">**Estado**</span><span class="sxs-lookup"><span data-stu-id="613b8-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613b8-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613b8-244">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="613b8-244">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="613b8-245">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="613b8-245">Current status of the object.</span></span> <span data-ttu-id="613b8-246">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="613b8-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="613b8-247">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="613b8-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="613b8-248">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="613b8-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="613b8-249">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="613b8-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="613b8-250">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="613b8-250">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="613b8-251">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="613b8-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="613b8-252">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="613b8-252">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="613b8-253">("Error")</span><span class="sxs-lookup"><span data-stu-id="613b8-253">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="613b8-254">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="613b8-254">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="613b8-255">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="613b8-255">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="613b8-256">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="613b8-256">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="613b8-257">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="613b8-257">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="613b8-258">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="613b8-258">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="613b8-259">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="613b8-259">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="613b8-260">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="613b8-260">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613b8-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613b8-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613b8-263">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="613b8-263">The name of the terminal.</span></span>

<span data-ttu-id="613b8-264">Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="613b8-264">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="613b8-265">**TimeLimitPolicy**</span><span class="sxs-lookup"><span data-stu-id="613b8-265">**TimeLimitPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613b8-266">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613b8-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613b8-267">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613b8-267">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="613b8-268">La Directiva que el servidor usa para determinar los límites de tiempo para las sesiones de usuario.</span><span class="sxs-lookup"><span data-stu-id="613b8-268">The policy the server uses to determine time-limits for user sessions.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="613b8-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuario** (0)</span><span class="sxs-lookup"><span data-stu-id="613b8-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="613b8-270">La configuración de la Directiva de límites de tiempo del usuario está en vigor.</span><span class="sxs-lookup"><span data-stu-id="613b8-270">The user's time-limits policy settings are in effect.</span></span>

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span data-ttu-id="613b8-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Invalidación de servidor** (1)</span><span class="sxs-lookup"><span data-stu-id="613b8-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Server Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="613b8-272">El servidor invalida la configuración de la Directiva de límites de tiempo del usuario.</span><span class="sxs-lookup"><span data-stu-id="613b8-272">The user's time-limits policy settings are overridden by the server.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="613b8-273">Observaciones</span><span class="sxs-lookup"><span data-stu-id="613b8-273">Remarks</span></span>

<span data-ttu-id="613b8-274">Tenga en cuenta que Winstations asociado a la sesión de consola no puede tener acceso a los métodos y las propiedades de esta clase.</span><span class="sxs-lookup"><span data-stu-id="613b8-274">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="613b8-275">Si se realiza un intento de hacerlo especificando "Console" como el valor de la propiedad TerminalName, los métodos de este objeto devolverán **WBEM \_ E \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="613b8-275">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="613b8-276">También se devolverá este código de error si una estación de ventana intenta llamar a métodos de este objeto con el fin de agregar o modificar las propiedades de seguridad de las cuentas LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="613b8-276">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="613b8-277">Para conectarse al espacio de nombres "root \\ cimv2 \\ TerminalServices", el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="613b8-277">To connect to the "root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="613b8-278">En el caso de las llamadas de C/C++, esto sería un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="613b8-278">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="613b8-279">En el caso de las llamadas de Visual Basic y scripting, esto sería un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="613b8-279">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="613b8-280">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="613b8-280">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="613b8-281">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="613b8-281">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="613b8-282">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="613b8-282">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="613b8-283">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="613b8-283">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="613b8-284">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="613b8-284">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="613b8-285">Requisitos</span><span class="sxs-lookup"><span data-stu-id="613b8-285">Requirements</span></span>



| <span data-ttu-id="613b8-286">Requisito</span><span class="sxs-lookup"><span data-stu-id="613b8-286">Requirement</span></span> | <span data-ttu-id="613b8-287">Value</span><span class="sxs-lookup"><span data-stu-id="613b8-287">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="613b8-288">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="613b8-288">Minimum supported client</span></span><br/> | <span data-ttu-id="613b8-289">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="613b8-289">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="613b8-290">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="613b8-290">Minimum supported server</span></span><br/> | <span data-ttu-id="613b8-291">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="613b8-291">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="613b8-292">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="613b8-292">Namespace</span></span><br/>                | <span data-ttu-id="613b8-293">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="613b8-293">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="613b8-294">MOF</span><span class="sxs-lookup"><span data-stu-id="613b8-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="613b8-295"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="613b8-295"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="613b8-296">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="613b8-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="613b8-297"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="613b8-297"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="613b8-298">Vea también</span><span class="sxs-lookup"><span data-stu-id="613b8-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="613b8-299">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="613b8-299">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="613b8-300">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="613b8-300">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

