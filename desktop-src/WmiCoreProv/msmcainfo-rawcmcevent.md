---
description: Contiene un evento de comprobación de máquina corregida (CMC). Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: e12efbf7-7d53-415a-bc48-90d33e4ce16d
title: MSMCAInfo_RawCMCEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCMCEvent
- MSMCAInfo_RawCMCEvent.Active
- MSMCAInfo_RawCMCEvent.Count
- MSMCAInfo_RawCMCEvent.InstanceName
- MSMCAInfo_RawCMCEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 1bb60d5fbcf004b924a91e640d8cd8a8c5ad3c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716706"
---
# <a name="msmcainfo_rawcmcevent-class"></a><span data-ttu-id="89e0f-104">MSMCAInfo \_ RawCMCEvent (clase)</span><span class="sxs-lookup"><span data-stu-id="89e0f-104">MSMCAInfo\_RawCMCEvent class</span></span>

<span data-ttu-id="89e0f-105">La clase **MSMCAInfo \_ RawCMCEvent** contiene un evento de comprobación de la máquina (CMC) corregido.</span><span class="sxs-lookup"><span data-stu-id="89e0f-105">The **MSMCAInfo\_RawCMCEvent** class contains a Corrected Machine Check (CMC) event.</span></span> <span data-ttu-id="89e0f-106">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="89e0f-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="89e0f-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="89e0f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="89e0f-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="89e0f-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89e0f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89e0f-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawCMCEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="89e0f-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="89e0f-110">Members</span></span>

<span data-ttu-id="89e0f-111">La clase **MSMCAInfo \_ RawCMCEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="89e0f-111">The **MSMCAInfo\_RawCMCEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="89e0f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="89e0f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89e0f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="89e0f-113">Properties</span></span>

<span data-ttu-id="89e0f-114">La clase **MSMCAInfo \_ RawCMCEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="89e0f-114">The **MSMCAInfo\_RawCMCEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89e0f-115">**Activo**</span><span class="sxs-lookup"><span data-stu-id="89e0f-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89e0f-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="89e0f-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89e0f-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89e0f-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89e0f-118">TRUE si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="89e0f-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89e0f-119">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="89e0f-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89e0f-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89e0f-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89e0f-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89e0f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89e0f-122">Número de registros de error.</span><span class="sxs-lookup"><span data-stu-id="89e0f-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="89e0f-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="89e0f-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89e0f-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="89e0f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89e0f-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89e0f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89e0f-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="89e0f-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="89e0f-127">Identificador único de esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="89e0f-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="89e0f-128">**Registros**</span><span class="sxs-lookup"><span data-stu-id="89e0f-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89e0f-129">Tipo de datos: matriz de **\_ entrada MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="89e0f-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="89e0f-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89e0f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89e0f-131">Matriz de registros de errores de arquitectura de comprobación de máquinas (MCA).</span><span class="sxs-lookup"><span data-stu-id="89e0f-131">Array of Machine Check Architecture (MCA) error records.</span></span> <span data-ttu-id="89e0f-132">La propiedad **Count** especifica el número de registros de error de MCA en la matriz.</span><span class="sxs-lookup"><span data-stu-id="89e0f-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89e0f-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89e0f-133">Remarks</span></span>

<span data-ttu-id="89e0f-134">La clase **MSMCAInfo \_ RawCMCEvent** se deriva de [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="89e0f-134">The **MSMCAInfo\_RawCMCEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89e0f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89e0f-135">Requirements</span></span>



| <span data-ttu-id="89e0f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="89e0f-136">Requirement</span></span> | <span data-ttu-id="89e0f-137">Value</span><span class="sxs-lookup"><span data-stu-id="89e0f-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89e0f-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89e0f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="89e0f-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="89e0f-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="89e0f-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89e0f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="89e0f-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89e0f-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="89e0f-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="89e0f-142">Namespace</span></span><br/>                | <span data-ttu-id="89e0f-143">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="89e0f-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="89e0f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="89e0f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89e0f-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89e0f-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="89e0f-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89e0f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89e0f-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89e0f-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89e0f-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="89e0f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89e0f-149">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="89e0f-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="89e0f-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="89e0f-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

