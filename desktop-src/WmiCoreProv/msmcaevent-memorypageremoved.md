---
description: Indica que se ha quitado una página de memoria del uso del sistema debido a errores de comprobación y corrección de errores de hardware excesivos (ECC). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: 364a2520-8d7c-44f2-95f6-eea9a5531975
title: MSMCAEvent_MemoryPageRemoved (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryPageRemoved
- MSMCAEvent_MemoryPageRemoved.Active
- MSMCAEvent_MemoryPageRemoved.InstanceName
- MSMCAEvent_MemoryPageRemoved.PhysicalAddress
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dc29c5b51531e204ab50f062dd08ef8d5abf1bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697544"
---
# <a name="msmcaevent_memorypageremoved-class"></a><span data-ttu-id="f301a-104">MSMCAEvent \_ MemoryPageRemoved (clase)</span><span class="sxs-lookup"><span data-stu-id="f301a-104">MSMCAEvent\_MemoryPageRemoved class</span></span>

<span data-ttu-id="f301a-105">La clase **MSMCAEvent \_ MemoryPageRemoved** indica que se ha quitado una página de memoria del uso del sistema debido a errores excesivos de comprobación de errores de hardware y de corrección (ECC).</span><span class="sxs-lookup"><span data-stu-id="f301a-105">The **MSMCAEvent\_MemoryPageRemoved** class indicates that a memory page has been removed from system use due to excessive hardware Error Checking and Correcting (ECC) errors.</span></span> <span data-ttu-id="f301a-106">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f301a-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="f301a-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f301a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f301a-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f301a-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f301a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f301a-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryPageRemoved : WmiEvent
{
  boolean Active;
  string  InstanceName;
  uint64  PhysicalAddress;
};
```

## <a name="members"></a><span data-ttu-id="f301a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f301a-110">Members</span></span>

<span data-ttu-id="f301a-111">La clase **MSMCAEvent \_ MemoryPageRemoved** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f301a-111">The **MSMCAEvent\_MemoryPageRemoved** class has these types of members:</span></span>

-   [<span data-ttu-id="f301a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f301a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f301a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f301a-113">Properties</span></span>

<span data-ttu-id="f301a-114">La clase **MSMCAEvent \_ MemoryPageRemoved** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f301a-114">The **MSMCAEvent\_MemoryPageRemoved** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f301a-115">**Activo**</span><span class="sxs-lookup"><span data-stu-id="f301a-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f301a-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f301a-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f301a-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f301a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f301a-118">**True** si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f301a-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f301a-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="f301a-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f301a-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f301a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f301a-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f301a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f301a-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f301a-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f301a-123">Identificador único para esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="f301a-123">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="f301a-124">**PhysicalAddress**</span><span class="sxs-lookup"><span data-stu-id="f301a-124">**PhysicalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f301a-125">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f301a-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f301a-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f301a-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f301a-127">Dirección de la página de memoria que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="f301a-127">Address of the page of memory that has been removed.</span></span>

<span data-ttu-id="f301a-128">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f301a-128">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f301a-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f301a-129">Remarks</span></span>

<span data-ttu-id="f301a-130">La clase **MSMCAEvent \_ MemoryPageRemoved** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="f301a-130">The **MSMCAEvent\_MemoryPageRemoved** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f301a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f301a-131">Requirements</span></span>



| <span data-ttu-id="f301a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f301a-132">Requirement</span></span> | <span data-ttu-id="f301a-133">Value</span><span class="sxs-lookup"><span data-stu-id="f301a-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f301a-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f301a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f301a-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f301a-135">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="f301a-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f301a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f301a-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f301a-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="f301a-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f301a-138">Namespace</span></span><br/>                | <span data-ttu-id="f301a-139">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="f301a-139">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="f301a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f301a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f301a-141"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f301a-141"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f301a-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f301a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f301a-143"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f301a-143"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f301a-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="f301a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f301a-145">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="f301a-145">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="f301a-146">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="f301a-146">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

