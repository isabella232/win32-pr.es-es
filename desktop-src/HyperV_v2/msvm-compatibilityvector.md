---
description: Hace referencia a la información de compatibilidad de una máquina virtual (VM) (cuando se ejecuta en un equipo de máquina virtual) o un host (cuando se ejecuta en un sistema de equipo host).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Msvm_CompatibilityVector (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66eba92daf420fb4bd332d3f7d537b7936618ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911030"
---
# <a name="msvm_compatibilityvector-class"></a><span data-ttu-id="f6b70-103">MSVM \_ CompatibilityVector (clase)</span><span class="sxs-lookup"><span data-stu-id="f6b70-103">Msvm\_CompatibilityVector class</span></span>

<span data-ttu-id="f6b70-104">Hace referencia a la información de compatibilidad de una máquina virtual (VM) (cuando se ejecuta en un equipo de máquina virtual) o un host (cuando se ejecuta en un sistema de equipo host).</span><span class="sxs-lookup"><span data-stu-id="f6b70-104">References the compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span>

<span data-ttu-id="f6b70-105">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f6b70-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6b70-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6b70-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a><span data-ttu-id="f6b70-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6b70-107">Members</span></span>

<span data-ttu-id="f6b70-108">La clase **MSVM \_ CompatibilityVector** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f6b70-108">The **Msvm\_CompatibilityVector** class has these types of members:</span></span>

-   [<span data-ttu-id="f6b70-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6b70-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6b70-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6b70-110">Properties</span></span>

<span data-ttu-id="f6b70-111">La clase **MSVM \_ CompatibilityVector** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6b70-111">The **Msvm\_CompatibilityVector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6b70-112">**CompareOperation**</span><span class="sxs-lookup"><span data-stu-id="f6b70-112">**CompareOperation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b70-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6b70-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6b70-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6b70-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b70-115">Identifica la operación de comparación que devolverá True si y solo si dos vectores son compatibles.</span><span class="sxs-lookup"><span data-stu-id="f6b70-115">Identifies the comparison operation that will return true if and only if two vectors are compatible.</span></span> <span data-ttu-id="f6b70-116">Los datos de la máquina virtual están en el lado izquierdo de la comparación y los datos del host están en el lado derecho.</span><span class="sxs-lookup"><span data-stu-id="f6b70-116">The VM's data is on the left hand side of the comparison, and the host's data is on the right hand side.</span></span>

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

<span data-ttu-id="f6b70-117">**Igual** (0)</span><span class="sxs-lookup"><span data-stu-id="f6b70-117">**Equal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

<span data-ttu-id="f6b70-118">**Supraconjunto** (1)</span><span class="sxs-lookup"><span data-stu-id="f6b70-118">**Superset** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

<span data-ttu-id="f6b70-119">**Subconjunto** (2)</span><span class="sxs-lookup"><span data-stu-id="f6b70-119">**Subset** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

<span data-ttu-id="f6b70-120">**Disjuntos** (3)</span><span class="sxs-lookup"><span data-stu-id="f6b70-120">**Disjoint** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

<span data-ttu-id="f6b70-121">**GreaterThan** (4)</span><span class="sxs-lookup"><span data-stu-id="f6b70-121">**GreaterThan** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

<span data-ttu-id="f6b70-122">**GreaterThanOrEqual** (5)</span><span class="sxs-lookup"><span data-stu-id="f6b70-122">**GreaterThanOrEqual** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

<span data-ttu-id="f6b70-123">**Lessthan** (6)</span><span class="sxs-lookup"><span data-stu-id="f6b70-123">**LessThan** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

<span data-ttu-id="f6b70-124">**LessThanOrEqual** (7)</span><span class="sxs-lookup"><span data-stu-id="f6b70-124">**LessThanOrEqual** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

<span data-ttu-id="f6b70-125">**Múltiplo** (8)</span><span class="sxs-lookup"><span data-stu-id="f6b70-125">**Multiple** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

<span data-ttu-id="f6b70-126">**Divisible** (9)</span><span class="sxs-lookup"><span data-stu-id="f6b70-126">**Divisible** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6b70-127">**CompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="f6b70-127">**CompatibilityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b70-128">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f6b70-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6b70-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6b70-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b70-130">Los datos del atributo de compatibilidad real que se usan para la comparación.</span><span class="sxs-lookup"><span data-stu-id="f6b70-130">The actual compatibility attribute data that is used for comparison.</span></span>

</dd> <dt>

<span data-ttu-id="f6b70-131">**VectorId**</span><span class="sxs-lookup"><span data-stu-id="f6b70-131">**VectorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6b70-132">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6b70-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6b70-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6b70-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6b70-134">Identifica un vector de compatibilidad que representa un atributo concreto.</span><span class="sxs-lookup"><span data-stu-id="f6b70-134">Identifies a compatibility vector that represents a specific attribute.</span></span> <span data-ttu-id="f6b70-135">Esta propiedad se usa para hacer coincidir los vectores correspondientes entre un host y una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f6b70-135">This property is used to match corresponding vectors between a host and a VM.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6b70-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6b70-136">Remarks</span></span>

<span data-ttu-id="f6b70-137">El método [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) de la clase [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) devuelve una matriz de instancias de **MSVM \_ CompatibilityVector** para el host (si se ejecuta en el host) o una máquina virtual (si se ejecuta en la máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="f6b70-137">The [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class returns an array of **Msvm\_CompatibilityVector** instances for the host (if run on the host) or a VM (if run on the VM).</span></span> <span data-ttu-id="f6b70-138">Cada **entrada \_ CompatibilityVector de MSVM** de la lista describe un vector de atributo de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="f6b70-138">Each **Msvm\_CompatibilityVector** entry in the list describes a compatibility attribute vector.</span></span> <span data-ttu-id="f6b70-139">Para que una máquina virtual sea compatible con un host, todos sus atributos de compatibilidad deben ser compatibles con los atributos de host s.</span><span class="sxs-lookup"><span data-stu-id="f6b70-139">For a VM to be compatible with a host, all of its compatibility attributes must be compatible with the host s attributes.</span></span>

<span data-ttu-id="f6b70-140">Cada entrada de **\_ CompatibilityVector de MSVM** tiene estas propiedades:</span><span class="sxs-lookup"><span data-stu-id="f6b70-140">Each **Msvm\_CompatibilityVector** entry has these properties:</span></span>

<dl> <dt>

<span data-ttu-id="f6b70-141">**VectorId**</span><span class="sxs-lookup"><span data-stu-id="f6b70-141">**VectorId**</span></span>
</dt> <dd>

<span data-ttu-id="f6b70-142">Identifica de forma única el vector de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="f6b70-142">Uniquely identifies the compatibility vector.</span></span> <span data-ttu-id="f6b70-143">Se usa para hacer coincidir los vectores que se van a comparar entre un host y una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f6b70-143">This is used to match the vectors to compare between a host and a VM.</span></span>

</dd> <dt>

<span data-ttu-id="f6b70-144">**CompareOperation**</span><span class="sxs-lookup"><span data-stu-id="f6b70-144">**CompareOperation**</span></span>
</dt> <dd>

<span data-ttu-id="f6b70-145">Identifica la operación de comparación que determina si los vectores son compatibles.</span><span class="sxs-lookup"><span data-stu-id="f6b70-145">Identifies the comparison operation that determines whether the vectors are compatible.</span></span>

</dd> <dt>

<span data-ttu-id="f6b70-146">**CompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="f6b70-146">**CompatibilityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f6b70-147">Contiene el atributo de compatibilidad real; Esto es, de hecho, la carga del atributo (por ejemplo, la máscara de características del procesador, el tamaño del vaciado de la línea de caché, etc.)</span><span class="sxs-lookup"><span data-stu-id="f6b70-147">Contains the actual compatibility attribute; This is effectively the attribute payload (e.g. processor feature mask, cache line flush size, etc.)</span></span>

</dd> </dl>

<span data-ttu-id="f6b70-148">El conjunto de operaciones definido para **CompareOperation** solo implica la comparación de enteros básica y la lógica bit a bit.</span><span class="sxs-lookup"><span data-stu-id="f6b70-148">The set of operations defined for **CompareOperation** just involve basic integer comparison and bitwise logic.</span></span> <span data-ttu-id="f6b70-149">Esto permite que el contenido real de **CompatibilityInfo** siga siendo opaco.</span><span class="sxs-lookup"><span data-stu-id="f6b70-149">This enables the actual contents of **CompatibilityInfo** to remain opaque.</span></span> <span data-ttu-id="f6b70-150">El conjunto de operaciones incluye:</span><span class="sxs-lookup"><span data-stu-id="f6b70-150">The set of operations include:</span></span>



| <span data-ttu-id="f6b70-151">CompareOperation</span><span class="sxs-lookup"><span data-stu-id="f6b70-151">CompareOperation</span></span> | <span data-ttu-id="f6b70-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6b70-152">Description</span></span>                                      | <span data-ttu-id="f6b70-153">Comparación de pseudocódigo</span><span class="sxs-lookup"><span data-stu-id="f6b70-153">Pseudocode Comparison</span></span>                |
|------------------|--------------------------------------------------|--------------------------------------|
| <span data-ttu-id="f6b70-154">VmCcEqual</span><span class="sxs-lookup"><span data-stu-id="f6b70-154">VmCcEqual</span></span>        | <span data-ttu-id="f6b70-155">VmAttr debe ser igual a HostAttr</span><span class="sxs-lookup"><span data-stu-id="f6b70-155">VmAttr must equal HostAttr</span></span>                       | <span data-ttu-id="f6b70-156">Si (VmAttr = = HostAttr)</span><span class="sxs-lookup"><span data-stu-id="f6b70-156">If (VmAttr == HostAttr)</span></span>              |
| <span data-ttu-id="f6b70-157">VmCcSuperSet</span><span class="sxs-lookup"><span data-stu-id="f6b70-157">VmCcSuperSet</span></span>     | <span data-ttu-id="f6b70-158">VmAttr debe ser un superconjunto de HostAttr</span><span class="sxs-lookup"><span data-stu-id="f6b70-158">VmAttr must be a superset of HostAttr</span></span>            | <span data-ttu-id="f6b70-159">If ((VmAttr & HostAttr) = = HostAttr)</span><span class="sxs-lookup"><span data-stu-id="f6b70-159">If ((VmAttr & HostAttr) == HostAttr)</span></span> |
| <span data-ttu-id="f6b70-160">VmCcSubSet</span><span class="sxs-lookup"><span data-stu-id="f6b70-160">VmCcSubSet</span></span>       | <span data-ttu-id="f6b70-161">VmAttr debe ser un subconjunto de HostAttr</span><span class="sxs-lookup"><span data-stu-id="f6b70-161">VmAttr must be a subset of HostAttr</span></span>              | <span data-ttu-id="f6b70-162">If ((VmAttr & HostAttr) = = VmAttr)</span><span class="sxs-lookup"><span data-stu-id="f6b70-162">If ((VmAttr & HostAttr) == VmAttr)</span></span>   |
| <span data-ttu-id="f6b70-163">VmCcDisjointSet</span><span class="sxs-lookup"><span data-stu-id="f6b70-163">VmCcDisjointSet</span></span>  | <span data-ttu-id="f6b70-164">VmAttr debe ser un conjunto separado de HostAttr</span><span class="sxs-lookup"><span data-stu-id="f6b70-164">VmAttr must be a disjoint set from HostAttr</span></span>      | <span data-ttu-id="f6b70-165">If ((VmAttr & HostAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="f6b70-165">If ((VmAttr & HostAttr) == 0)</span></span>        |
| <span data-ttu-id="f6b70-166">VmCcGreater</span><span class="sxs-lookup"><span data-stu-id="f6b70-166">VmCcGreater</span></span>      | <span data-ttu-id="f6b70-167">VmAttr debe ser mayor que HostAttr</span><span class="sxs-lookup"><span data-stu-id="f6b70-167">VmAttr must be greater than HostAttr</span></span>             | <span data-ttu-id="f6b70-168">If (VmAttr > HostAttr)</span><span class="sxs-lookup"><span data-stu-id="f6b70-168">If (VmAttr > HostAttr)</span></span>            |
| <span data-ttu-id="f6b70-169">VmCcGreaterEqual</span><span class="sxs-lookup"><span data-stu-id="f6b70-169">VmCcGreaterEqual</span></span> | <span data-ttu-id="f6b70-170">VmAttr debe ser mayor o igual que HostAttr</span><span class="sxs-lookup"><span data-stu-id="f6b70-170">VmAttr must be greater than or equal to HostAttr</span></span> | <span data-ttu-id="f6b70-171">If (VmAttr >= HostAttr)</span><span class="sxs-lookup"><span data-stu-id="f6b70-171">If (VmAttr >= HostAttr)</span></span>           |
| <span data-ttu-id="f6b70-172">VmCcLess</span><span class="sxs-lookup"><span data-stu-id="f6b70-172">VmCcLess</span></span>         | <span data-ttu-id="f6b70-173">VmAttr debe ser menor que HostAttr</span><span class="sxs-lookup"><span data-stu-id="f6b70-173">VmAttr must be less than HostAttr</span></span>                | <span data-ttu-id="f6b70-174">If (VmAttr < HostAttr)</span><span class="sxs-lookup"><span data-stu-id="f6b70-174">If (VmAttr < HostAttr)</span></span>            |
| <span data-ttu-id="f6b70-175">VmCcLessEqual</span><span class="sxs-lookup"><span data-stu-id="f6b70-175">VmCcLessEqual</span></span>    | <span data-ttu-id="f6b70-176">VmAttr debe ser menor o igual que HostAttr</span><span class="sxs-lookup"><span data-stu-id="f6b70-176">VmAttr must be less than or equal to HostAttr</span></span>    | <span data-ttu-id="f6b70-177">If (VmAttr <= HostAttr)</span><span class="sxs-lookup"><span data-stu-id="f6b70-177">If (VmAttr <= HostAttr)</span></span>           |
| <span data-ttu-id="f6b70-178">VmCcMultiple</span><span class="sxs-lookup"><span data-stu-id="f6b70-178">VmCcMultiple</span></span>     | <span data-ttu-id="f6b70-179">VmAttr debe ser un múltiplo de HostAttr</span><span class="sxs-lookup"><span data-stu-id="f6b70-179">VmAttr must be a multiple of HostAttr</span></span>            | <span data-ttu-id="f6b70-180">If ((VmAttr% HostAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="f6b70-180">If ((VmAttr % HostAttr) == 0)</span></span>        |
| <span data-ttu-id="f6b70-181">VmCcDivisor</span><span class="sxs-lookup"><span data-stu-id="f6b70-181">VmCcDivisor</span></span>      | <span data-ttu-id="f6b70-182">VmAttr debe ser un divisor de HostAttr</span><span class="sxs-lookup"><span data-stu-id="f6b70-182">VmAttr must be a divisor of HostAttr</span></span>             | <span data-ttu-id="f6b70-183">If ((HostAttr% VmAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="f6b70-183">If ((HostAttr % VmAttr) == 0)</span></span>        |



 

<span data-ttu-id="f6b70-184">SCVMM debe realizar estos pasos para determinar si una máquina virtual es compatible con un host.</span><span class="sxs-lookup"><span data-stu-id="f6b70-184">SCVMM needs to do these steps to determine whether a VM is compatible with a host.</span></span>

<span data-ttu-id="f6b70-185">**Para determinar si una máquina virtual es compatible con un host**</span><span class="sxs-lookup"><span data-stu-id="f6b70-185">**To determine whether a VM is compatible with a host**</span></span>

1.  <span data-ttu-id="f6b70-186">Recorra en iteración todos los elementos **\_ CompatibilityVector de MSVM** para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f6b70-186">Iterate through all of the **Msvm\_CompatibilityVector** elements for the VM.</span></span>
2.  <span data-ttu-id="f6b70-187">Para cada **elemento \_ CompatibilityVector de MSVM** , use la operación de compatibilidad especificada en **CompareOperation** para comparar el vector de compatibilidad de hardware de la máquina virtual con el vector de compatibilidad correspondiente para el host.</span><span class="sxs-lookup"><span data-stu-id="f6b70-187">For each **Msvm\_CompatibilityVector** element, use the compatibility operation specified in **CompareOperation** to compare the VM s hardware compatibility vector with the corresponding compatibility vector for the host.</span></span>
3.  <span data-ttu-id="f6b70-188">Si todos los elementos **\_ CompatibilityVector de MSVM** de la máquina virtual se consideran compatibles, la máquina virtual es compatible con el host (desde una perspectiva de características del procesador).</span><span class="sxs-lookup"><span data-stu-id="f6b70-188">If the all of the **Msvm\_CompatibilityVector** elements from the VM are deemed compatible, the VM is compatible with the host (from a processor feature perspective).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b70-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6b70-189">Requirements</span></span>



| <span data-ttu-id="f6b70-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6b70-190">Requirement</span></span> | <span data-ttu-id="f6b70-191">Value</span><span class="sxs-lookup"><span data-stu-id="f6b70-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b70-192">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6b70-192">Minimum supported client</span></span><br/> | <span data-ttu-id="f6b70-193">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="f6b70-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f6b70-194">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6b70-194">Minimum supported server</span></span><br/> | <span data-ttu-id="f6b70-195">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6b70-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f6b70-196">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6b70-196">Namespace</span></span><br/>                | <span data-ttu-id="f6b70-197">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f6b70-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6b70-198">MOF</span><span class="sxs-lookup"><span data-stu-id="f6b70-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6b70-199"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6b70-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6b70-200">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6b70-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6b70-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6b70-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f6b70-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6b70-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b70-203">**GetSystemCompatibilityVectors**</span><span class="sxs-lookup"><span data-stu-id="f6b70-203">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="f6b70-204">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="f6b70-204">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




