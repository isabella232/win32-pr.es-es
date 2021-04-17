---
title: Win32_RDMSVirtualDesktopCollection (clase)
description: Crea y administra una colección de escritorios virtuales.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktopCollection clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSVirtualDesktopCollection de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a6da0c13b6ab223afc7afe6e92039a5388c6204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676707"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="a0889-105">\_Clase Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="a0889-105">Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="a0889-106">Crea y administra una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a0889-106">Creates and manages a virtual desktop collection.</span></span>

<span data-ttu-id="a0889-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a0889-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0889-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0889-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a><span data-ttu-id="a0889-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0889-109">Members</span></span>

<span data-ttu-id="a0889-110">La **clase \_ RDMSVirtualDesktopCollection de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a0889-110">The **Win32\_RDMSVirtualDesktopCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="a0889-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0889-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0889-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0889-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a0889-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0889-113">Methods</span></span>

<span data-ttu-id="a0889-114">La clase **Win32 \_ RDMSVirtualDesktopCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a0889-114">The **Win32\_RDMSVirtualDesktopCollection** class has these methods.</span></span>



| <span data-ttu-id="a0889-115">Método</span><span class="sxs-lookup"><span data-stu-id="a0889-115">Method</span></span>                                                                                            | <span data-ttu-id="a0889-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0889-116">Description</span></span>                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0889-117">**AddVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="a0889-117">**AddVirtualDesktop**</span></span>](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="a0889-118">Agrega un escritorio virtual a una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a0889-118">Adds a virtual desktop to a virtual desktop collection.</span></span><br/>                                                                              |
| [<span data-ttu-id="a0889-119">**CancelPatch**</span><span class="sxs-lookup"><span data-stu-id="a0889-119">**CancelPatch**</span></span>](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | <span data-ttu-id="a0889-120">Cancela un trabajo de aprovisionamiento de actualizaciones de software para las máquinas virtuales de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a0889-120">Cancels a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>                                 |
| [<span data-ttu-id="a0889-121">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="a0889-121">**GetInt32Property**</span></span>](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="a0889-122">Recupera un valor de propiedad de entero de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a0889-122">Retrieves an integer property value from a virtual desktop collection.</span></span><br/>                                                               |
| [<span data-ttu-id="a0889-123">**GetPatchProperties**</span><span class="sxs-lookup"><span data-stu-id="a0889-123">**GetPatchProperties**</span></span>](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | <span data-ttu-id="a0889-124">Recupera las propiedades de un trabajo de aprovisionamiento de actualizaciones de software para las máquinas virtuales de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a0889-124">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>             |
| [<span data-ttu-id="a0889-125">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="a0889-125">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="a0889-126">Recupera un valor de propiedad de cadena de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a0889-126">Retrieves a string property value from a virtual desktop collection.</span></span><br/>                                                                 |
| [<span data-ttu-id="a0889-127">**ProvisioningEnumerateJobs**</span><span class="sxs-lookup"><span data-stu-id="a0889-127">**ProvisioningEnumerateJobs**</span></span>](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | <span data-ttu-id="a0889-128">Enumera los trabajos de aprovisionamiento de escritorio virtual para este servicio.</span><span class="sxs-lookup"><span data-stu-id="a0889-128">Enumerates virtual desktop provisioning jobs for this service.</span></span><br/>                                                                       |
| [<span data-ttu-id="a0889-129">**ProvisioningJobCancel**</span><span class="sxs-lookup"><span data-stu-id="a0889-129">**ProvisioningJobCancel**</span></span>](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | <span data-ttu-id="a0889-130">Cancela un trabajo de aprovisionamiento de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="a0889-130">Cancels a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="a0889-131">**ProvisioningJobExecute**</span><span class="sxs-lookup"><span data-stu-id="a0889-131">**ProvisioningJobExecute**</span></span>](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | <span data-ttu-id="a0889-132">Ejecuta un trabajo de aprovisionamiento de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="a0889-132">Runs a virtual desktop provisioning job.</span></span><br/>                                                                                             |
| [<span data-ttu-id="a0889-133">**ProvisioningJobGetReport**</span><span class="sxs-lookup"><span data-stu-id="a0889-133">**ProvisioningJobGetReport**</span></span>](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | <span data-ttu-id="a0889-134">Obtiene un informe sobre el estado de un trabajo de aprovisionamiento de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="a0889-134">Gets a report about the status of a virtual desktop provisioning job.</span></span><br/>                                                                |
| [<span data-ttu-id="a0889-135">**ProvisioningPrepJob**</span><span class="sxs-lookup"><span data-stu-id="a0889-135">**ProvisioningPrepJob**</span></span>](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | <span data-ttu-id="a0889-136">Crea un trabajo de aprovisionamiento de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="a0889-136">Creates a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="a0889-137">**RemoveVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="a0889-137">**RemoveVirtualDesktop**</span></span>](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | <span data-ttu-id="a0889-138">Quita un escritorio virtual de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a0889-138">Removes a virtual desktop from a virtual desktop collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="a0889-139">**SchedulePatch**</span><span class="sxs-lookup"><span data-stu-id="a0889-139">**SchedulePatch**</span></span>](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | <span data-ttu-id="a0889-140">Programa un trabajo de aprovisionamiento de actualizaciones de software que instala las actualizaciones de software en las máquinas virtuales de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a0889-140">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span><br/> |
| [<span data-ttu-id="a0889-141">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="a0889-141">**SetInt32Property**</span></span>](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="a0889-142">Actualiza un valor de propiedad de entero de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a0889-142">Updates an integer property value of a virtual desktop collection.</span></span><br/>                                                                   |
| [<span data-ttu-id="a0889-143">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="a0889-143">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="a0889-144">Actualiza un valor de propiedad de cadena de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a0889-144">Updates a string property value of a virtual desktop collection.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="a0889-145">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0889-145">Properties</span></span>

<span data-ttu-id="a0889-146">La **clase \_ RDMSVirtualDesktopCollection de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a0889-146">The **Win32\_RDMSVirtualDesktopCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0889-147">**Alias**</span><span class="sxs-lookup"><span data-stu-id="a0889-147">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0889-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-149">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a0889-150">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a0889-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a0889-151">Obtiene o establece el alias de la colección.</span><span class="sxs-lookup"><span data-stu-id="a0889-151">Gets or sets the alias of the collection</span></span>

</dd> <dt>

<span data-ttu-id="a0889-152">**CollectionDescription**</span><span class="sxs-lookup"><span data-stu-id="a0889-152">**CollectionDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0889-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a0889-155">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0889-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0889-156">Obtiene o establece la descripción de la colección.</span><span class="sxs-lookup"><span data-stu-id="a0889-156">Gets or sets the description of the collection</span></span>

</dd> <dt>

<span data-ttu-id="a0889-157">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="a0889-157">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-158">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="a0889-158">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a0889-159">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a0889-160">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0889-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0889-161">Obtiene o establece una matriz de valores que especifican los iconos de la colección.</span><span class="sxs-lookup"><span data-stu-id="a0889-161">Gets or sets an array of values that specify icons for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="a0889-162">**IsHA**</span><span class="sxs-lookup"><span data-stu-id="a0889-162">**IsHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-163">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a0889-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-164">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a0889-165">Obtiene o establece un valor que indica si la colección contiene máquinas virtuales de alta disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="a0889-165">Gets or sets a values that indicates whether the collection contains highly available VMs.</span></span> <span data-ttu-id="a0889-166">**True** si la colección contiene máquinas virtuales de alta disponibilidad; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a0889-166">**TRUE** if the collection contains highly available VMs; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a0889-167">**IsManaged (**</span><span class="sxs-lookup"><span data-stu-id="a0889-167">**IsManaged**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-168">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a0889-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a0889-170">Obtiene o establece un valor que indica si la colección está administrada.</span><span class="sxs-lookup"><span data-stu-id="a0889-170">Gets or sets a value that indicates whether the collection is managed.</span></span> <span data-ttu-id="a0889-171">**True** si la colección es administrada; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a0889-171">**TRUE** if the collection is managed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a0889-172">**IsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="a0889-172">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-173">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a0889-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-174">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a0889-175">Obtiene o establece un valor que indica si un usuario es un administrador en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0889-175">Gets or sets a values that indicates whether a user is an administrator on a VM.</span></span> <span data-ttu-id="a0889-176">**True** si el usuario es un administrador de una máquina virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a0889-176">**TRUE** if the user is an administrator on a VM; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a0889-177">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a0889-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0889-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-179">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a0889-180">Obtiene o establece el nombre de la colección.</span><span class="sxs-lookup"><span data-stu-id="a0889-180">Gets or sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="a0889-181">**RollbackEnabled**</span><span class="sxs-lookup"><span data-stu-id="a0889-181">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-182">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a0889-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-183">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a0889-184">Obtiene o establece un valor que indica si una máquina virtual se ha distribuido con una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0889-184">Gets or sets a values that indicates whether a VM was rolled with a VM snapshot.</span></span> <span data-ttu-id="a0889-185">**True** si la máquina virtual se ha distribuido con una instantánea de máquina virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a0889-185">**TRUE** if the VM was rolled with a VM snapshot; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a0889-186">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a0889-186">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0889-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-188">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a0889-189">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0889-189">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0889-190">Obtiene o establece un descriptor de seguridad con formato SSDL que controla el acceso a la colección.</span><span class="sxs-lookup"><span data-stu-id="a0889-190">Gets or sets an SSDL formated security descriptor that controls access to the collection.</span></span>

</dd> <dt>

<span data-ttu-id="a0889-191">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="a0889-191">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-192">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a0889-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-193">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-193">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a0889-194">Obtiene o establece un valor que indica si la colección se muestra en Terminal Services acceso web (acceso web de TS).</span><span class="sxs-lookup"><span data-stu-id="a0889-194">Gets or sets a values that indicates whether the collection is displayed in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="a0889-195">**True** para mostrar la colección en acceso web de TS; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a0889-195">**TRUE** to display the collection in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a0889-196">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a0889-196">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-197">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0889-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-198">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a0889-199">Obtiene o establece un valor que indica el tipo de sesiones de máquina virtual hospedadas por la colección.</span><span class="sxs-lookup"><span data-stu-id="a0889-199">Gets or sets a value that indicates the type of virtual machine sessions hosted by the collection.</span></span>

<span data-ttu-id="a0889-200">Esta propiedad contiene uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="a0889-200">This property contains one of the following values:</span></span>

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="a0889-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)</span><span class="sxs-lookup"><span data-stu-id="a0889-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a0889-202">Máquinas virtuales temporales.</span><span class="sxs-lookup"><span data-stu-id="a0889-202">Temporary virtual machines.</span></span>

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="a0889-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)</span><span class="sxs-lookup"><span data-stu-id="a0889-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a0889-204">Máquinas virtuales creadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="a0889-204">Manually created virtual machines.</span></span>

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="a0889-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)</span><span class="sxs-lookup"><span data-stu-id="a0889-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a0889-206">Máquinas virtuales generadas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a0889-206">Auto-generated virtual machines.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0889-207">**UserVHDSetting**</span><span class="sxs-lookup"><span data-stu-id="a0889-207">**UserVHDSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0889-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-209">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a0889-210">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0889-210">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0889-211">Obtiene o establece la configuración de VHD de datos de usuario para la colección.</span><span class="sxs-lookup"><span data-stu-id="a0889-211">Gets or sets the user data VHD setting for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="a0889-212">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="a0889-212">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0889-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0889-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0889-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0889-214">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a0889-215">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0889-215">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0889-216">Obtiene o establece la configuración de escritorio de las máquinas virtuales de la colección.</span><span class="sxs-lookup"><span data-stu-id="a0889-216">Gets or sets he desktop settings for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0889-217">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0889-217">Requirements</span></span>



| <span data-ttu-id="a0889-218">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0889-218">Requirement</span></span> | <span data-ttu-id="a0889-219">Value</span><span class="sxs-lookup"><span data-stu-id="a0889-219">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0889-220">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0889-220">Minimum supported client</span></span><br/> | <span data-ttu-id="a0889-221">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a0889-221">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a0889-222">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0889-222">Minimum supported server</span></span><br/> | <span data-ttu-id="a0889-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0889-223">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a0889-224">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a0889-224">Namespace</span></span><br/>                | <span data-ttu-id="a0889-225">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="a0889-225">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a0889-226">MOF</span><span class="sxs-lookup"><span data-stu-id="a0889-226">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0889-227"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0889-227"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0889-228">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a0889-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0889-229"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0889-229"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a0889-230">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0889-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0889-231">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a0889-231">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

