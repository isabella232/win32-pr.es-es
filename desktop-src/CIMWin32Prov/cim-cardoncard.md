---
description: La \_ Asociación CardOnCard de CIM describe las relaciones de las tarjetas que se pueden conectar a las motherboards/placas base, daughtercards de un adaptador o tarjetas que admiten módulos especiales de tipo tarjeta.
ms.assetid: a500b29d-d836-4755-b5df-b296e3cbd2ab
ms.tgt_platform: multiple
title: CIM_CardOnCard (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardOnCard
- CIM_CardOnCard.LocationWithinContainer
- CIM_CardOnCard.PartComponent
- CIM_CardOnCard.GroupComponent
- CIM_CardOnCard.MountOrSlotDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15f94bb8d0f159e71cac44f069f9d8e7d9453509
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423387"
---
# <a name="cim_cardoncard-class"></a><span data-ttu-id="7c970-103">\_Clase CardOnCard de CIM</span><span class="sxs-lookup"><span data-stu-id="7c970-103">CIM\_CardOnCard class</span></span>

<span data-ttu-id="7c970-104">La **Asociación \_ CardOnCard de CIM** describe las relaciones de las tarjetas que se pueden conectar a las motherboards/placas base, daughtercards de un adaptador o tarjetas que admiten módulos especiales de tipo tarjeta.</span><span class="sxs-lookup"><span data-stu-id="7c970-104">The **CIM\_CardOnCard** association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c970-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7c970-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7c970-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7c970-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7c970-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7c970-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7c970-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7c970-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c970-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c970-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B77-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardOnCard : CIM_Container
{
  string       LocationWithinContainer;
  CIM_Card REF PartComponent;
  CIM_Card REF GroupComponent;
  string       MountOrSlotDescription;
};
```

## <a name="members"></a><span data-ttu-id="7c970-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="7c970-110">Members</span></span>

<span data-ttu-id="7c970-111">La clase **CIM \_ CardOnCard** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7c970-111">The **CIM\_CardOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="7c970-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c970-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c970-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c970-113">Properties</span></span>

<span data-ttu-id="7c970-114">La clase **CIM \_ CardOnCard** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7c970-114">The **CIM\_CardOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c970-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="7c970-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c970-116">Tipo de datos **: \_ tarjeta CIM**</span><span class="sxs-lookup"><span data-stu-id="7c970-116">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="7c970-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c970-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c970-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7c970-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7c970-119">[**\_ Tarjeta CIM**](cim-card.md) que describe la tarjeta que hospeda otra tarjeta.</span><span class="sxs-lookup"><span data-stu-id="7c970-119">A [**CIM\_Card**](cim-card.md) that describes the card that hosts another card.</span></span>

</dd> <dt>

<span data-ttu-id="7c970-120">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="7c970-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c970-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c970-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c970-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c970-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c970-123">Cadena de forma libre que representa la posición del elemento físico en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="7c970-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="7c970-124">La información relativa a los elementos estacionarios del contenedor (por ejemplo, "segunda Bahía de unidad de la parte superior"), ángulos, altitudes y otros datos se puede grabar en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7c970-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="7c970-125">Esta cadena se puede complementar o utilizar en lugar de crear una instancia del objeto de [**\_ Ubicación CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="7c970-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="7c970-126">Esta propiedad se hereda del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="7c970-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c970-127">**MountOrSlotDescription**</span><span class="sxs-lookup"><span data-stu-id="7c970-127">**MountOrSlotDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c970-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c970-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c970-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c970-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c970-130">Describe e identifica cómo se monta la tarjeta o se conecta a la tarjeta "otra".</span><span class="sxs-lookup"><span data-stu-id="7c970-130">Describes and identifies how the card is mounted on or plugged into the "other" card.</span></span> <span data-ttu-id="7c970-131">La información de la ranura puede incluirse en este campo y puede ser suficiente para determinados fines de administración, lo que evita la creación de instancias de objetos de conector/ranura solo para modelar la relación de las tarjetas con los paneles de hospedaje u otros adaptadores.</span><span class="sxs-lookup"><span data-stu-id="7c970-131">Slot information can be included in this field and may be sufficient for certain management purposes, which avoids creating instantiations of connector/slot objects just to model the relationship of cards to hosting boards or other adapters.</span></span> <span data-ttu-id="7c970-132">Por otro lado, si la información de ranura y de conector está disponible, este campo se puede usar para proporcionar datos detallados de montaje de espacio o de montaje.</span><span class="sxs-lookup"><span data-stu-id="7c970-132">On the other hand, if slot and connector information is available, this field can be used to provide detailed mounting or slot insertion data.</span></span>

</dd> <dt>

<span data-ttu-id="7c970-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7c970-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c970-134">Tipo de datos **: \_ tarjeta CIM**</span><span class="sxs-lookup"><span data-stu-id="7c970-134">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="7c970-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c970-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c970-136">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="7c970-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="7c970-137">Una [**\_ tarjeta CIM**](cim-card.md) que describe la tarjeta conectada o montada en otra tarjeta.</span><span class="sxs-lookup"><span data-stu-id="7c970-137">A [**CIM\_Card**](cim-card.md) that describes the card that is plugged into or otherwise mounted on another card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c970-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c970-138">Remarks</span></span>

<span data-ttu-id="7c970-139">La clase **CIM \_ CardOnCard** se deriva del [**\_ contenedor CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="7c970-139">The **CIM\_CardOnCard** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="7c970-140">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="7c970-140">WMI does not implement this class.</span></span>

<span data-ttu-id="7c970-141">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7c970-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7c970-142">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7c970-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c970-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c970-143">Requirements</span></span>



| <span data-ttu-id="7c970-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c970-144">Requirement</span></span> | <span data-ttu-id="7c970-145">Value</span><span class="sxs-lookup"><span data-stu-id="7c970-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c970-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c970-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7c970-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c970-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c970-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c970-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7c970-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c970-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c970-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7c970-150">Namespace</span></span><br/>                | <span data-ttu-id="7c970-151">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7c970-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7c970-152">MOF</span><span class="sxs-lookup"><span data-stu-id="7c970-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c970-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c970-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c970-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c970-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c970-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c970-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c970-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c970-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c970-157">**\_Contenedor CIM**</span><span class="sxs-lookup"><span data-stu-id="7c970-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

