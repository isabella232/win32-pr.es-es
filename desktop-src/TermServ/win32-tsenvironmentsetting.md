---
title: Win32_TSEnvironmentSetting (clase)
description: Define los valores de configuración para la \_ clase de terminal Win32, incluida la Directiva de programa inicial.
ms.assetid: 2d310a1e-a1bd-4ccb-965e-8389aaa2e4c1
ms.tgt_platform: multiple
keywords:
- Win32_TSEnvironmentSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSEnvironmentSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting.Caption
- Win32_TSEnvironmentSetting.Description
- Win32_TSEnvironmentSetting.InstallDate
- Win32_TSEnvironmentSetting.Name
- Win32_TSEnvironmentSetting.Status
- Win32_TSEnvironmentSetting.TerminalName
- Win32_TSEnvironmentSetting.ClientWallPaper
- Win32_TSEnvironmentSetting.InitialProgramPath
- Win32_TSEnvironmentSetting.InitialProgramPolicy
- Win32_TSEnvironmentSetting.PolicySourceClientWallPaper
- Win32_TSEnvironmentSetting.PolicySourceInitialProgramPath
- Win32_TSEnvironmentSetting.PolicySourceStartIn
- Win32_TSEnvironmentSetting.Startin
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0689536385644ae3ef95d106e50ab198e5a57f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535200"
---
# <a name="win32_tsenvironmentsetting-class"></a><span data-ttu-id="52dc7-105">\_Clase Win32 TSEnvironmentSetting</span><span class="sxs-lookup"><span data-stu-id="52dc7-105">Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="52dc7-106">La clase WMI **\_ TSEnvironmentSetting de Win32** define los valores de configuración para la clase de [**\_ terminal Win32**](win32-terminal.md) , incluida la Directiva de programa inicial.</span><span class="sxs-lookup"><span data-stu-id="52dc7-106">The **Win32\_TSEnvironmentSetting** WMI class defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

<span data-ttu-id="52dc7-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="52dc7-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="52dc7-108">Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="52dc7-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="52dc7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52dc7-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSENVIRONMENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSEnvironmentSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientWallPaper;
  string   InitialProgramPath;
  uint32   InitialProgramPolicy;
  uint32   PolicySourceClientWallPaper;
  uint32   PolicySourceInitialProgramPath;
  uint32   PolicySourceStartIn;
  string   Startin;
};
```

## <a name="members"></a><span data-ttu-id="52dc7-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="52dc7-110">Members</span></span>

<span data-ttu-id="52dc7-111">La **clase \_ TSEnvironmentSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="52dc7-111">The **Win32\_TSEnvironmentSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="52dc7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="52dc7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="52dc7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="52dc7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="52dc7-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="52dc7-114">Methods</span></span>

<span data-ttu-id="52dc7-115">La clase **Win32 \_ TSEnvironmentSetting** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="52dc7-115">The **Win32\_TSEnvironmentSetting** class has these methods.</span></span>



| <span data-ttu-id="52dc7-116">Método</span><span class="sxs-lookup"><span data-stu-id="52dc7-116">Method</span></span>                                                                      | <span data-ttu-id="52dc7-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="52dc7-117">Description</span></span>                                                            |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="52dc7-118">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="52dc7-118">**InitialProgram**</span></span>](win32-tsenvironmentsetting-initialprogram.md)         | <span data-ttu-id="52dc7-119">Establece las propiedades del programa de inicio incluidas en esta clase.</span><span class="sxs-lookup"><span data-stu-id="52dc7-119">Sets the startup program properties included in this class.</span></span><br/> |
| [<span data-ttu-id="52dc7-120">**SetClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="52dc7-120">**SetClientWallPaper**</span></span>](win32-tsenvironmentsetting-setclientwallpaper.md) | <span data-ttu-id="52dc7-121">Establece la propiedad **ClientWallPaper** .</span><span class="sxs-lookup"><span data-stu-id="52dc7-121">Sets the **ClientWallPaper** property.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="52dc7-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="52dc7-122">Properties</span></span>

<span data-ttu-id="52dc7-123">La **clase \_ TSEnvironmentSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="52dc7-123">The **Win32\_TSEnvironmentSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52dc7-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="52dc7-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="52dc7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-127">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="52dc7-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-128">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="52dc7-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="52dc7-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52dc7-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-130">**ClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="52dc7-130">**ClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-131">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52dc7-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-133">Especifica si la imagen del papel tapiz se muestra en el cliente.</span><span class="sxs-lookup"><span data-stu-id="52dc7-133">Specifies whether the wallpaper image is displayed on the client.</span></span> <span data-ttu-id="52dc7-134">No mostrar la imagen del papel tapiz puede ahorrar recursos del sistema al reducir el tiempo necesario para volver a dibujar la pantalla.</span><span class="sxs-lookup"><span data-stu-id="52dc7-134">Not displaying the wallpaper image can save system resources by decreasing the time required to repaint the screen.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="52dc7-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="52dc7-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="52dc7-136">La imagen del papel tapiz no se muestra en el cliente.</span><span class="sxs-lookup"><span data-stu-id="52dc7-136">The wallpaper image is not displayed on the client.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="52dc7-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="52dc7-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="52dc7-138">La imagen del papel tapiz se muestra en el cliente.</span><span class="sxs-lookup"><span data-stu-id="52dc7-138">The wallpaper image is displayed on the client.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52dc7-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="52dc7-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="52dc7-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-142">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="52dc7-142">Description of the object.</span></span>

<span data-ttu-id="52dc7-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52dc7-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-144">**InitialProgramPath**</span><span class="sxs-lookup"><span data-stu-id="52dc7-144">**InitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="52dc7-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-147">El nombre y la ruta de acceso del programa que el usuario ejecutará inmediatamente después de iniciar sesión en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="52dc7-147">The name and the path of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-148">**InitialProgramPolicy**</span><span class="sxs-lookup"><span data-stu-id="52dc7-148">**InitialProgramPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52dc7-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="52dc7-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-151">La Directiva que el servidor usa para determinar la ruta de acceso y el nombre de archivo del programa de inicio, así como el nombre de la carpeta en la que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="52dc7-151">The policy the server uses to determine the startup program path and file name, and the name of the folder it is located in.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="52dc7-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuario** (0)</span><span class="sxs-lookup"><span data-stu-id="52dc7-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="52dc7-153">La configuración del programa de inicio del usuario está en vigor.</span><span class="sxs-lookup"><span data-stu-id="52dc7-153">The user's startup program settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="52dc7-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Invalidación de servidor** (1)</span><span class="sxs-lookup"><span data-stu-id="52dc7-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="52dc7-155">El servidor invalida la configuración del programa de inicio del usuario.</span><span class="sxs-lookup"><span data-stu-id="52dc7-155">The user's startup program settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>

<span data-ttu-id="52dc7-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Modo de aplicación única** (2)</span><span class="sxs-lookup"><span data-stu-id="52dc7-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Single-App Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="52dc7-157">En esta sesión solo se ejecutará una aplicación.</span><span class="sxs-lookup"><span data-stu-id="52dc7-157">Only a single application will be run in this session.</span></span> <span data-ttu-id="52dc7-158">Se omite la información del programa de inicio.</span><span class="sxs-lookup"><span data-stu-id="52dc7-158">The startup program information is ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52dc7-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="52dc7-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-160">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="52dc7-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-162">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="52dc7-162">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-163">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="52dc7-163">The date the object was installed.</span></span> <span data-ttu-id="52dc7-164">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="52dc7-164">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="52dc7-165">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52dc7-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-166">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="52dc7-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="52dc7-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-169">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="52dc7-169">The name of the object.</span></span>

<span data-ttu-id="52dc7-170">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52dc7-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-171">**PolicySourceClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="52dc7-171">**PolicySourceClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-172">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52dc7-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-174">Indica si la propiedad **ClientWallPaper** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="52dc7-174">Indicates whether the **ClientWallPaper** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="52dc7-175">0</span><span class="sxs-lookup"><span data-stu-id="52dc7-175">0</span></span>
</dt> <dd>

<span data-ttu-id="52dc7-176">Servidor</span><span class="sxs-lookup"><span data-stu-id="52dc7-176">Server</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-177">1</span><span class="sxs-lookup"><span data-stu-id="52dc7-177">1</span></span>
</dt> <dd>

<span data-ttu-id="52dc7-178">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="52dc7-178">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-179">2</span><span class="sxs-lookup"><span data-stu-id="52dc7-179">2</span></span>
</dt> <dd>

<span data-ttu-id="52dc7-180">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="52dc7-180">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52dc7-181">**PolicySourceInitialProgramPath**</span><span class="sxs-lookup"><span data-stu-id="52dc7-181">**PolicySourceInitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-182">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52dc7-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-184">Indica si la propiedad **InitialProgramPath** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="52dc7-184">Indicates whether the **InitialProgramPath** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="52dc7-185">0</span><span class="sxs-lookup"><span data-stu-id="52dc7-185">0</span></span>
</dt> <dd>

<span data-ttu-id="52dc7-186">Servidor</span><span class="sxs-lookup"><span data-stu-id="52dc7-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-187">1</span><span class="sxs-lookup"><span data-stu-id="52dc7-187">1</span></span>
</dt> <dd>

<span data-ttu-id="52dc7-188">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="52dc7-188">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-189">2</span><span class="sxs-lookup"><span data-stu-id="52dc7-189">2</span></span>
</dt> <dd>

<span data-ttu-id="52dc7-190">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="52dc7-190">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52dc7-191">**PolicySourceStartIn**</span><span class="sxs-lookup"><span data-stu-id="52dc7-191">**PolicySourceStartIn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-192">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52dc7-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-194">Indica si la propiedad de **Inicio** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="52dc7-194">Indicates whether the **StartIn** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="52dc7-195">0</span><span class="sxs-lookup"><span data-stu-id="52dc7-195">0</span></span>
</dt> <dd>

<span data-ttu-id="52dc7-196">Servidor</span><span class="sxs-lookup"><span data-stu-id="52dc7-196">Server</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-197">1</span><span class="sxs-lookup"><span data-stu-id="52dc7-197">1</span></span>
</dt> <dd>

<span data-ttu-id="52dc7-198">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="52dc7-198">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-199">2</span><span class="sxs-lookup"><span data-stu-id="52dc7-199">2</span></span>
</dt> <dd>

<span data-ttu-id="52dc7-200">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="52dc7-200">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52dc7-201">**Startin**</span><span class="sxs-lookup"><span data-stu-id="52dc7-201">**Startin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="52dc7-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-204">La ruta de acceso del directorio de trabajo del programa que el usuario ejecutará inmediatamente después de iniciar sesión en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="52dc7-204">The path of the working directory of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="52dc7-205">**Estado**</span><span class="sxs-lookup"><span data-stu-id="52dc7-205">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-206">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="52dc7-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-208">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="52dc7-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-209">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="52dc7-209">Current status of the object.</span></span> <span data-ttu-id="52dc7-210">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="52dc7-210">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="52dc7-211">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="52dc7-211">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="52dc7-212">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="52dc7-212">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="52dc7-213">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="52dc7-213">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="52dc7-214">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="52dc7-214">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="52dc7-215">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52dc7-215">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="52dc7-216">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="52dc7-216">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52dc7-217">("Error")</span><span class="sxs-lookup"><span data-stu-id="52dc7-217">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52dc7-218">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="52dc7-218">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52dc7-219">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="52dc7-219">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52dc7-220">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="52dc7-220">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52dc7-221">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="52dc7-221">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52dc7-222">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="52dc7-222">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52dc7-223">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="52dc7-223">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="52dc7-224">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="52dc7-224">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52dc7-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="52dc7-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52dc7-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52dc7-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52dc7-227">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="52dc7-227">The name of the terminal.</span></span>

<span data-ttu-id="52dc7-228">Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="52dc7-228">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52dc7-229">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52dc7-229">Remarks</span></span>

<span data-ttu-id="52dc7-230">Tenga en cuenta que los Winstations que están asociados a la sesión de consola no pueden tener acceso a los métodos y las propiedades de esta clase.</span><span class="sxs-lookup"><span data-stu-id="52dc7-230">Be aware that Winstations that are associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="52dc7-231">Si se realiza un intento de hacerlo especificando "Console" como el valor de la propiedad **TerminalName** , los métodos de este objeto devuelven **WBEM \_ E \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="52dc7-231">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="52dc7-232">Este código de error también se devuelve si una estación de ventana intenta llamar a métodos de este objeto para agregar o modificar las propiedades de seguridad de las cuentas LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="52dc7-232">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="52dc7-233">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="52dc7-233">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="52dc7-234">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="52dc7-234">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="52dc7-235">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="52dc7-235">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="52dc7-236">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="52dc7-236">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="52dc7-237">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="52dc7-237">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="52dc7-238">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="52dc7-238">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="52dc7-239">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="52dc7-239">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="52dc7-240">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="52dc7-240">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="52dc7-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52dc7-241">Requirements</span></span>



| <span data-ttu-id="52dc7-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="52dc7-242">Requirement</span></span> | <span data-ttu-id="52dc7-243">Value</span><span class="sxs-lookup"><span data-stu-id="52dc7-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52dc7-244">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52dc7-244">Minimum supported client</span></span><br/> | <span data-ttu-id="52dc7-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52dc7-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52dc7-246">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52dc7-246">Minimum supported server</span></span><br/> | <span data-ttu-id="52dc7-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52dc7-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52dc7-248">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="52dc7-248">Namespace</span></span><br/>                | <span data-ttu-id="52dc7-249">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="52dc7-249">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="52dc7-250">MOF</span><span class="sxs-lookup"><span data-stu-id="52dc7-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52dc7-251"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52dc7-251"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="52dc7-252">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52dc7-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52dc7-253"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52dc7-253"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52dc7-254">Vea también</span><span class="sxs-lookup"><span data-stu-id="52dc7-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52dc7-255">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="52dc7-255">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

