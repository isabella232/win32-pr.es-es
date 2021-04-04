---
description: Clase abstracta para las subclases que representan una colección de \_ objetos ManagedSystemElement de CIM. Estas colecciones permiten agrupar los elementos del sistema administrados con fines de identificación y simplificar la Asociación de configuraciones y configuraciones.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: CIM_CollectionOfMSEs (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e467e775c78364718f25cc732d6689d9fb2b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908741"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a><span data-ttu-id="f6822-104">CIM_CollectionOfMSEs (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="f6822-104">CIM_CollectionOfMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="f6822-105">Clase abstracta para las subclases que representan una colección de [**objetos \_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="f6822-105">An abstract class for subclasses that represent a collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span> <span data-ttu-id="f6822-106">Estas colecciones permiten agrupar los elementos del sistema administrados con fines de identificación y simplificar la Asociación de configuraciones y configuraciones.</span><span class="sxs-lookup"><span data-stu-id="f6822-106">These collections allow managed system elements to be grouped for identification purposes and to simplify the association of settings and configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6822-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6822-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a><span data-ttu-id="f6822-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6822-108">Members</span></span>

<span data-ttu-id="f6822-109">La clase **CIM \_ CollectionOfMSEs** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f6822-109">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="f6822-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6822-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6822-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6822-111">Properties</span></span>

<span data-ttu-id="f6822-112">La clase **CIM \_ CollectionOfMSEs** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6822-112">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6822-113">**Recopilación**</span><span class="sxs-lookup"><span data-stu-id="f6822-113">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6822-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6822-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6822-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6822-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6822-116">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f6822-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f6822-117">La identificación del objeto de colección.</span><span class="sxs-lookup"><span data-stu-id="f6822-117">The identification of the collection object.</span></span> <span data-ttu-id="f6822-118">Cuando se subclasen, la propiedad **CollectionID** se puede invalidar como una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="f6822-118">When subclassed, the **CollectionID** property can be overridden as a key property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6822-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6822-119">Requirements</span></span>



| <span data-ttu-id="f6822-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6822-120">Requirement</span></span> | <span data-ttu-id="f6822-121">Value</span><span class="sxs-lookup"><span data-stu-id="f6822-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6822-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6822-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6822-123">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6822-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f6822-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6822-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6822-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f6822-125">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f6822-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6822-126">Namespace</span></span><br/>                | <span data-ttu-id="f6822-127">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f6822-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f6822-128">MOF</span><span class="sxs-lookup"><span data-stu-id="f6822-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6822-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6822-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6822-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6822-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6822-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6822-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f6822-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6822-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6822-133">**\_Colección CIM**</span><span class="sxs-lookup"><span data-stu-id="f6822-133">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

