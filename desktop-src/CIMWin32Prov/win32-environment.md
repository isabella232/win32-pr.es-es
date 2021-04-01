---
description: Representa un entorno o una configuración de entorno del sistema en un equipo Windows.
ms.assetid: da7ee891-c759-4046-a9d8-d3caf66ab5a9
ms.tgt_platform: multiple
title: Win32_Environment (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Environment
- Win32_Environment.Caption
- Win32_Environment.Description
- Win32_Environment.InstallDate
- Win32_Environment.Status
- Win32_Environment.Name
- Win32_Environment.SystemVariable
- Win32_Environment.UserName
- Win32_Environment.VariableValue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b7267e3ac03c14cfc6ad6ca73ede42cc8478b41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907523"
---
# <a name="win32_environment-class"></a><span data-ttu-id="81ef4-103">\_Clase de entorno Win32</span><span class="sxs-lookup"><span data-stu-id="81ef4-103">Win32\_Environment class</span></span>

<span data-ttu-id="81ef4-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ entorno Win32** representa un entorno o una configuración de entorno del sistema en un equipo Windows.</span><span class="sxs-lookup"><span data-stu-id="81ef4-104">The **Win32\_Environment** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an environment or system environment setting on a Windows computer system.</span></span> <span data-ttu-id="81ef4-105">Al consultar esta clase se devuelven las variables de entorno que se encuentran en:</span><span class="sxs-lookup"><span data-stu-id="81ef4-105">Querying this class returns environment variables found in:</span></span>

<span data-ttu-id="81ef4-106">**HKEY \_ Entorno de \_ equipo local** \\  \\ **CurrentControlSet** \\ **control** \\ **SessionManager** \\ **Environment**</span><span class="sxs-lookup"><span data-stu-id="81ef4-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="81ef4-107">y</span><span class="sxs-lookup"><span data-stu-id="81ef4-107">and</span></span>

<span data-ttu-id="81ef4-108">**HKEY \_** \\ Entorno de **< usuario >** de usuarios \\ </span><span class="sxs-lookup"><span data-stu-id="81ef4-108">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="81ef4-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="81ef4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="81ef4-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="81ef4-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ef4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81ef4-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4D2-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_Environment : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  boolean  SystemVariable;
  string   UserName;
  string   VariableValue;
};
```

## <a name="members"></a><span data-ttu-id="81ef4-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="81ef4-112">Members</span></span>

<span data-ttu-id="81ef4-113">La clase de **\_ entorno Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="81ef4-113">The **Win32\_Environment** class has these types of members:</span></span>

-   [<span data-ttu-id="81ef4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81ef4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81ef4-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81ef4-115">Properties</span></span>

<span data-ttu-id="81ef4-116">La clase de **\_ entorno Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="81ef4-116">The **Win32\_Environment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81ef4-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="81ef4-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ef4-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81ef4-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81ef4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-120">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="81ef4-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="81ef4-121">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="81ef4-121">A short textual description of the object.</span></span>

<span data-ttu-id="81ef4-122">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81ef4-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ef4-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81ef4-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ef4-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81ef4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81ef4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-126">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="81ef4-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="81ef4-127">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="81ef4-127">A textual description of the object.</span></span>

<span data-ttu-id="81ef4-128">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81ef4-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ef4-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="81ef4-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ef4-130">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="81ef4-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81ef4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-132">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="81ef4-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="81ef4-133">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="81ef4-133">Indicates when the object was installed.</span></span> <span data-ttu-id="81ef4-134">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="81ef4-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="81ef4-135">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81ef4-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81ef4-136">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="81ef4-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ef4-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81ef4-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ef4-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-139">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="81ef4-139">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="81ef4-140">Cadena de caracteres que especifica el nombre de una variable de entorno basada en Windows.</span><span class="sxs-lookup"><span data-stu-id="81ef4-140">Character string that specifies the name of a Windows-based environment variable.</span></span> <span data-ttu-id="81ef4-141">Al especificar el nombre de una variable que aún no existe, una aplicación crea una nueva variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="81ef4-141">By specifying the name of a variable that does not yet exist, an application creates a new environment variable.</span></span>

<span data-ttu-id="81ef4-142">Ejemplo: "path"</span><span class="sxs-lookup"><span data-stu-id="81ef4-142">Example: "Path"</span></span>

</dd> <dt>

<span data-ttu-id="81ef4-143">**Estado**</span><span class="sxs-lookup"><span data-stu-id="81ef4-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ef4-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81ef4-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81ef4-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-146">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="81ef4-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="81ef4-147">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="81ef4-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="81ef4-148">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="81ef4-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="81ef4-149">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="81ef4-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="81ef4-150">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="81ef4-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="81ef4-151">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="81ef4-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="81ef4-152">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="81ef4-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="81ef4-153">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="81ef4-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="81ef4-154">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81ef4-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="81ef4-155">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="81ef4-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="81ef4-156">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="81ef4-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="81ef4-157">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="81ef4-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="81ef4-158">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="81ef4-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81ef4-159">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="81ef4-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="81ef4-160">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="81ef4-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="81ef4-161">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="81ef4-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="81ef4-162">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="81ef4-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="81ef4-163">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="81ef4-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="81ef4-164">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="81ef4-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="81ef4-165">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="81ef4-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="81ef4-166">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="81ef4-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="81ef4-167">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="81ef4-167">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81ef4-168">**SystemVariable**</span><span class="sxs-lookup"><span data-stu-id="81ef4-168">**SystemVariable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ef4-169">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="81ef4-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81ef4-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-171">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="81ef4-171">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="81ef4-172">Indica si la variable es una variable del sistema.</span><span class="sxs-lookup"><span data-stu-id="81ef4-172">Indicates whether the variable is a system variable.</span></span> <span data-ttu-id="81ef4-173">El sistema operativo establece una variable del sistema y es independiente de la configuración del entorno del usuario.</span><span class="sxs-lookup"><span data-stu-id="81ef4-173">A system variable is set by the operating system, and is independent from user environment settings.</span></span>

</dd> <dt>

<span data-ttu-id="81ef4-174">**UserName**</span><span class="sxs-lookup"><span data-stu-id="81ef4-174">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ef4-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81ef4-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="81ef4-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-177">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="81ef4-177">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="81ef4-178">Nombre del propietario de la configuración del entorno.</span><span class="sxs-lookup"><span data-stu-id="81ef4-178">Name of the owner of the environment setting.</span></span> <span data-ttu-id="81ef4-179">Se establece en <SYSTEM> para la configuración específica del sistema basado en Windows (en oposición a un usuario específico) y <DEFAULT> para la configuración de usuario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="81ef4-179">It is set to <SYSTEM> for settings that are specific to the Windows-based system (as opposed to a specific user) and <DEFAULT> for default user settings.</span></span>

<span data-ttu-id="81ef4-180">Ejemplo: "JSmith"</span><span class="sxs-lookup"><span data-stu-id="81ef4-180">Example: "JSmith"</span></span>

</dd> <dt>

<span data-ttu-id="81ef4-181">**VariableValue**</span><span class="sxs-lookup"><span data-stu-id="81ef4-181">**VariableValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ef4-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="81ef4-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-183">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="81ef4-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="81ef4-184">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="81ef4-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="81ef4-185">Variable de marcador de posición de una variable de entorno basada en Windows.</span><span class="sxs-lookup"><span data-stu-id="81ef4-185">Placeholder variable of a Windows-based environment variable.</span></span> <span data-ttu-id="81ef4-186">La información como el directorio del sistema de archivos puede cambiar de equipo a equipo.</span><span class="sxs-lookup"><span data-stu-id="81ef4-186">Information like the file system directory can change from computer to computer.</span></span> <span data-ttu-id="81ef4-187">El sistema operativo sustituye los marcadores de posición por estos.</span><span class="sxs-lookup"><span data-stu-id="81ef4-187">The operating system substitutes placeholders for these.</span></span>

<span data-ttu-id="81ef4-188">Ejemplo: "% SystemRoot%"</span><span class="sxs-lookup"><span data-stu-id="81ef4-188">Example: "%SystemRoot%"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81ef4-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81ef4-189">Remarks</span></span>

<span data-ttu-id="81ef4-190">La clase de **\_ entorno de Win32** se deriva de [**\_ SystemResource CIM**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="81ef4-190">The **Win32\_Environment** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span> <span data-ttu-id="81ef4-191">Puede usar esta clase para buscar las rutas de acceso de carpetas especiales, como la carpeta del sistema o los archivos de programa en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="81ef4-191">You can use this class to find the paths of special folders such as the System folder or Program files on a remote machine.</span></span> <span data-ttu-id="81ef4-192">Algunos ejemplos son: WINDIR, raízDelSistema, ProgramFiles y userprofile.</span><span class="sxs-lookup"><span data-stu-id="81ef4-192">Some examples are: windir, systemroot, programfiles, and userprofile.</span></span> <span data-ttu-id="81ef4-193">**Win32 \_** Básicamente, el entorno devuelve lo que se puede encontrar en:</span><span class="sxs-lookup"><span data-stu-id="81ef4-193">**Win32\_Environment** basically returns what can be found in:</span></span>

<span data-ttu-id="81ef4-194">**HKEY \_ Entorno de \_ equipo local** \\  \\ **CurrentControlSet** \\ **control** \\ **SessionManager** \\ **Environment**</span><span class="sxs-lookup"><span data-stu-id="81ef4-194">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="81ef4-195">y</span><span class="sxs-lookup"><span data-stu-id="81ef4-195">and</span></span>

<span data-ttu-id="81ef4-196">**HKEY \_** \\ Entorno de **< usuario >** de usuarios \\ </span><span class="sxs-lookup"><span data-stu-id="81ef4-196">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="81ef4-197">El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro.</span><span class="sxs-lookup"><span data-stu-id="81ef4-197">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="81ef4-198">Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio.</span><span class="sxs-lookup"><span data-stu-id="81ef4-198">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="81ef4-199">Para obtener más información, vea [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="81ef4-199">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="81ef4-200">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="81ef4-200">Examples</span></span>

<span data-ttu-id="81ef4-201">La [lista de variables de entorno en un equipo Perl de](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) ejemplo usa WMI para devolver información acerca de todas las variables de entorno de un equipo.</span><span class="sxs-lookup"><span data-stu-id="81ef4-201">The [List Environment Variables on a Computer](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl sample uses WMI to return information about all the environment variables on a computer.</span></span>

<span data-ttu-id="81ef4-202">En el siguiente ejemplo de código de VBScript se enumeran las variables de entorno en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="81ef4-202">The following VBScript code example enumerates the environment variables on the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colVar = objWMIService.ExecQuery("Select * from Win32_Environment")
For Each objVar in colVar
    Wscript.Echo "Description: " & objVar.Description & VBNewLine _
               & "Name: " & objVar.Name & VBNewLine _
               & "System Variable: " & objVar.SystemVariable & VBNewLine _
               & "User Name: " & objVar.UserName & VBNewLine _
               & "Variable Value: " & objVar.VariableValue 
Next
```



<span data-ttu-id="81ef4-203">El siguiente ejemplo de código de VBScript cambia una variable de entorno denominada \_ tipo de compilación a una entrada de valor por el usuario.</span><span class="sxs-lookup"><span data-stu-id="81ef4-203">The following VBScript code example changes an environment variable named BUILD\_TYPE to a value input by the user.</span></span> <span data-ttu-id="81ef4-204">El script supone que la variable de tipo de compilación \_ ya existe.</span><span class="sxs-lookup"><span data-stu-id="81ef4-204">The script assumes that the BUILD\_TYPE variable already exists.</span></span> <span data-ttu-id="81ef4-205">Si no existe, el script finaliza.</span><span class="sxs-lookup"><span data-stu-id="81ef4-205">If it does not exist then the script ends.</span></span> <span data-ttu-id="81ef4-206">Se comprueba el valor de entrada: debe ser "Build1", "Build2" o "Build3" y no se acepta ningún otro valor.</span><span class="sxs-lookup"><span data-stu-id="81ef4-206">The input value is checked: it must be either "Build1", "Build2", or "Build3", and no other value is accepted.</span></span> <span data-ttu-id="81ef4-207">La función [UCase](https://msdn.microsoft.com/library/aa902519.aspx) de VBScript hace que la entrada no distinga mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="81ef4-207">The VBScript [UCase](https://msdn.microsoft.com/library/aa902519.aspx) function makes the input case-insensitive.</span></span> <span data-ttu-id="81ef4-208">Si lo que se escribe no es uno de los tres valores aceptables, el script finaliza.</span><span class="sxs-lookup"><span data-stu-id="81ef4-208">If what is typed in is not one of the three acceptable values, the script ends.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_Environment")
Found = False
For Each objItem in colItems
    If objItem.Name = "BUILD_TYPE" Then
    Found = True
    Change = UCase(InputBox("BUILD_TYPE currently = " & objItem.VariableValue & VBNewLine _
                          & "Change options are Build1, Build2, Build3 "))
        If UCase(Change) = "BUILD1" OR Change = "BUILD2" OR Change = "BUILD3" Then
            objItem.VariableValue = Change
            objItem.Put_
        WScript.Echo "BUILD_TYPE changed to " & objItem.VariableValue
        Else 
        WScript.Echo "No input or unacceptable input." & " No change to BUILD_TYPE"
        End If
    End If
Next
If Found = False Then
    WScript.Echo "User-defined environment variable BUILD_TYPE not found."
End If
```



## <a name="requirements"></a><span data-ttu-id="81ef4-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81ef4-209">Requirements</span></span>



| <span data-ttu-id="81ef4-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="81ef4-210">Requirement</span></span> | <span data-ttu-id="81ef4-211">Value</span><span class="sxs-lookup"><span data-stu-id="81ef4-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81ef4-212">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81ef4-212">Minimum supported client</span></span><br/> | <span data-ttu-id="81ef4-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81ef4-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81ef4-214">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81ef4-214">Minimum supported server</span></span><br/> | <span data-ttu-id="81ef4-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81ef4-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81ef4-216">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="81ef4-216">Namespace</span></span><br/>                | <span data-ttu-id="81ef4-217">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="81ef4-217">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81ef4-218">MOF</span><span class="sxs-lookup"><span data-stu-id="81ef4-218">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81ef4-219"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81ef4-219"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81ef4-220">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81ef4-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81ef4-221"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81ef4-221"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81ef4-222">Vea también</span><span class="sxs-lookup"><span data-stu-id="81ef4-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ef4-223">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="81ef4-223">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dt>

<span data-ttu-id="81ef4-224">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81ef4-224">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

