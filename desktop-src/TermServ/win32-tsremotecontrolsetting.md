---
title: Win32_TSRemoteControlSetting (clase)
description: Define la configuración de control remoto para la \_ clase de terminal Win32.
ms.assetid: 2e23915e-ee1c-4e53-8d0d-4d3fc2fefce6
ms.tgt_platform: multiple
keywords:
- Win32_TSRemoteControlSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSRemoteControlSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting
- Win32_TSRemoteControlSetting.Caption
- Win32_TSRemoteControlSetting.Description
- Win32_TSRemoteControlSetting.InstallDate
- Win32_TSRemoteControlSetting.Name
- Win32_TSRemoteControlSetting.Status
- Win32_TSRemoteControlSetting.TerminalName
- Win32_TSRemoteControlSetting.LevelOfControl
- Win32_TSRemoteControlSetting.PolicySourceLevelOfControl
- Win32_TSRemoteControlSetting.RemoteControlPolicy
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e327744ad864e14e1f2580b3b71116e448f36e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490966"
---
# <a name="win32_tsremotecontrolsetting-class"></a><span data-ttu-id="2033c-105">\_Clase Win32 TSRemoteControlSetting</span><span class="sxs-lookup"><span data-stu-id="2033c-105">Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="2033c-106">La clase WMI **\_ TSRemoteControlSetting de Win32** define los valores de configuración de control remoto para la clase de [**\_ terminal Win32**](win32-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="2033c-106">The **Win32\_TSRemoteControlSetting** WMI class defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

<span data-ttu-id="2033c-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="2033c-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="2033c-108">Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="2033c-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="2033c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2033c-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSREMOTECONTROLSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSRemoteControlSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   LevelOfControl;
  uint32   PolicySourceLevelOfControl;
  uint32   RemoteControlPolicy;
};
```

## <a name="members"></a><span data-ttu-id="2033c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2033c-110">Members</span></span>

<span data-ttu-id="2033c-111">La **clase \_ TSRemoteControlSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2033c-111">The **Win32\_TSRemoteControlSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="2033c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2033c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2033c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2033c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2033c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="2033c-114">Methods</span></span>

<span data-ttu-id="2033c-115">La clase **Win32 \_ TSRemoteControlSetting** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2033c-115">The **Win32\_TSRemoteControlSetting** class has these methods.</span></span>



| <span data-ttu-id="2033c-116">Método</span><span class="sxs-lookup"><span data-stu-id="2033c-116">Method</span></span>                                                              | <span data-ttu-id="2033c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2033c-117">Description</span></span>                                                    |
|:--------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="2033c-118">**RemoteControl**</span><span class="sxs-lookup"><span data-stu-id="2033c-118">**RemoteControl**</span></span>](win32-tsremotecontrolsetting-remotecontrol.md) | <span data-ttu-id="2033c-119">Establece la propiedad **LevelOfControl** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="2033c-119">Sets the **LevelOfControl** property of this class.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2033c-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2033c-120">Properties</span></span>

<span data-ttu-id="2033c-121">La **clase \_ TSRemoteControlSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2033c-121">The **Win32\_TSRemoteControlSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2033c-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2033c-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2033c-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2033c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2033c-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2033c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2033c-125">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2033c-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2033c-126">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="2033c-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="2033c-127">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2033c-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2033c-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2033c-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2033c-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2033c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2033c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2033c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2033c-131">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2033c-131">Description of the object.</span></span>

<span data-ttu-id="2033c-132">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2033c-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2033c-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2033c-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2033c-134">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2033c-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2033c-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2033c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2033c-136">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="2033c-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="2033c-137">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="2033c-137">The date the object was installed.</span></span> <span data-ttu-id="2033c-138">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="2033c-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2033c-139">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2033c-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2033c-140">**LevelOfControl**</span><span class="sxs-lookup"><span data-stu-id="2033c-140">**LevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2033c-141">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2033c-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2033c-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2033c-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2033c-143">Nivel de control de la sesión, que especifica si la sesión solo la verá el usuario remoto o si se puede ver y controlar mediante un teclado y un mouse.</span><span class="sxs-lookup"><span data-stu-id="2033c-143">Level of control for the session, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="2033c-144">Para obtener más información, vea la sección Comentarios del método [**Remotecontrol**](win32-tsremotecontrolsetting-remotecontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="2033c-144">For more information, see the Remarks section of the [**RemoteControl**](win32-tsremotecontrolsetting-remotecontrol.md) method.</span></span> <span data-ttu-id="2033c-145">Se admiten los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2033c-145">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="2033c-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deshabilitar** (0)</span><span class="sxs-lookup"><span data-stu-id="2033c-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2033c-147">El control remoto está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="2033c-147">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="2033c-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span><span class="sxs-lookup"><span data-stu-id="2033c-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2033c-149">El usuario del control remoto tiene control total sobre la sesión del usuario, con el permiso del usuario.</span><span class="sxs-lookup"><span data-stu-id="2033c-149">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="2033c-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span><span class="sxs-lookup"><span data-stu-id="2033c-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2033c-151">El usuario del control remoto tiene control total sobre la sesión del usuario; el permiso del usuario no es necesario.</span><span class="sxs-lookup"><span data-stu-id="2033c-151">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="2033c-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span><span class="sxs-lookup"><span data-stu-id="2033c-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2033c-153">El usuario del control remoto puede ver la sesión de forma remota, con el permiso del usuario; el usuario remoto no puede controlar activamente la sesión.</span><span class="sxs-lookup"><span data-stu-id="2033c-153">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="2033c-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span><span class="sxs-lookup"><span data-stu-id="2033c-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2033c-155">El usuario del control remoto puede ver la sesión de forma remota, pero no controlar activamente la sesión. el permiso del usuario no es necesario.</span><span class="sxs-lookup"><span data-stu-id="2033c-155">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2033c-156">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2033c-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2033c-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2033c-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2033c-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2033c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2033c-159">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="2033c-159">The name of the object.</span></span>

<span data-ttu-id="2033c-160">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2033c-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2033c-161">**PolicySourceLevelOfControl**</span><span class="sxs-lookup"><span data-stu-id="2033c-161">**PolicySourceLevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2033c-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2033c-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2033c-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2033c-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2033c-164">Indica si la propiedad **LevelOfControl** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2033c-164">Indicates whether the **LevelOfControl** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="2033c-165">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="2033c-165">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="2033c-166">Servidor</span><span class="sxs-lookup"><span data-stu-id="2033c-166">Server</span></span>

</dd> <dt>

<span data-ttu-id="2033c-167">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="2033c-167">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="2033c-168">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="2033c-168">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="2033c-169">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="2033c-169">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="2033c-170">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2033c-170">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2033c-171">**RemoteControlPolicy**</span><span class="sxs-lookup"><span data-stu-id="2033c-171">**RemoteControlPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2033c-172">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2033c-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2033c-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2033c-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2033c-174">La Directiva que el servidor usa para recuperar la configuración de control remoto.</span><span class="sxs-lookup"><span data-stu-id="2033c-174">The policy the server uses to retrieve the remote control settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="2033c-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuario** (0)</span><span class="sxs-lookup"><span data-stu-id="2033c-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2033c-176">La configuración de control remoto del usuario está en vigor.</span><span class="sxs-lookup"><span data-stu-id="2033c-176">The user's remote control settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="2033c-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Invalidación de servidor** (1)</span><span class="sxs-lookup"><span data-stu-id="2033c-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2033c-178">El servidor invalida la configuración de control remoto del usuario.</span><span class="sxs-lookup"><span data-stu-id="2033c-178">The user's remote control settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2033c-179">**Estado**</span><span class="sxs-lookup"><span data-stu-id="2033c-179">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2033c-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2033c-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2033c-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2033c-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2033c-182">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="2033c-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="2033c-183">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2033c-183">Current status of the object.</span></span> <span data-ttu-id="2033c-184">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="2033c-184">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2033c-185">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="2033c-185">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2033c-186">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="2033c-186">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2033c-187">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="2033c-187">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2033c-188">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="2033c-188">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2033c-189">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2033c-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="2033c-190">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="2033c-190">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2033c-191">("Error")</span><span class="sxs-lookup"><span data-stu-id="2033c-191">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2033c-192">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="2033c-192">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2033c-193">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="2033c-193">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2033c-194">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="2033c-194">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2033c-195">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="2033c-195">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2033c-196">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="2033c-196">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2033c-197">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="2033c-197">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2033c-198">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="2033c-198">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2033c-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2033c-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2033c-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2033c-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2033c-201">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="2033c-201">The name of the terminal.</span></span>

<span data-ttu-id="2033c-202">Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="2033c-202">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2033c-203">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2033c-203">Remarks</span></span>

<span data-ttu-id="2033c-204">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="2033c-204">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="2033c-205">En el caso de las llamadas de C/C++, esto sería un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="2033c-205">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="2033c-206">En el caso de las llamadas de Visual Basic y scripting, esto sería un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="2033c-206">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="2033c-207">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="2033c-207">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="2033c-208">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2033c-208">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2033c-209">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2033c-209">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2033c-210">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="2033c-210">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2033c-211">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2033c-211">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2033c-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2033c-212">Requirements</span></span>



| <span data-ttu-id="2033c-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="2033c-213">Requirement</span></span> | <span data-ttu-id="2033c-214">Value</span><span class="sxs-lookup"><span data-stu-id="2033c-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2033c-215">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2033c-215">Minimum supported client</span></span><br/> | <span data-ttu-id="2033c-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2033c-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2033c-217">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2033c-217">Minimum supported server</span></span><br/> | <span data-ttu-id="2033c-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2033c-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2033c-219">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2033c-219">Namespace</span></span><br/>                | <span data-ttu-id="2033c-220">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2033c-220">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2033c-221">MOF</span><span class="sxs-lookup"><span data-stu-id="2033c-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2033c-222"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2033c-222"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2033c-223">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2033c-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2033c-224"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2033c-224"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2033c-225">Vea también</span><span class="sxs-lookup"><span data-stu-id="2033c-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2033c-226">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="2033c-226">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="2033c-227">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="2033c-227">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

