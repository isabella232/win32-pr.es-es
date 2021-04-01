---
description: La \_ relación DependencyContext de CIM asocia una \_ clase de dependencia CIM a uno o más objetos de configuración de CIM \_ . Por ejemplo, las dependencias de un equipo pueden cambiar en función de la red a la que está conectado el sistema.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: CIM_DependencyContext (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69319a4f4d228d484da62411060ae3fead90bb79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907301"
---
# <a name="cim_dependencycontext-class"></a><span data-ttu-id="50db6-104">\_Clase DependencyContext de CIM</span><span class="sxs-lookup"><span data-stu-id="50db6-104">CIM\_DependencyContext class</span></span>

<span data-ttu-id="50db6-105">La **relación \_ DependencyContext de CIM** asocia una clase de [**\_ dependencia CIM**](cim-dependency.md) a uno o más objetos de [**\_ configuración de CIM**](cim-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="50db6-105">The **CIM\_DependencyContext** relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="50db6-106">Por ejemplo, las dependencias de un equipo pueden cambiar en función de la red a la que está conectado el sistema.</span><span class="sxs-lookup"><span data-stu-id="50db6-106">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50db6-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="50db6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="50db6-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="50db6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="50db6-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="50db6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="50db6-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="50db6-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="50db6-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50db6-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a><span data-ttu-id="50db6-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="50db6-112">Members</span></span>

<span data-ttu-id="50db6-113">La clase **CIM \_ DependencyContext** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="50db6-113">The **CIM\_DependencyContext** class has these types of members:</span></span>

-   [<span data-ttu-id="50db6-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50db6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50db6-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50db6-115">Properties</span></span>

<span data-ttu-id="50db6-116">La clase **CIM \_ DependencyContext** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="50db6-116">The **CIM\_DependencyContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50db6-117">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="50db6-117">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50db6-118">Tipo de datos **: \_ configuración de CIM**</span><span class="sxs-lookup"><span data-stu-id="50db6-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="50db6-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="50db6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50db6-120">Calificadores: [ **agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="50db6-120">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="50db6-121">Referencia al objeto de configuración que agrega la dependencia.</span><span class="sxs-lookup"><span data-stu-id="50db6-121">Reference to the configuration object that aggregates the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="50db6-122">**Dependencia**</span><span class="sxs-lookup"><span data-stu-id="50db6-122">**Dependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50db6-123">Tipo de datos **: \_ dependencia CIM**</span><span class="sxs-lookup"><span data-stu-id="50db6-123">Data type: **CIM\_Dependency**</span></span>
</dt> <dt>

<span data-ttu-id="50db6-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="50db6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50db6-125">Referencia a una dependencia agregada.</span><span class="sxs-lookup"><span data-stu-id="50db6-125">Reference to an aggregated dependency.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50db6-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50db6-126">Remarks</span></span>

<span data-ttu-id="50db6-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="50db6-127">WMI does not implement this class.</span></span>

<span data-ttu-id="50db6-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="50db6-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="50db6-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="50db6-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="50db6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50db6-130">Requirements</span></span>



| <span data-ttu-id="50db6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="50db6-131">Requirement</span></span> | <span data-ttu-id="50db6-132">Value</span><span class="sxs-lookup"><span data-stu-id="50db6-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50db6-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50db6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="50db6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50db6-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50db6-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50db6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="50db6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50db6-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50db6-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="50db6-137">Namespace</span></span><br/>                | <span data-ttu-id="50db6-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="50db6-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="50db6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="50db6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50db6-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50db6-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="50db6-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="50db6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50db6-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50db6-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

