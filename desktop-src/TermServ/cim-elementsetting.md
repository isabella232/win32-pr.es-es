---
title: CIM_ElementSetting (clase) (Servicios de Escritorio remoto)
description: Representa la asociación entre los elementos del sistema administrados y la clase de configuración definida para ellos.
ms.assetid: b74c2fef-0f3a-46b9-9dd8-11016a8f7b57
ms.tgt_platform: multiple
keywords:
- CIM_ElementSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de CIM_ElementSetting de clase, se describe
topic_type:
- apiref
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Caption
- CIM_ElementSetting.Description
- CIM_ElementSetting.InstallDate
- CIM_ElementSetting.Name
- CIM_ElementSetting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aff40961ddc8fa07de6c49d6c95aefe3d005d6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150005"
---
# <a name="cim_elementsetting-class-remote-desktop-services"></a><span data-ttu-id="32eb4-105">CIM_ElementSetting (clase) (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="32eb4-105">CIM_ElementSetting class (Remote Desktop Services)</span></span>

<span data-ttu-id="32eb4-106">Representa la asociación entre los elementos del sistema administrados y la clase de configuración definida para ellos.</span><span class="sxs-lookup"><span data-stu-id="32eb4-106">Represents the association between managed system elements and the setting class defined for them.</span></span>

<span data-ttu-id="32eb4-107">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="32eb4-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="32eb4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32eb4-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="32eb4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="32eb4-109">Members</span></span>

<span data-ttu-id="32eb4-110">La clase **CIM \_ ElementSetting** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="32eb4-110">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="32eb4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32eb4-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32eb4-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32eb4-112">Properties</span></span>

<span data-ttu-id="32eb4-113">La clase **CIM \_ ElementSetting** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="32eb4-113">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32eb4-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="32eb4-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32eb4-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32eb4-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32eb4-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32eb4-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32eb4-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="32eb4-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="32eb4-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="32eb4-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="32eb4-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32eb4-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32eb4-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="32eb4-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32eb4-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32eb4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32eb4-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32eb4-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32eb4-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="32eb4-123">Description of the object.</span></span>

<span data-ttu-id="32eb4-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32eb4-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32eb4-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="32eb4-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32eb4-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="32eb4-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="32eb4-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32eb4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32eb4-128">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="32eb4-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="32eb4-129">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="32eb4-129">The date the object was installed.</span></span> <span data-ttu-id="32eb4-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="32eb4-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="32eb4-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32eb4-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32eb4-132">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="32eb4-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32eb4-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32eb4-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32eb4-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32eb4-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32eb4-135">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="32eb4-135">The name of the object.</span></span>

<span data-ttu-id="32eb4-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32eb4-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32eb4-137">**Estado**</span><span class="sxs-lookup"><span data-stu-id="32eb4-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32eb4-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32eb4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32eb4-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32eb4-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32eb4-140">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="32eb4-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="32eb4-141">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="32eb4-141">Current status of the object.</span></span> <span data-ttu-id="32eb4-142">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="32eb4-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="32eb4-143">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="32eb4-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="32eb4-144">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="32eb4-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="32eb4-145">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="32eb4-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="32eb4-146">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="32eb4-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="32eb4-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32eb4-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="32eb4-148">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="32eb4-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32eb4-149">("Error")</span><span class="sxs-lookup"><span data-stu-id="32eb4-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32eb4-150">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="32eb4-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32eb4-151">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="32eb4-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32eb4-152">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="32eb4-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32eb4-153">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="32eb4-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32eb4-154">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="32eb4-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32eb4-155">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="32eb4-155">("Service")</span></span>


<span data-ttu-id="32eb4-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="32eb4-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="32eb4-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32eb4-157">Requirements</span></span>



| <span data-ttu-id="32eb4-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="32eb4-158">Requirement</span></span> | <span data-ttu-id="32eb4-159">Value</span><span class="sxs-lookup"><span data-stu-id="32eb4-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32eb4-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32eb4-160">Minimum supported client</span></span><br/> | <span data-ttu-id="32eb4-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32eb4-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32eb4-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32eb4-162">Minimum supported server</span></span><br/> | <span data-ttu-id="32eb4-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32eb4-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32eb4-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32eb4-164">Namespace</span></span><br/>                | <span data-ttu-id="32eb4-165">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="32eb4-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="32eb4-166">MOF</span><span class="sxs-lookup"><span data-stu-id="32eb4-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32eb4-167"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32eb4-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="32eb4-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32eb4-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32eb4-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32eb4-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32eb4-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="32eb4-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32eb4-171">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="32eb4-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

