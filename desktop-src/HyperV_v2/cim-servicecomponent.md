---
description: Representa una asociación en la que un servicio es un componente de un servicio primario, que en conjunto, forman un servicio de nivel superior.
ms.assetid: c629d59d-d9d3-4019-a378-cd1d4d31a5d9
title: CIM_ServiceComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceComponent
- CIM_ServiceComponent.GroupComponent
- CIM_ServiceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2bfb9943685f8568674e696a76df94fda502fcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275554"
---
# <a name="cim_servicecomponent-class"></a><span data-ttu-id="d18e3-103">\_Clase ServiceComponent de CIM</span><span class="sxs-lookup"><span data-stu-id="d18e3-103">CIM\_ServiceComponent class</span></span>

<span data-ttu-id="d18e3-104">Representa una asociación en la que un servicio es un componente de un servicio primario, que en conjunto, forman un servicio de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="d18e3-104">Represents an association in which a service is a component of a parent service, which together, form a higher-level service.</span></span>

## <a name="syntax"></a><span data-ttu-id="d18e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d18e3-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceComponent : CIM_Component
{
  CIM_Service REF GroupComponent;
  CIM_Service REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d18e3-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d18e3-106">Members</span></span>

<span data-ttu-id="d18e3-107">La clase **CIM \_ ServiceComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d18e3-107">The **CIM\_ServiceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="d18e3-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d18e3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d18e3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d18e3-109">Properties</span></span>

<span data-ttu-id="d18e3-110">La clase **CIM \_ ServiceComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d18e3-110">The **CIM\_ServiceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d18e3-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d18e3-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18e3-112">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="d18e3-112">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="d18e3-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d18e3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d18e3-114">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="d18e3-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d18e3-115">El servicio primario.</span><span class="sxs-lookup"><span data-stu-id="d18e3-115">The parent service.</span></span>

</dd> <dt>

<span data-ttu-id="d18e3-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d18e3-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18e3-117">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="d18e3-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="d18e3-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d18e3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d18e3-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="d18e3-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d18e3-120">Servicio de componentes.</span><span class="sxs-lookup"><span data-stu-id="d18e3-120">The component service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d18e3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d18e3-121">Requirements</span></span>



| <span data-ttu-id="d18e3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d18e3-122">Requirement</span></span> | <span data-ttu-id="d18e3-123">Value</span><span class="sxs-lookup"><span data-stu-id="d18e3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d18e3-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d18e3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d18e3-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d18e3-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d18e3-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d18e3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d18e3-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d18e3-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d18e3-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d18e3-128">Namespace</span></span><br/>                | <span data-ttu-id="d18e3-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d18e3-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d18e3-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d18e3-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d18e3-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d18e3-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d18e3-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d18e3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d18e3-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d18e3-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d18e3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d18e3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18e3-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="d18e3-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

