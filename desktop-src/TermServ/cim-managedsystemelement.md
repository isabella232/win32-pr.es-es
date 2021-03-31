---
title: CIM_ManagedSystemElement (clase) (Servicios de Escritorio remoto)
description: La clase base para la jerarquía de elementos del sistema.
ms.assetid: c71c0441-381f-4a46-864c-9206c43a27d0
ms.tgt_platform: multiple
keywords:
- CIM_ManagedSystemElement clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de CIM_ManagedSystemElement de clase, se describe
topic_type:
- apiref
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b242369df24724fdcc31ce925a229dba5bb515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150004"
---
# <a name="cim_managedsystemelement-class-remote-desktop-services"></a><span data-ttu-id="b18ec-105">CIM_ManagedSystemElement (clase) (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="b18ec-105">CIM_ManagedSystemElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="b18ec-106">La clase base para la jerarquía de elementos del sistema.</span><span class="sxs-lookup"><span data-stu-id="b18ec-106">The base class for the system element hierarchy.</span></span>

<span data-ttu-id="b18ec-107">Cualquier componente del sistema distinguible es un candidato para la inclusión en esta clase.</span><span class="sxs-lookup"><span data-stu-id="b18ec-107">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="b18ec-108">Algunos ejemplos son componentes de software, como archivos; dispositivos, como unidades de disco y controladores; y componentes físicos, como chips y tarjetas</span><span class="sxs-lookup"><span data-stu-id="b18ec-108">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards</span></span>

<span data-ttu-id="b18ec-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b18ec-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b18ec-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b18ec-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="b18ec-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b18ec-111">Members</span></span>

<span data-ttu-id="b18ec-112">La clase del **\_ ManagedSystemElement de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b18ec-112">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="b18ec-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b18ec-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b18ec-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b18ec-114">Properties</span></span>

<span data-ttu-id="b18ec-115">La clase del **\_ ManagedSystemElement de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b18ec-115">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b18ec-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b18ec-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b18ec-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b18ec-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b18ec-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b18ec-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b18ec-119">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b18ec-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b18ec-120">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="b18ec-120">Short description (one-line string) of the object.</span></span>

</dd> <dt>

<span data-ttu-id="b18ec-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b18ec-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b18ec-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b18ec-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b18ec-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b18ec-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b18ec-124">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b18ec-124">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="b18ec-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b18ec-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b18ec-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b18ec-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b18ec-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b18ec-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b18ec-128">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="b18ec-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="b18ec-129">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b18ec-129">The date the object was installed.</span></span> <span data-ttu-id="b18ec-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="b18ec-130">A lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="b18ec-131">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b18ec-131">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b18ec-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b18ec-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b18ec-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b18ec-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b18ec-134">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="b18ec-134">The name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="b18ec-135">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b18ec-135">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b18ec-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b18ec-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b18ec-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b18ec-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b18ec-138">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="b18ec-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="b18ec-139">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b18ec-139">Current status of the object.</span></span> <span data-ttu-id="b18ec-140">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="b18ec-140">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b18ec-141">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="b18ec-141">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b18ec-142">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="b18ec-142">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b18ec-143">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="b18ec-143">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b18ec-144">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b18ec-144">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<dt>



 <span data-ttu-id="b18ec-145">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="b18ec-145">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b18ec-146">("Error")</span><span class="sxs-lookup"><span data-stu-id="b18ec-146">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b18ec-147">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="b18ec-147">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b18ec-148">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="b18ec-148">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b18ec-149">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b18ec-149">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b18ec-150">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="b18ec-150">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b18ec-151">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="b18ec-151">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b18ec-152">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="b18ec-152">("Service")</span></span>


<span data-ttu-id="b18ec-153"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b18ec-153"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b18ec-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b18ec-154">Requirements</span></span>



| <span data-ttu-id="b18ec-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="b18ec-155">Requirement</span></span> | <span data-ttu-id="b18ec-156">Value</span><span class="sxs-lookup"><span data-stu-id="b18ec-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b18ec-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b18ec-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b18ec-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b18ec-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b18ec-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b18ec-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b18ec-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b18ec-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b18ec-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b18ec-161">Namespace</span></span><br/>                | <span data-ttu-id="b18ec-162">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b18ec-162">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b18ec-163">MOF</span><span class="sxs-lookup"><span data-stu-id="b18ec-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b18ec-164"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b18ec-164"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b18ec-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b18ec-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b18ec-166"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b18ec-166"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

