---
description: Asocia el \_ ReferencePointCollection MSVM a los objetos MSVM \_ VirtualSystemReferencePoint incluidos.
ms.assetid: 826125c3-0a89-4573-ac28-88588eac248d
title: Msvm_CollectedReferencePoints (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedReferencePoints
- Msvm_CollectedReferencePoints.Collection
- Msvm_CollectedReferencePoints.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4891d4ec4c613c92c3b5d5a090f2683bfc77dc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810916"
---
# <a name="msvm_collectedreferencepoints-class"></a><span data-ttu-id="5e875-103">MSVM \_ CollectedReferencePoints (clase)</span><span class="sxs-lookup"><span data-stu-id="5e875-103">Msvm\_CollectedReferencePoints class</span></span>

<span data-ttu-id="5e875-104">Asocia el [**\_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) a los objetos [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) incluidos.</span><span class="sxs-lookup"><span data-stu-id="5e875-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the contained [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) objects.</span></span>

<span data-ttu-id="5e875-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5e875-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e875-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e875-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedReferencePoints : CIM_CollectedMSEs
{
  Msvm_ReferencePointCollection    REF Collection;
  Msvm_VirtualSystemReferencePoint REF Member;
};
```

## <a name="members"></a><span data-ttu-id="5e875-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e875-107">Members</span></span>

<span data-ttu-id="5e875-108">La clase **MSVM \_ CollectedReferencePoints** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5e875-108">The **Msvm\_CollectedReferencePoints** class has these types of members:</span></span>

-   [<span data-ttu-id="5e875-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e875-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e875-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e875-110">Properties</span></span>

<span data-ttu-id="5e875-111">La clase **MSVM \_ CollectedReferencePoints** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e875-111">The **Msvm\_CollectedReferencePoints** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e875-112">**Colección**</span><span class="sxs-lookup"><span data-stu-id="5e875-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e875-113">Tipo de datos: **MSVM \_ ReferencePointCollection**</span><span class="sxs-lookup"><span data-stu-id="5e875-113">Data type: **Msvm\_ReferencePointCollection**</span></span>
</dt> <dt>

<span data-ttu-id="5e875-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e875-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e875-115">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="5e875-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="5e875-116">Objeto de agrupación o contenedor de [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md) que representa la colección.</span><span class="sxs-lookup"><span data-stu-id="5e875-116">An [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="5e875-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="5e875-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e875-118">Tipo de datos: **MSVM \_ VirtualSystemReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="5e875-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="5e875-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e875-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e875-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("miembro")</span><span class="sxs-lookup"><span data-stu-id="5e875-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="5e875-121">[**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que contiene los miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="5e875-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e875-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e875-122">Requirements</span></span>



| <span data-ttu-id="5e875-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e875-123">Requirement</span></span> | <span data-ttu-id="5e875-124">Value</span><span class="sxs-lookup"><span data-stu-id="5e875-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e875-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e875-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5e875-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e875-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5e875-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e875-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5e875-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5e875-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5e875-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e875-129">Namespace</span></span><br/>                | <span data-ttu-id="5e875-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5e875-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5e875-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5e875-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e875-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e875-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e875-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e875-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e875-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e875-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e875-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e875-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e875-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="5e875-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

