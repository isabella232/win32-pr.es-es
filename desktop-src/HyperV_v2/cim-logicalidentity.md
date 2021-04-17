---
description: Representa una asociación genérica entre dos elementos administrados que representan distintos aspectos de la misma entidad subyacente.
ms.assetid: 28d153de-ce9c-4cd3-8995-0d959846be4d
title: CIM_LogicalIdentity (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SystemElement
- CIM_LogicalIdentity.SameElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 71382910dc195c0fa6ef2456e1811d66d90a41e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666237"
---
# <a name="cim_logicalidentity-class-hyper-v-management"></a><span data-ttu-id="1a406-103">CIM_LogicalIdentity (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="1a406-103">CIM_LogicalIdentity class (Hyper-V management)</span></span>

<span data-ttu-id="1a406-104">Representa una asociación genérica entre dos elementos administrados que representan distintos aspectos de la misma entidad subyacente.</span><span class="sxs-lookup"><span data-stu-id="1a406-104">Represents a generic association between two managed elements that represent different aspects of the same underlying entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a406-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a406-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_LogicalIdentity
{
  CIM_ManagedElement REF SystemElement;
  CIM_ManagedElement REF SameElement;
};
```

## <a name="members"></a><span data-ttu-id="1a406-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1a406-106">Members</span></span>

<span data-ttu-id="1a406-107">La clase **CIM \_ LogicalIdentity** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1a406-107">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="1a406-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a406-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a406-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a406-109">Properties</span></span>

<span data-ttu-id="1a406-110">La clase **CIM \_ LogicalIdentity** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a406-110">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a406-111">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="1a406-111">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a406-112">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="1a406-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="1a406-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a406-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a406-114">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a406-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1a406-115">Segundo aspecto de la asociación.</span><span class="sxs-lookup"><span data-stu-id="1a406-115">The second aspect in the association.</span></span>

</dd> <dt>

<span data-ttu-id="1a406-116">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="1a406-116">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a406-117">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="1a406-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="1a406-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a406-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a406-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a406-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1a406-120">Primer aspecto de la asociación.</span><span class="sxs-lookup"><span data-stu-id="1a406-120">The first aspect in the association.</span></span> <span data-ttu-id="1a406-121">El uso del sistema en el nombre de la propiedad no limita el ámbito de la asociación.</span><span class="sxs-lookup"><span data-stu-id="1a406-121">The use of System in the property name does not limit the scope of the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a406-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a406-122">Requirements</span></span>



| <span data-ttu-id="1a406-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a406-123">Requirement</span></span> | <span data-ttu-id="1a406-124">Value</span><span class="sxs-lookup"><span data-stu-id="1a406-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a406-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a406-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1a406-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1a406-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1a406-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a406-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1a406-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1a406-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1a406-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a406-129">Namespace</span></span><br/>                | <span data-ttu-id="1a406-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1a406-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1a406-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1a406-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a406-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a406-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a406-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a406-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a406-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a406-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

