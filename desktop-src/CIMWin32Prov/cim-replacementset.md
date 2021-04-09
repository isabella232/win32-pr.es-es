---
description: La \_ clase CIM ReplacementSet agrega elementos físicos que se deben reemplazar juntos.
ms.assetid: db55ae2d-49b3-4cc9-95ee-1e757f58a427
ms.tgt_platform: multiple
title: CIM_ReplacementSet (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReplacementSet
- CIM_ReplacementSet.Description
- CIM_ReplacementSet.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: defc63628e494465d7a31d8adcea758e538c4c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152872"
---
# <a name="cim_replacementset-class"></a><span data-ttu-id="17315-103">\_Clase ReplacementSet de CIM</span><span class="sxs-lookup"><span data-stu-id="17315-103">CIM\_ReplacementSet class</span></span>

<span data-ttu-id="17315-104">La clase **CIM \_ ReplacementSet** agrega elementos físicos que se deben reemplazar juntos.</span><span class="sxs-lookup"><span data-stu-id="17315-104">The **CIM\_ReplacementSet** class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="17315-105">Por ejemplo, al reemplazar una tarjeta de memoria, los chips de memoria de componente también se pueden quitar y reemplazar.</span><span class="sxs-lookup"><span data-stu-id="17315-105">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="17315-106">O bien, esta asociación se puede usar para reemplazar o actualizar un conjunto de chips de memoria.</span><span class="sxs-lookup"><span data-stu-id="17315-106">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17315-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="17315-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="17315-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="17315-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="17315-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="17315-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="17315-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="17315-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17315-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17315-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ReplacementSet
{
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="17315-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="17315-112">Members</span></span>

<span data-ttu-id="17315-113">La clase **CIM \_ ReplacementSet** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="17315-113">The **CIM\_ReplacementSet** class has these types of members:</span></span>

-   [<span data-ttu-id="17315-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17315-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17315-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17315-115">Properties</span></span>

<span data-ttu-id="17315-116">La clase **CIM \_ ReplacementSet** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="17315-116">The **CIM\_ReplacementSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17315-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17315-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17315-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17315-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17315-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17315-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17315-120">Cadena de forma libre que especifica información relacionada con esta clase.</span><span class="sxs-lookup"><span data-stu-id="17315-120">Free-form string that specifies information related to this class.</span></span> <span data-ttu-id="17315-121">En esta propiedad se puede incluir el propósito del conjunto o la información relacionada con la forma en que se reemplazan los elementos de componente.</span><span class="sxs-lookup"><span data-stu-id="17315-121">The purpose of the set, or information related to how the component elements are replaced, can be included in this property.</span></span>

</dd> <dt>

<span data-ttu-id="17315-122">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="17315-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17315-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="17315-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17315-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17315-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17315-125">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17315-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17315-126">Cadena de forma libre que define una etiqueta para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="17315-126">Free-form string that defines a label for this property.</span></span> <span data-ttu-id="17315-127">Esta propiedad es la clave para el objeto.</span><span class="sxs-lookup"><span data-stu-id="17315-127">This property is the key for the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17315-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17315-128">Remarks</span></span>

<span data-ttu-id="17315-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="17315-129">WMI does not implement this class.</span></span>

<span data-ttu-id="17315-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="17315-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="17315-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="17315-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="17315-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17315-132">Requirements</span></span>



| <span data-ttu-id="17315-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="17315-133">Requirement</span></span> | <span data-ttu-id="17315-134">Value</span><span class="sxs-lookup"><span data-stu-id="17315-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17315-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17315-135">Minimum supported client</span></span><br/> | <span data-ttu-id="17315-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17315-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17315-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17315-137">Minimum supported server</span></span><br/> | <span data-ttu-id="17315-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17315-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17315-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17315-139">Namespace</span></span><br/>                | <span data-ttu-id="17315-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="17315-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17315-141">MOF</span><span class="sxs-lookup"><span data-stu-id="17315-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17315-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17315-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17315-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17315-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17315-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17315-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

