---
title: Win32_TSGetIcon (clase)
description: Devuelve el contenido del icono especificado por la ruta de acceso y el índice del archivo.
ms.assetid: c0ab50f1-f5a9-4f5e-8280-40c638f09e1c
ms.tgt_platform: multiple
keywords:
- Win32_TSGetIcon clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGetIcon de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGetIcon
- Win32_TSGetIcon.Caption
- Win32_TSGetIcon.Description
- Win32_TSGetIcon.InstallDate
- Win32_TSGetIcon.Name
- Win32_TSGetIcon.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0186e158f025be8e8a5e6cf3e87f3ad5d8b296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996490"
---
# <a name="win32_tsgeticon-class"></a><span data-ttu-id="2057d-105">\_Clase Win32 TSGetIcon</span><span class="sxs-lookup"><span data-stu-id="2057d-105">Win32\_TSGetIcon class</span></span>

<span data-ttu-id="2057d-106">Devuelve el contenido del icono especificado por la ruta de acceso y el índice del archivo.</span><span class="sxs-lookup"><span data-stu-id="2057d-106">Returns the contents of the icon specified by file path and index</span></span>

<span data-ttu-id="2057d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2057d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2057d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2057d-108">Syntax</span></span>

``` syntax
class Win32_TSGetIcon : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="2057d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2057d-109">Members</span></span>

<span data-ttu-id="2057d-110">La **clase \_ TSGetIcon de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2057d-110">The **Win32\_TSGetIcon** class has these types of members:</span></span>

-   [<span data-ttu-id="2057d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2057d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="2057d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2057d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2057d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2057d-113">Methods</span></span>

<span data-ttu-id="2057d-114">La clase **Win32 \_ TSGetIcon** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2057d-114">The **Win32\_TSGetIcon** class has these methods.</span></span>



| <span data-ttu-id="2057d-115">Método</span><span class="sxs-lookup"><span data-stu-id="2057d-115">Method</span></span>                                     | <span data-ttu-id="2057d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2057d-116">Description</span></span>                                            |
|:-------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="2057d-117">**GetIcon**</span><span class="sxs-lookup"><span data-stu-id="2057d-117">**GetIcon**</span></span>](geticon-win32-tsgeticon.md) | <span data-ttu-id="2057d-118">Devuelve el contenido del icono especificado.</span><span class="sxs-lookup"><span data-stu-id="2057d-118">Returns the contents of the specified icon.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2057d-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2057d-119">Properties</span></span>

<span data-ttu-id="2057d-120">La **clase \_ TSGetIcon de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2057d-120">The **Win32\_TSGetIcon** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2057d-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2057d-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2057d-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2057d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2057d-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2057d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2057d-124">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2057d-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2057d-125">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="2057d-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="2057d-126">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2057d-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2057d-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2057d-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2057d-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2057d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2057d-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2057d-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2057d-130">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2057d-130">Description of the object.</span></span>

<span data-ttu-id="2057d-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2057d-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2057d-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2057d-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2057d-133">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2057d-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2057d-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2057d-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2057d-135">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="2057d-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="2057d-136">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="2057d-136">The date the object was installed.</span></span> <span data-ttu-id="2057d-137">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="2057d-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2057d-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2057d-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2057d-139">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2057d-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2057d-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2057d-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2057d-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2057d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2057d-142">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="2057d-142">The name of the object.</span></span>

<span data-ttu-id="2057d-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2057d-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2057d-144">**Estado**</span><span class="sxs-lookup"><span data-stu-id="2057d-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2057d-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2057d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2057d-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2057d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2057d-147">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="2057d-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="2057d-148">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2057d-148">Current status of the object.</span></span> <span data-ttu-id="2057d-149">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="2057d-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2057d-150">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="2057d-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2057d-151">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="2057d-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2057d-152">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="2057d-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2057d-153">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="2057d-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2057d-154">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2057d-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="2057d-155">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="2057d-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2057d-156">("Error")</span><span class="sxs-lookup"><span data-stu-id="2057d-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2057d-157">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="2057d-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2057d-158">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="2057d-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2057d-159">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="2057d-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2057d-160">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="2057d-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2057d-161">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="2057d-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2057d-162">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="2057d-162">("Service")</span></span>


<span data-ttu-id="2057d-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2057d-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2057d-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2057d-164">Requirements</span></span>



| <span data-ttu-id="2057d-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="2057d-165">Requirement</span></span> | <span data-ttu-id="2057d-166">Value</span><span class="sxs-lookup"><span data-stu-id="2057d-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2057d-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2057d-167">Minimum supported client</span></span><br/> | <span data-ttu-id="2057d-168">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2057d-168">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2057d-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2057d-169">Minimum supported server</span></span><br/> | <span data-ttu-id="2057d-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2057d-170">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="2057d-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2057d-171">Namespace</span></span><br/>                | <span data-ttu-id="2057d-172">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2057d-172">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2057d-173">MOF</span><span class="sxs-lookup"><span data-stu-id="2057d-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2057d-174"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2057d-174"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="2057d-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2057d-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2057d-176"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2057d-176"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

