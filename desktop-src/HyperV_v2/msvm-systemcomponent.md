---
description: Establece un &\# 0034; parte de&\# 0034; relación entre un sistema y cualquier elemento del sistema administrado del que está compuesto.
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Msvm_SystemComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee150793143b549c90d280eef287ee6a5afb66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423695"
---
# <a name="msvm_systemcomponent-class"></a><span data-ttu-id="9aad8-103">MSVM \_ SystemComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="9aad8-103">Msvm\_SystemComponent class</span></span>

<span data-ttu-id="9aad8-104">Establece una relación de "parte de" entre un sistema y cualquier elemento del sistema administrado del que se compone.</span><span class="sxs-lookup"><span data-stu-id="9aad8-104">Establishes a "part of" relationship between a system and any managed system element of which it is composed.</span></span>

<span data-ttu-id="9aad8-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9aad8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aad8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9aad8-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9aad8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9aad8-107">Members</span></span>

<span data-ttu-id="9aad8-108">La clase **MSVM \_ SystemComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9aad8-108">The **Msvm\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="9aad8-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9aad8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9aad8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9aad8-110">Properties</span></span>

<span data-ttu-id="9aad8-111">La clase **MSVM \_ SystemComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9aad8-111">The **Msvm\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9aad8-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9aad8-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aad8-113">Tipo de datos: **[ **\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="9aad8-113">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="9aad8-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9aad8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9aad8-115">Elemento primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="9aad8-115">The parent element in the association.</span></span> <span data-ttu-id="9aad8-116">Esta propiedad se hereda de [**\_ SystemComponent CIM**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span><span class="sxs-lookup"><span data-stu-id="9aad8-116">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> <dt>

<span data-ttu-id="9aad8-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9aad8-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aad8-118">Tipo de datos: **[ **\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span><span class="sxs-lookup"><span data-stu-id="9aad8-118">Data type: **[**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span></span>
</dt> <dt>

<span data-ttu-id="9aad8-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9aad8-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9aad8-120">Elemento secundario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="9aad8-120">The child element in the association.</span></span> <span data-ttu-id="9aad8-121">Esta propiedad se hereda de [**\_ SystemComponent CIM**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span><span class="sxs-lookup"><span data-stu-id="9aad8-121">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9aad8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aad8-122">Requirements</span></span>



| <span data-ttu-id="9aad8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aad8-123">Requirement</span></span> | <span data-ttu-id="9aad8-124">Value</span><span class="sxs-lookup"><span data-stu-id="9aad8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aad8-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9aad8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9aad8-126">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="9aad8-126">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9aad8-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9aad8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9aad8-128">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9aad8-128">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9aad8-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9aad8-129">Namespace</span></span><br/>                | <span data-ttu-id="9aad8-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9aad8-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9aad8-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9aad8-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9aad8-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9aad8-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9aad8-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9aad8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aad8-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9aad8-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

