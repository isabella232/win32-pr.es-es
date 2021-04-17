---
description: Representa y asocia entre una vista y una instancia de que representa la vista normalizada de un recurso administrado.
ms.assetid: 9c6eb3d5-7366-4954-9e64-12f889c64114
title: CIM_ElementView (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementView
- CIM_ElementView.Antecedent
- CIM_ElementView.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ffc0e4b69667800b1880cae1a992a207cc95a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667575"
---
# <a name="cim_elementview-class"></a><span data-ttu-id="3b743-103">\_Clase ElementView de CIM</span><span class="sxs-lookup"><span data-stu-id="3b743-103">CIM\_ElementView class</span></span>

<span data-ttu-id="3b743-104">Representa y asocia entre una vista y una instancia de que representa la vista normalizada de un recurso administrado.</span><span class="sxs-lookup"><span data-stu-id="3b743-104">Represents and association between a view, and an instance that represents the normalized view of a managed resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b743-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b743-105">Syntax</span></span>

``` syntax
[Abstract, Association, Experimental, Version("2.21.1"), UMLPackagePath("CIM::Core::CoreElements")]
class CIM_ElementView : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_View           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3b743-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b743-106">Members</span></span>

<span data-ttu-id="3b743-107">La clase **CIM \_ ElementView** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3b743-107">The **CIM\_ElementView** class has these types of members:</span></span>

-   [<span data-ttu-id="3b743-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b743-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b743-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b743-109">Properties</span></span>

<span data-ttu-id="3b743-110">La clase **CIM \_ ElementView** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3b743-110">The **CIM\_ElementView** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b743-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3b743-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b743-112">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="3b743-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="3b743-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b743-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b743-114">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="3b743-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3b743-115">Instancia de que representa la vista normalizada del recurso administrado.</span><span class="sxs-lookup"><span data-stu-id="3b743-115">The instance that represents the normalized view of the managed resource.</span></span>

</dd> <dt>

<span data-ttu-id="3b743-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="3b743-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b743-117">Tipo de datos **: \_ vista CIM**</span><span class="sxs-lookup"><span data-stu-id="3b743-117">Data type: **CIM\_View**</span></span>
</dt> <dt>

<span data-ttu-id="3b743-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b743-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b743-119">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="3b743-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3b743-120">La vista que representa una vista de agregado o desnormalizado del recurso administrado.</span><span class="sxs-lookup"><span data-stu-id="3b743-120">The view that represents a de-normalized or aggregate view of the managed resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b743-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b743-121">Requirements</span></span>



| <span data-ttu-id="3b743-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b743-122">Requirement</span></span> | <span data-ttu-id="3b743-123">Value</span><span class="sxs-lookup"><span data-stu-id="3b743-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b743-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b743-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3b743-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b743-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3b743-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b743-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3b743-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3b743-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3b743-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b743-128">Namespace</span></span><br/>                | <span data-ttu-id="3b743-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3b743-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3b743-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3b743-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b743-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b743-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b743-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b743-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b743-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b743-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3b743-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b743-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b743-135">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3b743-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

