---
description: La \_ relación SlotInSlot de CIM representa la capacidad de un adaptador especial de extender la estructura de ranura existente para habilitar la conexión de tarjetas que, de lo contrario, no es compatible con un marco o un panel de hospedaje.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: CIM_SlotInSlot (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659372"
---
# <a name="cim_slotinslot-class"></a><span data-ttu-id="13d7e-103">\_Clase SlotInSlot de CIM</span><span class="sxs-lookup"><span data-stu-id="13d7e-103">CIM\_SlotInSlot class</span></span>

<span data-ttu-id="13d7e-104">La **relación \_ SlotInSlot de CIM** representa la capacidad de un adaptador especial de extender la estructura de ranura existente para habilitar la conexión de tarjetas que, de lo contrario, no es compatible con un marco o un panel de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="13d7e-104">The **CIM\_SlotInSlot** relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span> <span data-ttu-id="13d7e-105">Las ranuras son tipos especiales de conectores en los que normalmente se insertan tarjetas adaptadoras.</span><span class="sxs-lookup"><span data-stu-id="13d7e-105">Slots are special types of connectors into which adapter cards are typically inserted.</span></span> <span data-ttu-id="13d7e-106">El adaptador crea eficazmente una nueva ranura y se puede considerar (conceptualmente) como una ranura en una ranura.</span><span class="sxs-lookup"><span data-stu-id="13d7e-106">The adapter effectively creates a new slot and can be thought of (conceptually) as a slot in a slot.</span></span> <span data-ttu-id="13d7e-107">Las tarjetas que de otro modo serían físicamente o eléctricamente incompatibles con las ranuras existentes se admitirían al interactuar con la ranura proporcionada por el adaptador.</span><span class="sxs-lookup"><span data-stu-id="13d7e-107">Cards that would otherwise be physically or electrically incompatible with the existing slots would be supported by interfacing to the slot provided by the adapter.</span></span> <span data-ttu-id="13d7e-108">Por ejemplo, las tarjetas de red son muy costosas.</span><span class="sxs-lookup"><span data-stu-id="13d7e-108">For example, networking boards are very expensive.</span></span> <span data-ttu-id="13d7e-109">A medida que el nuevo hardware está disponible, cambian las configuraciones de chasis y tarjeta.</span><span class="sxs-lookup"><span data-stu-id="13d7e-109">As new hardware becomes available, chassis and card configurations change.</span></span> <span data-ttu-id="13d7e-110">Para proteger la inversión de sus clientes, los proveedores de redes fabrican adaptadores especiales que permiten que las tarjetas antiguas se ajusten a nuevos chasis o paneles de hospedaje o a tarjetas nuevas para caber en tarjetas antiguas mediante el uso de un adaptador especial que se adapta a una o más ranuras existentes y presenta una nueva ranura en la que puede caber la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="13d7e-110">To protect the investment of their customers, networking vendors will manufacture special adapters that enable old cards to fit into new chassis or hosting boards or new cards to fit into old cards by using a special adapter that fits over one or more existing slots and presents a new slot into which the card can fit.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13d7e-111">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="13d7e-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="13d7e-112">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="13d7e-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="13d7e-113">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="13d7e-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="13d7e-114">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="13d7e-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13d7e-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13d7e-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="13d7e-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="13d7e-116">Members</span></span>

<span data-ttu-id="13d7e-117">La clase **CIM \_ SlotInSlot** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="13d7e-117">The **CIM\_SlotInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="13d7e-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13d7e-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13d7e-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13d7e-119">Properties</span></span>

<span data-ttu-id="13d7e-120">La clase **CIM \_ SlotInSlot** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="13d7e-120">The **CIM\_SlotInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13d7e-121">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="13d7e-121">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d7e-122">Tipo de datos **: \_ ranura CIM**</span><span class="sxs-lookup"><span data-stu-id="13d7e-122">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="13d7e-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13d7e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d7e-124">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="13d7e-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="13d7e-125">Una [**\_ ranura CIM**](cim-slot.md) que describe las ranuras existentes de la placa de hospedaje o fotograma que se está adaptando para dar cabida a una tarjeta que de otro modo no sería físicamente o eléctricamente compatible con ella.</span><span class="sxs-lookup"><span data-stu-id="13d7e-125">A [**CIM\_Slot**](cim-slot.md) that describes the existing slot(s) of the hosting board, or frame that are being adapted to accommodate a card that would otherwise not be physically and/or electrically compatible with it.</span></span>

</dd> <dt>

<span data-ttu-id="13d7e-126">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="13d7e-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d7e-127">Tipo de datos **: \_ ranura CIM**</span><span class="sxs-lookup"><span data-stu-id="13d7e-127">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="13d7e-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13d7e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d7e-129">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="13d7e-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="13d7e-130">Una [**\_ ranura CIM**](cim-slot.md) que describe la nueva ranura proporcionada por la placa del adaptador.</span><span class="sxs-lookup"><span data-stu-id="13d7e-130">A [**CIM\_Slot**](cim-slot.md) that describes the new slot provided by the adapter board.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13d7e-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13d7e-131">Remarks</span></span>

<span data-ttu-id="13d7e-132">La clase **CIM \_ SlotInSlot** se deriva de [**CIM \_ ConnectTo**](cim-connectedto.md).</span><span class="sxs-lookup"><span data-stu-id="13d7e-132">The **CIM\_SlotInSlot** class is derived from [**CIM\_ConnectedTo**](cim-connectedto.md).</span></span>

<span data-ttu-id="13d7e-133">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="13d7e-133">WMI does not implement this class.</span></span>

<span data-ttu-id="13d7e-134">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="13d7e-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="13d7e-135">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="13d7e-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d7e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13d7e-136">Requirements</span></span>



| <span data-ttu-id="13d7e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="13d7e-137">Requirement</span></span> | <span data-ttu-id="13d7e-138">Value</span><span class="sxs-lookup"><span data-stu-id="13d7e-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13d7e-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13d7e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="13d7e-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13d7e-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13d7e-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13d7e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="13d7e-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13d7e-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13d7e-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="13d7e-143">Namespace</span></span><br/>                | <span data-ttu-id="13d7e-144">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="13d7e-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13d7e-145">MOF</span><span class="sxs-lookup"><span data-stu-id="13d7e-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13d7e-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13d7e-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13d7e-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13d7e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13d7e-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13d7e-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d7e-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="13d7e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d7e-150">**\_Connected de CIM**</span><span class="sxs-lookup"><span data-stu-id="13d7e-150">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> </dl>

 

