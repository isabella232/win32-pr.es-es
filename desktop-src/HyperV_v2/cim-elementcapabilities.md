---
description: Representa una asociación entre un elemento administrado y sus capacidades.
ms.assetid: 0e080042-4a56-40b7-acc5-cf69eb2a0604
title: CIM_ElementCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapabilities
- CIM_ElementCapabilities.ManagedElement
- CIM_ElementCapabilities.Capabilities
- CIM_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c705d0bb4743d4919ca840f51b3324510558078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687033"
---
# <a name="cim_elementcapabilities-class"></a><span data-ttu-id="2d335-103">\_Clase ElementCapabilities de CIM</span><span class="sxs-lookup"><span data-stu-id="2d335-103">CIM\_ElementCapabilities class</span></span>

<span data-ttu-id="2d335-104">Representa una asociación entre un elemento administrado y sus capacidades.</span><span class="sxs-lookup"><span data-stu-id="2d335-104">Represents an association between a managed element and its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d335-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d335-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="2d335-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d335-106">Members</span></span>

<span data-ttu-id="2d335-107">La clase **CIM \_ ElementCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2d335-107">The **CIM\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="2d335-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d335-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d335-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2d335-109">Properties</span></span>

<span data-ttu-id="2d335-110">La clase **CIM \_ ElementCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2d335-110">The **CIM\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d335-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="2d335-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d335-112">Tipo de datos **: \_ capacidades de CIM**</span><span class="sxs-lookup"><span data-stu-id="2d335-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="2d335-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d335-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d335-114">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2d335-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2d335-115">Las capacidades asociadas al elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="2d335-115">The capabilities associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="2d335-116">**Características**</span><span class="sxs-lookup"><span data-stu-id="2d335-116">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d335-117">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d335-117">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2d335-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d335-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d335-119">Un conjunto de información descriptiva sobre las capacidades.</span><span class="sxs-lookup"><span data-stu-id="2d335-119">A set of descriptive information about the capabilities.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="2d335-120">**Predeterminado** (2)</span><span class="sxs-lookup"><span data-stu-id="2d335-120">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>

<span data-ttu-id="2d335-121">**Actual** (3)</span><span class="sxs-lookup"><span data-stu-id="2d335-121">**Current** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2d335-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2d335-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="2d335-123">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="2d335-123">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2d335-124">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="2d335-124">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d335-125">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="2d335-125">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="2d335-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2d335-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d335-127">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="2d335-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2d335-128">Elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="2d335-128">The managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d335-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d335-129">Requirements</span></span>



| <span data-ttu-id="2d335-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d335-130">Requirement</span></span> | <span data-ttu-id="2d335-131">Value</span><span class="sxs-lookup"><span data-stu-id="2d335-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d335-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d335-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2d335-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2d335-133">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2d335-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d335-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2d335-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d335-135">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2d335-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2d335-136">Namespace</span></span><br/>                | <span data-ttu-id="2d335-137">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2d335-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2d335-138">MOF</span><span class="sxs-lookup"><span data-stu-id="2d335-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d335-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d335-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d335-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d335-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d335-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d335-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

