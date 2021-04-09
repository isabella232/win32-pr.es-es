---
description: La \_ clase CIM ProcessExecutable representa un vínculo entre un proceso y un archivo de datos e indica que el archivo participa en la ejecución del proceso.
ms.assetid: 6db69bf3-b28e-4d0b-8878-558e12052767
ms.tgt_platform: multiple
title: CIM_ProcessExecutable (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessExecutable
- CIM_ProcessExecutable.Dependent
- CIM_ProcessExecutable.Antecedent
- CIM_ProcessExecutable.BaseAddress
- CIM_ProcessExecutable.GlobalProcessCount
- CIM_ProcessExecutable.ModuleInstance
- CIM_ProcessExecutable.ProcessCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aedb1e79ad842e4cb04746ff47bfab142a536f43
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080288"
---
# <a name="cim_processexecutable-class"></a><span data-ttu-id="4c4f4-103">\_Clase ProcessExecutable de CIM</span><span class="sxs-lookup"><span data-stu-id="4c4f4-103">CIM\_ProcessExecutable class</span></span>

<span data-ttu-id="4c4f4-104">La clase **CIM \_ ProcessExecutable** representa un vínculo entre un proceso y un archivo de datos e indica que el archivo participa en la ejecución del proceso.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-104">The **CIM\_ProcessExecutable** class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c4f4-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4c4f4-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4c4f4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4c4f4-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4c4f4-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c4f4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c4f4-109">Syntax</span></span>

``` syntax
[Privileges("SeDebugPrivilege"), Dynamic, Provider("CIMWin32"), UUID("{8502C542-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ProcessExecutable : CIM_Dependency
{
  CIM_Process  REF Dependent;
  CIM_DataFile REF Antecedent;
  uint64           BaseAddress;
  uint32           GlobalProcessCount;
  uint32           ModuleInstance;
  uint32           ProcessCount;
};
```

## <a name="members"></a><span data-ttu-id="4c4f4-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="4c4f4-110">Members</span></span>

<span data-ttu-id="4c4f4-111">La clase **CIM \_ ProcessExecutable** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4c4f4-111">The **CIM\_ProcessExecutable** class has these types of members:</span></span>

-   [<span data-ttu-id="4c4f4-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c4f4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c4f4-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c4f4-113">Properties</span></span>

<span data-ttu-id="4c4f4-114">La clase **CIM \_ ProcessExecutable** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-114">The **CIM\_ProcessExecutable** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c4f4-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4f4-116">Tipo de datos **: \_ archivo** de datos CIM</span><span class="sxs-lookup"><span data-stu-id="4c4f4-116">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c4f4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) (antecedente), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4c4f4-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4c4f4-119">Un [**\_ archivo**](cim-datafile.md) de datos CIM que describe el archivo de datos que participa en la ejecución del proceso.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-119">A [**CIM\_DataFile**](cim-datafile.md) that describes the data file participating in the execution of the process.</span></span>

</dd> <dt>

<span data-ttu-id="4c4f4-120">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-120">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4f4-121">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c4f4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-123">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4c4f4-123">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4c4f4-124">Dirección base del módulo en el espacio de direcciones del proceso asociado.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-124">Base address of the module in the address space of the associated process.</span></span>

<span data-ttu-id="4c4f4-125">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4c4f4-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4c4f4-126">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4f4-127">Tipo de datos **: \_ proceso CIM**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-127">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c4f4-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-129">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) (dependiente), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4c4f4-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4c4f4-130">[**\_ Proceso CIM**](cim-process.md) que describe el proceso.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-130">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="4c4f4-131">**GlobalProcessCount**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-131">**GlobalProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4f4-132">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c4f4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-134">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4c4f4-134">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4c4f4-135">Número actual de procesos que tienen el archivo cargado en memoria.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-135">Current number of processes that have the file loaded in memory.</span></span>

</dd> <dt>

<span data-ttu-id="4c4f4-136">**ModuleInstance**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-136">**ModuleInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4f4-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c4f4-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-139">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4c4f4-139">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4c4f4-140">Identificador de instancia de Win32.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-140">Win32 instance handle.</span></span> <span data-ttu-id="4c4f4-141">Esta propiedad está obsoleta y no hay ningún valor de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-141">This property is obsolete, and there is no replacement value.</span></span>

</dd> <dt>

<span data-ttu-id="4c4f4-142">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-142">**ProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4f4-143">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c4f4-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c4f4-145">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4c4f4-145">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4c4f4-146">Recuento de referencias del archivo en el proceso asociado.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-146">Reference count of the file in the associated process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c4f4-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c4f4-147">Remarks</span></span>

<span data-ttu-id="4c4f4-148">La clase **CIM \_ ProcessExecutable** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="4c4f4-148">The **CIM\_ProcessExecutable** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="4c4f4-149">WMI implementa la clase **\_ ProcessExecutable de CIM** .</span><span class="sxs-lookup"><span data-stu-id="4c4f4-149">WMI implements the **CIM\_ProcessExecutable** class.</span></span> <span data-ttu-id="4c4f4-150">La clase **CIM \_ ProcessExecutable** es una clase dinámica.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-150">The **CIM\_ProcessExecutable** class is a dynamic class.</span></span>

<span data-ttu-id="4c4f4-151">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4c4f4-152">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="4c4f4-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4f4-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c4f4-153">Requirements</span></span>



| <span data-ttu-id="4c4f4-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c4f4-154">Requirement</span></span> | <span data-ttu-id="4c4f4-155">Value</span><span class="sxs-lookup"><span data-stu-id="4c4f4-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c4f4-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c4f4-156">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4f4-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c4f4-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c4f4-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c4f4-158">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4f4-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c4f4-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c4f4-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4c4f4-160">Namespace</span></span><br/>                | <span data-ttu-id="4c4f4-161">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4c4f4-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4c4f4-162">MOF</span><span class="sxs-lookup"><span data-stu-id="4c4f4-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c4f4-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c4f4-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c4f4-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c4f4-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c4f4-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c4f4-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c4f4-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c4f4-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4f4-167">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="4c4f4-167">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

