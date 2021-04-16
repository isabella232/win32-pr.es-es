---
title: CIM_Setting (clase) (Servicios de Escritorio remoto)
description: Representa los parámetros operativos y relacionados con la configuración de uno o más elementos del sistema administrados.
ms.assetid: d0007762-5d13-421b-a73a-3392a77686a6
ms.tgt_platform: multiple
keywords:
- CIM_Setting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de CIM_Setting de clase, se describe
topic_type:
- apiref
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.InstallDate
- CIM_Setting.Name
- CIM_Setting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d3a9517df9af92f428000ed064b2bb88b348a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676616"
---
# <a name="cim_setting-class-remote-desktop-services"></a><span data-ttu-id="cd6cc-105">CIM_Setting (clase) (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="cd6cc-105">CIM_Setting class (Remote Desktop Services)</span></span>

<span data-ttu-id="cd6cc-106">Representa los parámetros operativos y relacionados con la configuración de uno o más elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-106">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

<span data-ttu-id="cd6cc-107">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd6cc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd6cc-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="cd6cc-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd6cc-109">Members</span></span>

<span data-ttu-id="cd6cc-110">La clase de **\_ configuración CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cd6cc-110">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="cd6cc-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd6cc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd6cc-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd6cc-112">Properties</span></span>

<span data-ttu-id="cd6cc-113">La clase de **\_ configuración CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-113">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd6cc-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="cd6cc-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6cc-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cd6cc-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6cc-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd6cc-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6cc-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="cd6cc-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cd6cc-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="cd6cc-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd6cc-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd6cc-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd6cc-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6cc-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cd6cc-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6cc-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd6cc-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd6cc-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-123">Description of the object.</span></span>

<span data-ttu-id="cd6cc-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd6cc-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd6cc-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cd6cc-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6cc-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd6cc-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd6cc-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd6cc-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6cc-128">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="cd6cc-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="cd6cc-129">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-129">The date the object was installed.</span></span> <span data-ttu-id="cd6cc-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="cd6cc-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd6cc-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd6cc-132">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="cd6cc-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6cc-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cd6cc-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6cc-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd6cc-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd6cc-135">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-135">The name of the object.</span></span>

<span data-ttu-id="cd6cc-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd6cc-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd6cc-137">**Estado**</span><span class="sxs-lookup"><span data-stu-id="cd6cc-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd6cc-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cd6cc-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd6cc-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd6cc-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd6cc-140">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="cd6cc-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="cd6cc-141">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-141">Current status of the object.</span></span> <span data-ttu-id="cd6cc-142">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="cd6cc-143">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="cd6cc-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="cd6cc-144">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="cd6cc-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cd6cc-145">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cd6cc-146">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="cd6cc-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cd6cc-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd6cc-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="cd6cc-148">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="cd6cc-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd6cc-149">("Error")</span><span class="sxs-lookup"><span data-stu-id="cd6cc-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd6cc-150">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="cd6cc-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd6cc-151">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="cd6cc-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd6cc-152">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="cd6cc-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd6cc-153">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="cd6cc-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd6cc-154">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="cd6cc-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="cd6cc-155">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="cd6cc-155">("Service")</span></span>


<span data-ttu-id="cd6cc-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cd6cc-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="cd6cc-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd6cc-157">Requirements</span></span>



| <span data-ttu-id="cd6cc-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd6cc-158">Requirement</span></span> | <span data-ttu-id="cd6cc-159">Value</span><span class="sxs-lookup"><span data-stu-id="cd6cc-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6cc-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd6cc-160">Minimum supported client</span></span><br/> | <span data-ttu-id="cd6cc-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd6cc-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd6cc-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd6cc-162">Minimum supported server</span></span><br/> | <span data-ttu-id="cd6cc-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd6cc-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd6cc-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cd6cc-164">Namespace</span></span><br/>                | <span data-ttu-id="cd6cc-165">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cd6cc-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cd6cc-166">MOF</span><span class="sxs-lookup"><span data-stu-id="cd6cc-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd6cc-167"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd6cc-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd6cc-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd6cc-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd6cc-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd6cc-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd6cc-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd6cc-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd6cc-171">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="cd6cc-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

