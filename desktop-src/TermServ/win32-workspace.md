---
title: Win32_Workspace (clase)
description: Especifica Servicios de Escritorio remoto información de configuración del área de trabajo.
ms.assetid: 27192dca-cbb4-4620-ae52-c27aba4b4dff
ms.tgt_platform: multiple
keywords:
- Win32_Workspace clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_Workspace de clase, se describe
topic_type:
- apiref
api_name:
- Win32_Workspace
- Win32_Workspace.Caption
- Win32_Workspace.Description
- Win32_Workspace.InstallDate
- Win32_Workspace.Name
- Win32_Workspace.Status
- Win32_Workspace.IsDefaultName
- Win32_Workspace.ID
- Win32_Workspace.Redirector
- Win32_Workspace.RedirectorAlternateAddress
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1153a4eb8a260e539845a9458a5c8cee4581d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676573"
---
# <a name="win32_workspace-class"></a><span data-ttu-id="0119e-105">\_Clase de área de trabajo Win32</span><span class="sxs-lookup"><span data-stu-id="0119e-105">Win32\_Workspace class</span></span>

<span data-ttu-id="0119e-106">Especifica Servicios de Escritorio remoto información de configuración del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="0119e-106">Specifies Remote Desktop Services workspace configuration information.</span></span>

<span data-ttu-id="0119e-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0119e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0119e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0119e-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov"), singleton]
class Win32_Workspace : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  IsDefaultName;
  string   ID;
  string   Redirector;
  string   RedirectorAlternateAddress;
};
```

## <a name="members"></a><span data-ttu-id="0119e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0119e-109">Members</span></span>

<span data-ttu-id="0119e-110">La clase del **\_ área de trabajo Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0119e-110">The **Win32\_Workspace** class has these types of members:</span></span>

-   [<span data-ttu-id="0119e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0119e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0119e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0119e-112">Properties</span></span>

<span data-ttu-id="0119e-113">La clase del **\_ área de trabajo Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0119e-113">The **Win32\_Workspace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0119e-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0119e-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0119e-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0119e-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0119e-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0119e-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0119e-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0119e-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0119e-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="0119e-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0119e-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0119e-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0119e-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0119e-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0119e-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0119e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0119e-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0119e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0119e-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="0119e-123">Description of the object.</span></span>

<span data-ttu-id="0119e-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0119e-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0119e-125">**Id**</span><span class="sxs-lookup"><span data-stu-id="0119e-125">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0119e-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0119e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0119e-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0119e-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0119e-128">Identificador del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="0119e-128">The identifier of the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="0119e-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0119e-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0119e-130">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0119e-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0119e-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0119e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0119e-132">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="0119e-132">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0119e-133">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="0119e-133">The date the object was installed.</span></span> <span data-ttu-id="0119e-134">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="0119e-134">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0119e-135">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0119e-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0119e-136">**IsDefaultName**</span><span class="sxs-lookup"><span data-stu-id="0119e-136">**IsDefaultName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0119e-137">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0119e-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0119e-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0119e-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0119e-139">Especifica si el nombre del área de trabajo es el nombre predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0119e-139">Specifies if the workspace name is the default name.</span></span> <span data-ttu-id="0119e-140">Contiene un valor distinto de cero si el nombre es un nombre predeterminado o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="0119e-140">Contains nonzero if the name is a default name or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="0119e-141">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0119e-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0119e-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0119e-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0119e-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0119e-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0119e-144">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="0119e-144">The name of the object.</span></span>

<span data-ttu-id="0119e-145">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0119e-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0119e-146">**Redirector**</span><span class="sxs-lookup"><span data-stu-id="0119e-146">**Redirector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0119e-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0119e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0119e-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0119e-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0119e-149">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0119e-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0119e-150">Nombre del equipo del redirector del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="0119e-150">The machine name of the redirector for the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="0119e-151">**RedirectorAlternateAddress**</span><span class="sxs-lookup"><span data-stu-id="0119e-151">**RedirectorAlternateAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0119e-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0119e-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0119e-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0119e-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0119e-154">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0119e-154">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0119e-155">Dirección alternativa del redirector.</span><span class="sxs-lookup"><span data-stu-id="0119e-155">The alternate address for the redirector.</span></span>

</dd> <dt>

<span data-ttu-id="0119e-156">**Estado**</span><span class="sxs-lookup"><span data-stu-id="0119e-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0119e-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0119e-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0119e-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0119e-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0119e-159">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0119e-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0119e-160">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="0119e-160">Current status of the object.</span></span> <span data-ttu-id="0119e-161">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="0119e-161">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0119e-162">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="0119e-162">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0119e-163">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="0119e-163">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0119e-164">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="0119e-164">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0119e-165">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="0119e-165">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0119e-166">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0119e-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0119e-167">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="0119e-167">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0119e-168">("Error")</span><span class="sxs-lookup"><span data-stu-id="0119e-168">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0119e-169">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="0119e-169">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0119e-170">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="0119e-170">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0119e-171">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="0119e-171">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0119e-172">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="0119e-172">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0119e-173">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="0119e-173">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0119e-174">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="0119e-174">("Service")</span></span>


<span data-ttu-id="0119e-175"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0119e-175"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0119e-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0119e-176">Requirements</span></span>



| <span data-ttu-id="0119e-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="0119e-177">Requirement</span></span> | <span data-ttu-id="0119e-178">Value</span><span class="sxs-lookup"><span data-stu-id="0119e-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0119e-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0119e-179">Minimum supported client</span></span><br/> | <span data-ttu-id="0119e-180">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0119e-180">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0119e-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0119e-181">Minimum supported server</span></span><br/> | <span data-ttu-id="0119e-182">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0119e-182">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="0119e-183">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0119e-183">Namespace</span></span><br/>                | <span data-ttu-id="0119e-184">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0119e-184">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0119e-185">MOF</span><span class="sxs-lookup"><span data-stu-id="0119e-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0119e-186"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0119e-186"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="0119e-187">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0119e-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0119e-188"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0119e-188"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

