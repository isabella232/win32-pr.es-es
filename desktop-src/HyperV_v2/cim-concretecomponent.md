---
description: Representa una asociación genérica que se usa para establecer las partes de una relación entre los elementos administrados.
ms.assetid: 9785ea8b-fb76-4ffe-8649-aa2fe1b01d5f
title: CIM_ConcreteComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteComponent
- CIM_ConcreteComponent.GroupComponent
- CIM_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77ee0f33f540bfd215ec10a24c3c574976189d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910401"
---
# <a name="cim_concretecomponent-class"></a><span data-ttu-id="61b0d-103">\_Clase ConcreteComponent de CIM</span><span class="sxs-lookup"><span data-stu-id="61b0d-103">CIM\_ConcreteComponent class</span></span>

<span data-ttu-id="61b0d-104">Representa una asociación genérica que se usa para establecer las partes de una relación entre los elementos administrados.</span><span class="sxs-lookup"><span data-stu-id="61b0d-104">Represents a generic association used to establish the parts of a relationship between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b0d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61b0d-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteComponent : CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="61b0d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="61b0d-106">Members</span></span>

<span data-ttu-id="61b0d-107">La clase **CIM \_ ConcreteComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="61b0d-107">The **CIM\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="61b0d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61b0d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61b0d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61b0d-109">Properties</span></span>

<span data-ttu-id="61b0d-110">La clase **CIM \_ ConcreteComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="61b0d-110">The **CIM\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61b0d-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="61b0d-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61b0d-112">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="61b0d-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="61b0d-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61b0d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61b0d-114">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="61b0d-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="61b0d-115">Elemento primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="61b0d-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="61b0d-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="61b0d-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61b0d-117">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="61b0d-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="61b0d-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61b0d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61b0d-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="61b0d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="61b0d-120">Elemento secundario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="61b0d-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61b0d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61b0d-121">Requirements</span></span>



| <span data-ttu-id="61b0d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="61b0d-122">Requirement</span></span> | <span data-ttu-id="61b0d-123">Value</span><span class="sxs-lookup"><span data-stu-id="61b0d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b0d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61b0d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="61b0d-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61b0d-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="61b0d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61b0d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="61b0d-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61b0d-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="61b0d-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="61b0d-128">Namespace</span></span><br/>                | <span data-ttu-id="61b0d-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="61b0d-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="61b0d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="61b0d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61b0d-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61b0d-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61b0d-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61b0d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61b0d-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61b0d-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61b0d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="61b0d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b0d-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="61b0d-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

