---
description: La \_ clase CIM StatisticalInformation es una clase raíz para la colección arbitraria de datos estadísticos o métricas aplicables a uno o varios elementos del sistema administrados.
ms.assetid: ecc3b310-c553-416b-b4e3-705965557945
ms.tgt_platform: multiple
title: CIM_StatisticalInformation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StatisticalInformation
- CIM_StatisticalInformation.Caption
- CIM_StatisticalInformation.Description
- CIM_StatisticalInformation.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6eda3e2463c880a58c4e23a6d09dcab99417ead
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907495"
---
# <a name="cim_statisticalinformation-class"></a><span data-ttu-id="44a89-103">\_Clase StatisticalInformation de CIM</span><span class="sxs-lookup"><span data-stu-id="44a89-103">CIM\_StatisticalInformation class</span></span>

<span data-ttu-id="44a89-104">La clase **CIM \_ StatisticalInformation** es una clase raíz para la colección arbitraria de datos estadísticos o métricas aplicables a uno o varios elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="44a89-104">The **CIM\_StatisticalInformation** class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44a89-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="44a89-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="44a89-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="44a89-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="44a89-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="44a89-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="44a89-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="44a89-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a89-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44a89-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A1-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_StatisticalInformation
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="44a89-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="44a89-110">Members</span></span>

<span data-ttu-id="44a89-111">La clase **CIM \_ StatisticalInformation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="44a89-111">The **CIM\_StatisticalInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="44a89-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44a89-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44a89-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44a89-113">Properties</span></span>

<span data-ttu-id="44a89-114">La clase **CIM \_ StatisticalInformation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="44a89-114">The **CIM\_StatisticalInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44a89-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="44a89-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a89-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="44a89-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44a89-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44a89-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a89-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="44a89-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="44a89-119">Breve descripción textual de la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="44a89-119">Short textual description for the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="44a89-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44a89-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a89-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="44a89-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44a89-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44a89-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44a89-123">Descripción textual de la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="44a89-123">Textual description of the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="44a89-124">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="44a89-124">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44a89-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="44a89-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44a89-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44a89-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44a89-127">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="44a89-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="44a89-128">Etiqueta por la que se conoce la estadística o la métrica.</span><span class="sxs-lookup"><span data-stu-id="44a89-128">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="44a89-129">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="44a89-129">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44a89-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44a89-130">Remarks</span></span>

<span data-ttu-id="44a89-131">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="44a89-131">WMI does not implement this class.</span></span> <span data-ttu-id="44a89-132">Para las clases WMI derivadas de **CIM \_ StatisticalInformation**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="44a89-132">For WMI classes derived from **CIM\_StatisticalInformation**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="44a89-133">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="44a89-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="44a89-134">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="44a89-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="44a89-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44a89-135">Requirements</span></span>



| <span data-ttu-id="44a89-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="44a89-136">Requirement</span></span> | <span data-ttu-id="44a89-137">Value</span><span class="sxs-lookup"><span data-stu-id="44a89-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44a89-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44a89-138">Minimum supported client</span></span><br/> | <span data-ttu-id="44a89-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44a89-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44a89-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44a89-140">Minimum supported server</span></span><br/> | <span data-ttu-id="44a89-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44a89-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44a89-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="44a89-142">Namespace</span></span><br/>                | <span data-ttu-id="44a89-143">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="44a89-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44a89-144">MOF</span><span class="sxs-lookup"><span data-stu-id="44a89-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44a89-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44a89-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44a89-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44a89-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44a89-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44a89-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

