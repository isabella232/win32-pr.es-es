---
description: 'Msvm_CollectedCollections clase : asocia Msvm \_ VirtualSystemCollection a los objetos ComputerSystem de Msvm \_ contenidos.'
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Msvm_CollectedCollections clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 83719d364fac22923d68206c8cfe7d37adad5edb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112133"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="7982f-103">Clase Msvm \_ CollectedCollections</span><span class="sxs-lookup"><span data-stu-id="7982f-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="7982f-104">Asocia [**Msvm \_ VirtualSystemCollection a**](msvm-virtualsystemcollection.md) los objetos [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) contenidos.</span><span class="sxs-lookup"><span data-stu-id="7982f-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="7982f-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7982f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7982f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7982f-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="7982f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7982f-107">Members</span></span>

<span data-ttu-id="7982f-108">La **clase \_ CollectedCollections de Msvm** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7982f-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="7982f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7982f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7982f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7982f-110">Properties</span></span>

<span data-ttu-id="7982f-111">La **clase \_ CollectedCollections de Msvm** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7982f-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7982f-112">**Colección**</span><span class="sxs-lookup"><span data-stu-id="7982f-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7982f-113">Tipo de datos: **Msvm \_ ManagementCollection**</span><span class="sxs-lookup"><span data-stu-id="7982f-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="7982f-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7982f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7982f-115">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="7982f-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="7982f-116">Una [**agrupación \_ Msvm ManagementCollection**](msvm-managementcollection.md) o un objeto "bag" que representa la colección.</span><span class="sxs-lookup"><span data-stu-id="7982f-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="7982f-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="7982f-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7982f-118">Tipo de datos: **\_ Cim CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="7982f-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="7982f-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7982f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7982f-120">Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="7982f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="7982f-121">Colección [**\_ CIMOfMSE**](cim-collectionofmses.md) que contiene los miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="7982f-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7982f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7982f-122">Requirements</span></span>



| <span data-ttu-id="7982f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7982f-123">Requirement</span></span> | <span data-ttu-id="7982f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7982f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7982f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7982f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7982f-126">Windows 10 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="7982f-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7982f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7982f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7982f-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7982f-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7982f-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7982f-129">Namespace</span></span><br/>                | <span data-ttu-id="7982f-130">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="7982f-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7982f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="7982f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7982f-132"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="7982f-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7982f-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7982f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7982f-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7982f-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7982f-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7982f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7982f-136">**CIM \_ CollectedMSEs**</span><span class="sxs-lookup"><span data-stu-id="7982f-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

