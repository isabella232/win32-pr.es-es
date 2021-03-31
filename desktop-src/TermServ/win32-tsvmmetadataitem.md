---
title: Win32_TSVmMetadataItem (clase)
description: Representa un elemento de metadatos para una máquina virtual Escritorio remoto.
ms.assetid: d2678eb0-8634-450c-b73f-611b6f68d556
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataItem clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSVmMetadataItem de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataItem
- Win32_TSVmMetadataItem.Caption
- Win32_TSVmMetadataItem.Description
- Win32_TSVmMetadataItem.InstallDate
- Win32_TSVmMetadataItem.Name
- Win32_TSVmMetadataItem.Status
- Win32_TSVmMetadataItem.VmName
- Win32_TSVmMetadataItem.SectionId
- Win32_TSVmMetadataItem.Value
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872cec5bf3ff0e7b45ab07cb41b6227bcfb8636d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995989"
---
# <a name="win32_tsvmmetadataitem-class"></a><span data-ttu-id="00508-105">\_Clase Win32 TSVmMetadataItem</span><span class="sxs-lookup"><span data-stu-id="00508-105">Win32\_TSVmMetadataItem class</span></span>

<span data-ttu-id="00508-106">Representa un elemento de metadatos para una máquina virtual Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="00508-106">Represents a metadata item for a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="00508-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="00508-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00508-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00508-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  sint32   SectionId;
  string   Value;
};
```

## <a name="members"></a><span data-ttu-id="00508-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="00508-109">Members</span></span>

<span data-ttu-id="00508-110">La **clase \_ TSVmMetadataItem de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="00508-110">The **Win32\_TSVmMetadataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="00508-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00508-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00508-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00508-112">Properties</span></span>

<span data-ttu-id="00508-113">La **clase \_ TSVmMetadataItem de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="00508-113">The **Win32\_TSVmMetadataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00508-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="00508-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00508-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="00508-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00508-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00508-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00508-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="00508-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="00508-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="00508-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="00508-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="00508-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="00508-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00508-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00508-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="00508-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00508-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00508-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00508-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="00508-123">Description of the object.</span></span>

<span data-ttu-id="00508-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="00508-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="00508-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="00508-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00508-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="00508-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="00508-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00508-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00508-128">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="00508-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="00508-129">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="00508-129">The date the object was installed.</span></span> <span data-ttu-id="00508-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="00508-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="00508-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="00508-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="00508-132">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="00508-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00508-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="00508-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00508-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00508-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00508-135">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="00508-135">The name of the object.</span></span>

<span data-ttu-id="00508-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="00508-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="00508-137">**SectionId**</span><span class="sxs-lookup"><span data-stu-id="00508-137">**SectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00508-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="00508-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="00508-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00508-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00508-140">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="00508-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="00508-141">Especifica la sección dentro de los metadatos donde reside este elemento.</span><span class="sxs-lookup"><span data-stu-id="00508-141">Specifies the section within the metadata where this item resides.</span></span>

<dt>

<span data-ttu-id="00508-142">0</span><span class="sxs-lookup"><span data-stu-id="00508-142">0</span></span>
</dt> <dd>

<span data-ttu-id="00508-143">Sección de configuración.</span><span class="sxs-lookup"><span data-stu-id="00508-143">Configuration section.</span></span>

</dd> <dt>

<span data-ttu-id="00508-144">1</span><span class="sxs-lookup"><span data-stu-id="00508-144">1</span></span>
</dt> <dd>

<span data-ttu-id="00508-145">Sección de configuración de la habilitación.</span><span class="sxs-lookup"><span data-stu-id="00508-145">Enlightenment settings section.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="00508-146">**Estado**</span><span class="sxs-lookup"><span data-stu-id="00508-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00508-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="00508-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00508-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00508-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00508-149">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="00508-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="00508-150">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="00508-150">Current status of the object.</span></span> <span data-ttu-id="00508-151">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="00508-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="00508-152">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="00508-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="00508-153">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="00508-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="00508-154">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="00508-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="00508-155">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="00508-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="00508-156">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="00508-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="00508-157">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="00508-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="00508-158">("Error")</span><span class="sxs-lookup"><span data-stu-id="00508-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="00508-159">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="00508-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="00508-160">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="00508-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="00508-161">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="00508-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="00508-162">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="00508-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="00508-163">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="00508-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="00508-164">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="00508-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="00508-165">**Valor**</span><span class="sxs-lookup"><span data-stu-id="00508-165">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00508-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="00508-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00508-167">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="00508-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="00508-168">Valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="00508-168">The value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="00508-169">**VmName**</span><span class="sxs-lookup"><span data-stu-id="00508-169">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00508-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="00508-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00508-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00508-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00508-172">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="00508-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="00508-173">El nombre de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="00508-173">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00508-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00508-174">Requirements</span></span>



| <span data-ttu-id="00508-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="00508-175">Requirement</span></span> | <span data-ttu-id="00508-176">Value</span><span class="sxs-lookup"><span data-stu-id="00508-176">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="00508-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00508-177">Minimum supported client</span></span><br/> | <span data-ttu-id="00508-178">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="00508-178">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="00508-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00508-179">Minimum supported server</span></span><br/> | <span data-ttu-id="00508-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="00508-180">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="00508-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="00508-181">Namespace</span></span><br/>                | <span data-ttu-id="00508-182">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="00508-182">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="00508-183">MOF</span><span class="sxs-lookup"><span data-stu-id="00508-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00508-184"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00508-184"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="00508-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="00508-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00508-186"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00508-186"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

