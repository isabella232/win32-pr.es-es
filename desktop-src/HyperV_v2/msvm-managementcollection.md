---
description: Representa una colección de otras colecciones.
ms.assetid: 1f7f5517-55d9-44a3-b0ca-444a9d7d5941
title: Msvm_ManagementCollection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ManagementCollection
- Msvm_ManagementCollection.CollectionID
- Msvm_ManagementCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2d3499bb161495152b6de4b8aebd7c64d041d069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688569"
---
# <a name="msvm_managementcollection-class"></a><span data-ttu-id="f0a59-103">MSVM \_ ManagementCollection (clase)</span><span class="sxs-lookup"><span data-stu-id="f0a59-103">Msvm\_ManagementCollection class</span></span>

<span data-ttu-id="f0a59-104">Representa una colección de otras colecciones.</span><span class="sxs-lookup"><span data-stu-id="f0a59-104">Represents a collection of other collections.</span></span>

<span data-ttu-id="f0a59-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f0a59-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a59-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0a59-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ManagementCollection : CIM_CollectionOfMSEs
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="f0a59-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0a59-107">Members</span></span>

<span data-ttu-id="f0a59-108">La clase **MSVM \_ ManagementCollection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f0a59-108">The **Msvm\_ManagementCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="f0a59-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0a59-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0a59-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0a59-110">Properties</span></span>

<span data-ttu-id="f0a59-111">La clase **MSVM \_ ManagementCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f0a59-111">The **Msvm\_ManagementCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0a59-112">**Recopilación**</span><span class="sxs-lookup"><span data-stu-id="f0a59-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a59-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a59-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a59-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a59-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a59-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f0a59-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f0a59-116">Identificación única del objeto de colección.</span><span class="sxs-lookup"><span data-stu-id="f0a59-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="f0a59-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f0a59-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a59-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a59-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a59-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a59-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a59-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="f0a59-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="f0a59-121">Nombre definido por el usuario para la colección.</span><span class="sxs-lookup"><span data-stu-id="f0a59-121">An user-defined name for the collection.</span></span> <span data-ttu-id="f0a59-122">Tenga en cuenta que no se garantiza que sea único.</span><span class="sxs-lookup"><span data-stu-id="f0a59-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0a59-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0a59-123">Requirements</span></span>



| <span data-ttu-id="f0a59-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0a59-124">Requirement</span></span> | <span data-ttu-id="f0a59-125">Value</span><span class="sxs-lookup"><span data-stu-id="f0a59-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a59-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0a59-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a59-127">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0a59-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f0a59-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0a59-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a59-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f0a59-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f0a59-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0a59-130">Namespace</span></span><br/>                | <span data-ttu-id="f0a59-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f0a59-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f0a59-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f0a59-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0a59-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0a59-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0a59-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0a59-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0a59-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0a59-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f0a59-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0a59-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a59-137">**CollectionOfMSEs de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f0a59-137">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

