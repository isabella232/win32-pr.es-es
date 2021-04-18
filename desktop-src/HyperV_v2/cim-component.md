---
description: Representa una asociación genérica entre un elemento administrado primario y un elemento administrado secundario en el que el elemento secundario representa un componente o parte del elemento primario.
ms.assetid: b5cef452-2d00-483c-8e70-f804f1e3536b
title: CIM_Component (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56ff83a4da51ba18205a8d8ab5e6e57ea1a7794b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687713"
---
# <a name="cim_component-class-hyper-v-management"></a><span data-ttu-id="a9a6a-103">CIM_Component (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="a9a6a-103">CIM_Component class (Hyper-V management)</span></span>

<span data-ttu-id="a9a6a-104">Representa una asociación genérica entre un elemento administrado primario y un elemento administrado secundario en el que el elemento secundario representa un componente o parte del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="a9a6a-104">Represents a generic association between a parent managed element and a child managed element where the child represents a component or part of the parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a6a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9a6a-105">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, Version("2.7.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a9a6a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a9a6a-106">Members</span></span>

<span data-ttu-id="a9a6a-107">La clase de **\_ componentes CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a9a6a-107">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="a9a6a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9a6a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9a6a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9a6a-109">Properties</span></span>

<span data-ttu-id="a9a6a-110">La clase de **\_ componentes CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a9a6a-110">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9a6a-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a9a6a-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9a6a-112">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="a9a6a-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="a9a6a-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9a6a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9a6a-114">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a9a6a-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a9a6a-115">Elemento primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="a9a6a-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="a9a6a-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a9a6a-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9a6a-117">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="a9a6a-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="a9a6a-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9a6a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9a6a-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a9a6a-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a9a6a-120">Elemento secundario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="a9a6a-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9a6a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9a6a-121">Requirements</span></span>



| <span data-ttu-id="a9a6a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9a6a-122">Requirement</span></span> | <span data-ttu-id="a9a6a-123">Value</span><span class="sxs-lookup"><span data-stu-id="a9a6a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a6a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9a6a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a6a-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a9a6a-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a9a6a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9a6a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a6a-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9a6a-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a9a6a-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9a6a-128">Namespace</span></span><br/>                | <span data-ttu-id="a9a6a-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a9a6a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a9a6a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a9a6a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9a6a-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9a6a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9a6a-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a9a6a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9a6a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9a6a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

