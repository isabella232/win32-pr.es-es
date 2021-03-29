---
description: Win32 \_ StartupCommand&\# 8194; La clase WMI representa un comando que se ejecuta automáticamente cuando un usuario inicia sesión en el sistema del equipo.
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Win32_StartupCommand (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907456"
---
# <a name="win32_startupcommand-class"></a><span data-ttu-id="47457-103">\_Clase Win32 StartupCommand</span><span class="sxs-lookup"><span data-stu-id="47457-103">Win32\_StartupCommand class</span></span>

<span data-ttu-id="47457-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ StartupCommand de Win32** representa un comando que se ejecuta automáticamente cuando un usuario inicia sesión en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="47457-104">The **Win32\_StartupCommand** [WMI class](../wmisdk/retrieving-a-class.md) represents a command that runs automatically when a user logs onto the computer system.</span></span>

<span data-ttu-id="47457-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="47457-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="47457-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="47457-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="47457-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47457-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a><span data-ttu-id="47457-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="47457-108">Members</span></span>

<span data-ttu-id="47457-109">La **clase \_ StartupCommand de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="47457-109">The **Win32\_StartupCommand** class has these types of members:</span></span>

-   [<span data-ttu-id="47457-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47457-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47457-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47457-111">Properties</span></span>

<span data-ttu-id="47457-112">La **clase \_ StartupCommand de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="47457-112">The **Win32\_StartupCommand** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47457-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="47457-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47457-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47457-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47457-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47457-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47457-116">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="47457-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="47457-117">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="47457-117">Short textual description of the current object.</span></span>

<span data-ttu-id="47457-118">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="47457-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="47457-119">**Comando**</span><span class="sxs-lookup"><span data-stu-id="47457-119">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47457-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47457-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47457-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47457-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47457-122">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")</span><span class="sxs-lookup"><span data-stu-id="47457-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>
</dt> </dl>

<span data-ttu-id="47457-123">Comando ejecutado por el comando de inicio.</span><span class="sxs-lookup"><span data-stu-id="47457-123">Command run by the startup command.</span></span>

<span data-ttu-id="47457-124">WMI obtiene estos datos de la clave del registro</span><span class="sxs-lookup"><span data-stu-id="47457-124">WMI obtains this data from the registry key</span></span>

<span data-ttu-id="47457-125">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Run**</span><span class="sxs-lookup"><span data-stu-id="47457-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Run**</span></span>

<span data-ttu-id="47457-126">Ejemplo: "C: \\ Windows \\notepad.exe myfile.txt"</span><span class="sxs-lookup"><span data-stu-id="47457-126">Example: "C:\\Windows\\notepad.exe myfile.txt"</span></span>

</dd> <dt>

<span data-ttu-id="47457-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="47457-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47457-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47457-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47457-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47457-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47457-130">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="47457-130">Textual description of the current object.</span></span>

<span data-ttu-id="47457-131">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="47457-131">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="47457-132">**Ubicación**</span><span class="sxs-lookup"><span data-stu-id="47457-132">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47457-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47457-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47457-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47457-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47457-135">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CURRENTVERSION \\ \\ Windows")</span><span class="sxs-lookup"><span data-stu-id="47457-135">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|\\\\SOFTWARE\\\\MICROSOFT\\\\WINDOWS\\\\CURRENTVERSION\\\\Windows")</span></span>
</dt> </dl>

<span data-ttu-id="47457-136">Ruta de acceso en la que el comando de inicio reside en el sistema de archivos de disco.</span><span class="sxs-lookup"><span data-stu-id="47457-136">Path where the startup command resides on the disk file system.</span></span>

<span data-ttu-id="47457-137">Por ejemplo: HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="47457-137">For example: HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

<span data-ttu-id="47457-138">**Startup** ("startup")</span><span class="sxs-lookup"><span data-stu-id="47457-138">**Startup** ("Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

<span data-ttu-id="47457-139">**Inicio común** ("Inicio común")</span><span class="sxs-lookup"><span data-stu-id="47457-139">**Common Startup** ("Common Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

<span data-ttu-id="47457-140">**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")</span><span class="sxs-lookup"><span data-stu-id="47457-140">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

<span data-ttu-id="47457-141">**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices")</span><span class="sxs-lookup"><span data-stu-id="47457-141">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="47457-142">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="47457-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47457-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47457-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47457-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47457-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47457-145">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| File Structures \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| cFileName")</span><span class="sxs-lookup"><span data-stu-id="47457-145">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Structures\|[**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa)\|cFileName")</span></span>
</dt> </dl>

<span data-ttu-id="47457-146">Nombre de archivo del comando de inicio.</span><span class="sxs-lookup"><span data-stu-id="47457-146">File name of the startup command.</span></span>

<span data-ttu-id="47457-147">Ejemplo: "búsqueda rápida"</span><span class="sxs-lookup"><span data-stu-id="47457-147">Example: "FindFast"</span></span>

</dd> <dt>

<span data-ttu-id="47457-148">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="47457-148">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47457-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47457-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47457-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47457-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47457-151">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="47457-151">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="47457-152">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="47457-152">Identifier by which the current object is known.</span></span>

<span data-ttu-id="47457-153">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="47457-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="47457-154">**User**</span><span class="sxs-lookup"><span data-stu-id="47457-154">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47457-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47457-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47457-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47457-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47457-157">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="47457-157">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="47457-158">Nombre de usuario para el que se ejecutará este comando de inicio.</span><span class="sxs-lookup"><span data-stu-id="47457-158">User name for whom this startup command will run.</span></span>

<span data-ttu-id="47457-159">Ejemplo: "midominio mi \\ nombre"</span><span class="sxs-lookup"><span data-stu-id="47457-159">Example: "mydomain\\myname"</span></span>

</dd> <dt>

<span data-ttu-id="47457-160">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="47457-160">**UserSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47457-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47457-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47457-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47457-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47457-163">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="47457-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="47457-164">La propiedad UserSID indica el SID del usuario para el que se ejecutará este comando de inicio.</span><span class="sxs-lookup"><span data-stu-id="47457-164">The UserSID property indicates the SID of the user for whom this startup command will run.</span></span> <span data-ttu-id="47457-165">Esa propiedad de usuario puede estar vacía, pero UserSID todavía tiene un valor si no se puede resolver el nombre de usuario (por ejemplo, en el caso de un usuario eliminado).</span><span class="sxs-lookup"><span data-stu-id="47457-165">That User property may be empty but UserSID still has a value if the user name can't be resolved (like in the case of a deleted user).</span></span> <span data-ttu-id="47457-166">La propiedad es útil para distinguir entre los comandos asociados a dos usuarios distintos con nombres sin resolver.</span><span class="sxs-lookup"><span data-stu-id="47457-166">The property is helpful to distinguish between commands associated w/ two different users with unresolved names.</span></span> <span data-ttu-id="47457-167">Puede ser NULL cuando el comando está asociado a elementos que no identifican realmente a un usuario como todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="47457-167">It may be NULL when the command is associated with items not actually identifying a user like All Users.</span></span>

<span data-ttu-id="47457-168">Ejemplo: S-1-5-21-1579938362-1064596589-3161144252-1006</span><span class="sxs-lookup"><span data-stu-id="47457-168">Example:S-1-5-21-1579938362-1064596589-3161144252-1006</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47457-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47457-169">Remarks</span></span>

<span data-ttu-id="47457-170">La **clase \_ StartupCommand de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="47457-170">The **Win32\_StartupCommand** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="47457-171">El inicio del equipo no termina después de que se haya cargado el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="47457-171">Computer startup does not end after the operating system has been loaded.</span></span> <span data-ttu-id="47457-172">En su lugar, se puede configurar el sistema operativo Windows para que se ejecuten los comandos de inicio cada vez que se inicie Windows.</span><span class="sxs-lookup"><span data-stu-id="47457-172">Instead, the Windows operating system can be configured so that startup commands are run each time Windows starts.</span></span> <span data-ttu-id="47457-173">Los comandos de inicio se almacenan en el registro o como parte del perfil de usuario y se usan para iniciar automáticamente las aplicaciones o los scripts especificados cada vez que se carga Windows.</span><span class="sxs-lookup"><span data-stu-id="47457-173">Startup commands are stored in the registry or as part of the user profile and are used to automatically start specified scripts or applications each time Windows is loaded.</span></span>

<span data-ttu-id="47457-174">En la mayoría de los casos, los programas de inicio automático son útiles. garantizan que ciertas aplicaciones, como las herramientas antivirus, se inician y ejecutan automáticamente cada vez que se carga Windows.</span><span class="sxs-lookup"><span data-stu-id="47457-174">In most cases, autostart programs are useful; they ensure that certain applications, such as antivirus tools, are automatically started and run each time Windows is loaded.</span></span> <span data-ttu-id="47457-175">Sin embargo, los programas de inicio automático también pueden ser responsables de problemas como los siguientes:</span><span class="sxs-lookup"><span data-stu-id="47457-175">However, autostart programs also can be responsible for problems such as:</span></span>

-   <span data-ttu-id="47457-176">Equipos que tardan mucho tiempo en iniciarse.</span><span class="sxs-lookup"><span data-stu-id="47457-176">Computers that take an exceptionally long time to start.</span></span> <span data-ttu-id="47457-177">Esto puede ser el resultado de un gran número de aplicaciones que se deben iniciar cada vez que se inicia Windows.</span><span class="sxs-lookup"><span data-stu-id="47457-177">This might be the result of a large number of applications that must be started each time Windows starts.</span></span>
-   <span data-ttu-id="47457-178">Aplicaciones que se representan en la barra de tareas o en el administrador de tareas, aunque el usuario no las haya iniciado.</span><span class="sxs-lookup"><span data-stu-id="47457-178">Applications that are represented in the Taskbar or in Task Manager, even though the user did not start them.</span></span> <span data-ttu-id="47457-179">Aunque estas aplicaciones no causan necesariamente problemas, pueden dar lugar a llamadas al Departamento de soporte técnico por parte de usuarios que se confunden en el lugar en el que provienen estos programas y por qué se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="47457-179">Although these applications do not necessarily cause problems, they can result in help desk calls from users who are confused as to where these programs came from and why they are running.</span></span>
-   <span data-ttu-id="47457-180">Equipos que experimentan problemas incluso cuando parecen inactivos.</span><span class="sxs-lookup"><span data-stu-id="47457-180">Computers experiencing problems even when they seem idle.</span></span> <span data-ttu-id="47457-181">A menudo se realiza un seguimiento de estos problemas con los comandos de inicio que se ejecutan cuando nadie es consciente de que se están ejecutando.</span><span class="sxs-lookup"><span data-stu-id="47457-181">These problems are often traced to startup commands that are running when no one is aware that they are running.</span></span>

<span data-ttu-id="47457-182">La identificación de las aplicaciones y los scripts que se ejecutan automáticamente en el inicio es una tarea administrativa importante pero difícil, porque los comandos de inicio se pueden almacenar en muchas ubicaciones diferentes:</span><span class="sxs-lookup"><span data-stu-id="47457-182">Identifying the applications and scripts that automatically run at startup is an important but difficult administrative task, because startup commands can be stored in many different locations:</span></span>

-   <span data-ttu-id="47457-183">HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="47457-183">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="47457-184">HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="47457-184">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="47457-185">HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="47457-185">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="47457-186">HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="47457-186">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="47457-187">HKU \\ ProgID \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="47457-187">HKU\\ProgID\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="47457-188">SystemDrive \\ documentos y configuración \\ todos los usuarios \\ menú Inicio \\ programas \\ Inicio</span><span class="sxs-lookup"><span data-stu-id="47457-188">systemdrive\\Documents and Settings\\All Users\\Start Menu\\Programs\\Startup</span></span>
-   <span data-ttu-id="47457-189">unidadDelSistema \\ documentos y configuración \\ nombre de usuario \\ Inicio menú \\ programas \\ Inicio</span><span class="sxs-lookup"><span data-stu-id="47457-189">systemdrive\\Documents and Settings\\username\\Start Menu\\Programs\\Startup</span></span>

<span data-ttu-id="47457-190">Puede usar la clase Win32 StartupCommand de WMI \_ para enumerar programas de inicio automático con independencia de dónde se almacene la información.</span><span class="sxs-lookup"><span data-stu-id="47457-190">You can use the WMI Win32\_StartupCommand class to enumerate autostart programs regardless of where the information is stored.</span></span>

<span data-ttu-id="47457-191">El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro.</span><span class="sxs-lookup"><span data-stu-id="47457-191">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="47457-192">Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio.</span><span class="sxs-lookup"><span data-stu-id="47457-192">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="47457-193">Para obtener más información, vea [ejecutar operaciones con privilegios](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="47457-193">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="47457-194">Puede cambiar los valores del registro donde **Win32 \_ StartupCommand** obtiene los datos mediante una llamada a los métodos del [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) WMI en el script o en C++.</span><span class="sxs-lookup"><span data-stu-id="47457-194">You can change the registry values where **Win32\_StartupCommand** obtains data by calling the WMI [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) methods in script or in C++.</span></span> <span data-ttu-id="47457-195">Para obtener más información, vea [modificar el registro del sistema](../wmisdk/modifying-the-system-registry.md).</span><span class="sxs-lookup"><span data-stu-id="47457-195">For more information, see [Modifying the System Registry](../wmisdk/modifying-the-system-registry.md).</span></span>

## <a name="examples"></a><span data-ttu-id="47457-196">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="47457-196">Examples</span></span>

<span data-ttu-id="47457-197">El siguiente VBScript enumera los comandos de inicio en un equipo.</span><span class="sxs-lookup"><span data-stu-id="47457-197">The following VBScript enumerates the startup commands on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
Next
```



## <a name="requirements"></a><span data-ttu-id="47457-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47457-198">Requirements</span></span>



| <span data-ttu-id="47457-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="47457-199">Requirement</span></span> | <span data-ttu-id="47457-200">Value</span><span class="sxs-lookup"><span data-stu-id="47457-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47457-201">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47457-201">Minimum supported client</span></span><br/> | <span data-ttu-id="47457-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47457-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47457-203">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47457-203">Minimum supported server</span></span><br/> | <span data-ttu-id="47457-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47457-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47457-205">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="47457-205">Namespace</span></span><br/>                | <span data-ttu-id="47457-206">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="47457-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="47457-207">MOF</span><span class="sxs-lookup"><span data-stu-id="47457-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47457-208"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47457-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="47457-209">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47457-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47457-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47457-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47457-211">Vea también</span><span class="sxs-lookup"><span data-stu-id="47457-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47457-212">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="47457-212">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="47457-213">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="47457-213">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
