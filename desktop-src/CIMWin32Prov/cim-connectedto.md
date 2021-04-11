---
description: La clase de CIM \_ Connected representa una asociación que indica que dos o más conectores físicos están conectados.
ms.assetid: fedd9227-8a3b-461a-995b-08cbceb81181
ms.tgt_platform: multiple
title: CIM_ConnectedTo (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectedTo
- CIM_ConnectedTo.Dependent
- CIM_ConnectedTo.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f1a507cb529f2040607024e1a6167ddcd5dc7c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080226"
---
# <a name="cim_connectedto-class"></a><span data-ttu-id="01803-103">\_Clase Connected de CIM</span><span class="sxs-lookup"><span data-stu-id="01803-103">CIM\_ConnectedTo class</span></span>

<span data-ttu-id="01803-104">La clase de **CIM \_ Connected** representa una asociación que indica que dos o más conectores físicos están conectados.</span><span class="sxs-lookup"><span data-stu-id="01803-104">The **CIM\_ConnectedTo** class represents an association that indicates that two or more physical connectors are connected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01803-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="01803-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="01803-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="01803-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="01803-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="01803-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="01803-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="01803-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01803-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01803-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B85-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectedTo : CIM_Dependency
{
  CIM_PhysicalConnector REF Dependent;
  CIM_PhysicalConnector REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="01803-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="01803-110">Members</span></span>

<span data-ttu-id="01803-111">La **clase \_ Connected de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="01803-111">The **CIM\_ConnectedTo** class has these types of members:</span></span>

-   [<span data-ttu-id="01803-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01803-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01803-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01803-113">Properties</span></span>

<span data-ttu-id="01803-114">La **clase \_ conectada de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="01803-114">The **CIM\_ConnectedTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01803-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="01803-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01803-116">Tipo de datos: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="01803-116">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="01803-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01803-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01803-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="01803-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="01803-119">Un [**\_ PhysicalConnector de CIM**](cim-physicalconnector.md) que representa un conector físico que actúa como un extremo de la conexión.</span><span class="sxs-lookup"><span data-stu-id="01803-119">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents a physical connector that serves as one end of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="01803-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="01803-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01803-121">Tipo de datos: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="01803-121">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="01803-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01803-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01803-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="01803-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="01803-124">Un [**\_ PhysicalConnector de CIM**](cim-physicalconnector.md) que representa otro conector físico que actúa como el otro extremo de la conexión.</span><span class="sxs-lookup"><span data-stu-id="01803-124">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents another physical connector that serves as the other end of the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01803-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01803-125">Remarks</span></span>

<span data-ttu-id="01803-126">La **clase \_ conectada de CIM** se hereda de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="01803-126">The **CIM\_ConnectedTo** class is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="01803-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="01803-127">WMI does not implement this class.</span></span>

<span data-ttu-id="01803-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="01803-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01803-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="01803-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01803-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01803-130">Requirements</span></span>



| <span data-ttu-id="01803-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="01803-131">Requirement</span></span> | <span data-ttu-id="01803-132">Value</span><span class="sxs-lookup"><span data-stu-id="01803-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01803-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01803-133">Minimum supported client</span></span><br/> | <span data-ttu-id="01803-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01803-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01803-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01803-135">Minimum supported server</span></span><br/> | <span data-ttu-id="01803-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01803-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01803-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01803-137">Namespace</span></span><br/>                | <span data-ttu-id="01803-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="01803-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01803-139">MOF</span><span class="sxs-lookup"><span data-stu-id="01803-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01803-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01803-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01803-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01803-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01803-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01803-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01803-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="01803-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01803-144">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="01803-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

