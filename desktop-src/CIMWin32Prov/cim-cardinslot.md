---
description: La \_ clase CIM CardInSlot asocia una tarjeta de adaptador con el contenedor en el que se inserta.
ms.assetid: 253fb444-2a9e-4099-a4d5-352b643d8e32
ms.tgt_platform: multiple
title: CIM_CardInSlot (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardInSlot
- CIM_CardInSlot.Dependent
- CIM_CardInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 19c6e7334b8a13854241c3fd2ee41dd7010255b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907345"
---
# <a name="cim_cardinslot-class"></a><span data-ttu-id="b8369-103">\_Clase CardInSlot de CIM</span><span class="sxs-lookup"><span data-stu-id="b8369-103">CIM\_CardInSlot class</span></span>

<span data-ttu-id="b8369-104">La clase **CIM \_ CardInSlot** asocia una tarjeta de adaptador con el contenedor en el que se inserta.</span><span class="sxs-lookup"><span data-stu-id="b8369-104">The **CIM\_CardInSlot** class associates an adapter card with the container into which it is inserted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8369-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="b8369-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b8369-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b8369-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b8369-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b8369-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b8369-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b8369-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8369-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8369-109">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|System Slot|004.4"), UUID("{FAF76B8A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardInSlot : CIM_PackageInSlot
{
  CIM_Card REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="b8369-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8369-110">Members</span></span>

<span data-ttu-id="b8369-111">La clase **CIM \_ CardInSlot** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b8369-111">The **CIM\_CardInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="b8369-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8369-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8369-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8369-113">Properties</span></span>

<span data-ttu-id="b8369-114">La clase **CIM \_ CardInSlot** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b8369-114">The **CIM\_CardInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8369-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b8369-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8369-116">Tipo de datos **: \_ ranura CIM**</span><span class="sxs-lookup"><span data-stu-id="b8369-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="b8369-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8369-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8369-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="b8369-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b8369-119">Una [**\_ ranura CIM**](cim-slot.md) que describe la ranura en la que se inserta la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="b8369-119">A [**CIM\_Slot**](cim-slot.md) that describes the slot into which the card is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="b8369-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="b8369-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8369-121">Tipo de datos **: \_ tarjeta CIM**</span><span class="sxs-lookup"><span data-stu-id="b8369-121">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="b8369-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8369-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8369-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="b8369-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b8369-124">[**\_ Tarjeta CIM**](cim-card.md) que describe la tarjeta de la ranura.</span><span class="sxs-lookup"><span data-stu-id="b8369-124">A [**CIM\_Card**](cim-card.md) that describes the card in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8369-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8369-125">Remarks</span></span>

<span data-ttu-id="b8369-126">La clase **CIM \_ CardInSlot** se deriva de [**\_ PackageInSlot de CIM**](cim-packageinslot.md).</span><span class="sxs-lookup"><span data-stu-id="b8369-126">The **CIM\_CardInSlot** class is derived from [**CIM\_PackageInSlot**](cim-packageinslot.md).</span></span>

<span data-ttu-id="b8369-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="b8369-127">WMI does not implement this class.</span></span>

<span data-ttu-id="b8369-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="b8369-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b8369-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="b8369-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8369-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8369-130">Requirements</span></span>



| <span data-ttu-id="b8369-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8369-131">Requirement</span></span> | <span data-ttu-id="b8369-132">Value</span><span class="sxs-lookup"><span data-stu-id="b8369-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8369-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8369-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b8369-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8369-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8369-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8369-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b8369-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8369-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8369-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8369-137">Namespace</span></span><br/>                | <span data-ttu-id="b8369-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b8369-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8369-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b8369-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8369-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8369-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8369-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8369-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8369-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8369-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8369-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8369-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8369-144">**\_PACKAGEINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="b8369-144">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> </dl>

 

