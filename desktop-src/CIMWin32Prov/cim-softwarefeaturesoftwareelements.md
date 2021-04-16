---
description: La \_ Asociación SoftwareFeatureSoftwareElements de CIM identifica los elementos de software que componen una característica de software específica.
ms.assetid: 933586c5-b85e-4136-b557-5151a48abc32
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureSoftwareElements (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSoftwareElements
- CIM_SoftwareFeatureSoftwareElements.PartComponent
- CIM_SoftwareFeatureSoftwareElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71712ebb3f8bf2ab2067325f16cf31af7fb1dc38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659368"
---
# <a name="cim_softwarefeaturesoftwareelements-class"></a><span data-ttu-id="3b44b-103">\_Clase SoftwareFeatureSoftwareElements de CIM</span><span class="sxs-lookup"><span data-stu-id="3b44b-103">CIM\_SoftwareFeatureSoftwareElements class</span></span>

<span data-ttu-id="3b44b-104">La **Asociación \_ SoftwareFeatureSoftwareElements de CIM** identifica los elementos de software que componen una característica de software específica.</span><span class="sxs-lookup"><span data-stu-id="3b44b-104">The **CIM\_SoftwareFeatureSoftwareElements** association identifies the software elements that make up a specific software feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b44b-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="3b44b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3b44b-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3b44b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3b44b-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3b44b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3b44b-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3b44b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b44b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b44b-109">Syntax</span></span>

``` syntax
[UUID("{A91081E2-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSoftwareElements : CIM_Component
{
  CIM_SoftwareElement REF PartComponent;
  CIM_SoftwareFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="3b44b-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b44b-110">Members</span></span>

<span data-ttu-id="3b44b-111">La clase **CIM \_ SoftwareFeatureSoftwareElements** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3b44b-111">The **CIM\_SoftwareFeatureSoftwareElements** class has these types of members:</span></span>

-   [<span data-ttu-id="3b44b-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b44b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b44b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b44b-113">Properties</span></span>

<span data-ttu-id="3b44b-114">La clase **CIM \_ SoftwareFeatureSoftwareElements** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3b44b-114">The **CIM\_SoftwareFeatureSoftwareElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b44b-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3b44b-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b44b-116">Tipo de datos: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="3b44b-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="3b44b-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b44b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b44b-118">Calificadores: [ **agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3b44b-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3b44b-119">Componente de grupo.</span><span class="sxs-lookup"><span data-stu-id="3b44b-119">The group component.</span></span>

<span data-ttu-id="3b44b-120">Esta propiedad se hereda del [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="3b44b-120">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b44b-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3b44b-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b44b-122">Tipo de datos: **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="3b44b-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="3b44b-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b44b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b44b-124">Componente del elemento.</span><span class="sxs-lookup"><span data-stu-id="3b44b-124">The part component.</span></span>

<span data-ttu-id="3b44b-125">Esta propiedad se hereda del [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="3b44b-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b44b-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b44b-126">Remarks</span></span>

<span data-ttu-id="3b44b-127">La **Asociación \_ SoftwareFeatureSoftwareElements de CIM** se deriva [**del \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="3b44b-127">The **CIM\_SoftwareFeatureSoftwareElements** association is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="3b44b-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="3b44b-128">WMI does not implement this class.</span></span> <span data-ttu-id="3b44b-129">Para las clases WMI derivadas de **CIM \_ SoftwareFeatureSoftwareElements**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3b44b-129">For WMI classes derived from **CIM\_SoftwareFeatureSoftwareElements**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3b44b-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="3b44b-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3b44b-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="3b44b-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b44b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b44b-132">Requirements</span></span>



| <span data-ttu-id="3b44b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b44b-133">Requirement</span></span> | <span data-ttu-id="3b44b-134">Value</span><span class="sxs-lookup"><span data-stu-id="3b44b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b44b-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b44b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3b44b-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b44b-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b44b-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b44b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3b44b-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b44b-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b44b-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b44b-139">Namespace</span></span><br/>                | <span data-ttu-id="3b44b-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3b44b-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b44b-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3b44b-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b44b-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b44b-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b44b-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b44b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b44b-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b44b-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b44b-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b44b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b44b-146">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="3b44b-146">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

