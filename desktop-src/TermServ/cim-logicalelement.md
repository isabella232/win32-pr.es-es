---
title: CIM_LogicalElement (clase) (Servicios de Escritorio remoto)
description: La clase base para todos los componentes del sistema que representan componentes del sistema abstractos, como perfiles, procesos o capacidades del sistema, en forma de dispositivos lógicos.
ms.assetid: 21e4a2ba-7bc5-4e33-a888-198299137da6
ms.tgt_platform: multiple
keywords:
- CIM_LogicalElement clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de CIM_LogicalElement de clase, se describe
topic_type:
- apiref
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f7e58fe64f3b9dbb76a11d308aadbe6ce50331f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422027"
---
# <a name="cim_logicalelement-class-remote-desktop-services"></a><span data-ttu-id="1e84c-105">CIM_LogicalElement (clase) (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="1e84c-105">CIM_LogicalElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="1e84c-106">La clase base para todos los componentes del sistema que representan componentes del sistema abstractos, como perfiles, procesos o capacidades del sistema, en forma de dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="1e84c-106">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

<span data-ttu-id="1e84c-107">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1e84c-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e84c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e84c-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="1e84c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e84c-109">Members</span></span>

<span data-ttu-id="1e84c-110">La clase **CIM \_ LogicalElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1e84c-110">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="1e84c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e84c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e84c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e84c-112">Properties</span></span>

<span data-ttu-id="1e84c-113">La clase **CIM \_ LogicalElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1e84c-113">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e84c-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1e84c-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e84c-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e84c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e84c-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e84c-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e84c-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1e84c-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1e84c-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="1e84c-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="1e84c-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e84c-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e84c-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1e84c-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e84c-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e84c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e84c-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e84c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e84c-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="1e84c-123">Description of the object.</span></span>

<span data-ttu-id="1e84c-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e84c-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e84c-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1e84c-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e84c-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1e84c-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1e84c-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e84c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e84c-128">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="1e84c-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="1e84c-129">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="1e84c-129">The date the object was installed.</span></span> <span data-ttu-id="1e84c-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="1e84c-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1e84c-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e84c-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e84c-132">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1e84c-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e84c-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e84c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e84c-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e84c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e84c-135">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="1e84c-135">The name of the object.</span></span>

<span data-ttu-id="1e84c-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e84c-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e84c-137">**Estado**</span><span class="sxs-lookup"><span data-stu-id="1e84c-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e84c-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e84c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e84c-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e84c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e84c-140">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="1e84c-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="1e84c-141">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1e84c-141">Current status of the object.</span></span> <span data-ttu-id="1e84c-142">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="1e84c-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1e84c-143">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="1e84c-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1e84c-144">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="1e84c-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1e84c-145">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="1e84c-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1e84c-146">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="1e84c-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1e84c-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e84c-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="1e84c-148">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="1e84c-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e84c-149">("Error")</span><span class="sxs-lookup"><span data-stu-id="1e84c-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e84c-150">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="1e84c-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e84c-151">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="1e84c-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e84c-152">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="1e84c-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e84c-153">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="1e84c-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e84c-154">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="1e84c-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1e84c-155">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="1e84c-155">("Service")</span></span>


<span data-ttu-id="1e84c-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1e84c-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1e84c-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e84c-157">Requirements</span></span>



| <span data-ttu-id="1e84c-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e84c-158">Requirement</span></span> | <span data-ttu-id="1e84c-159">Value</span><span class="sxs-lookup"><span data-stu-id="1e84c-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e84c-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e84c-160">Minimum supported client</span></span><br/> | <span data-ttu-id="1e84c-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e84c-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e84c-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e84c-162">Minimum supported server</span></span><br/> | <span data-ttu-id="1e84c-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e84c-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e84c-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1e84c-164">Namespace</span></span><br/>                | <span data-ttu-id="1e84c-165">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1e84c-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1e84c-166">MOF</span><span class="sxs-lookup"><span data-stu-id="1e84c-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e84c-167"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e84c-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e84c-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e84c-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e84c-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e84c-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e84c-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e84c-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e84c-171">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="1e84c-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

