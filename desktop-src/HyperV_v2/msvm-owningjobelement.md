---
description: Representa una asociación entre un trabajo y el elemento administrado responsable de la creación del trabajo.
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Msvm_OwningJobElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_OwningJobElement
- Msvm_OwningJobElement.OwningElement
- Msvm_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 34aa6f390d21a37421e09f30f9a775784717be9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688560"
---
# <a name="msvm_owningjobelement-class"></a><span data-ttu-id="96201-103">MSVM \_ OwningJobElement (clase)</span><span class="sxs-lookup"><span data-stu-id="96201-103">Msvm\_OwningJobElement class</span></span>

<span data-ttu-id="96201-104">Representa una asociación entre un trabajo y el elemento administrado responsable de la creación del trabajo.</span><span class="sxs-lookup"><span data-stu-id="96201-104">Represents an association between a job and the managed element responsible for the creation of the job.</span></span>

<span data-ttu-id="96201-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="96201-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="96201-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96201-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_OwningJobElement : CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  Msvm_ConcreteJob   REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="96201-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="96201-107">Members</span></span>

<span data-ttu-id="96201-108">La clase **MSVM \_ OwningJobElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="96201-108">The **Msvm\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="96201-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96201-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96201-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96201-110">Properties</span></span>

<span data-ttu-id="96201-111">La clase **MSVM \_ OwningJobElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="96201-111">The **Msvm\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96201-112">**OwnedElement**</span><span class="sxs-lookup"><span data-stu-id="96201-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96201-113">Tipo de datos: **[ **MSVM \_ ConcreteJob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="96201-113">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="96201-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96201-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96201-115">El trabajo creado por el elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="96201-115">The job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="96201-116">**OwningElement**</span><span class="sxs-lookup"><span data-stu-id="96201-116">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96201-117">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="96201-117">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="96201-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96201-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96201-119">Elemento administrado responsable de la creación del trabajo.</span><span class="sxs-lookup"><span data-stu-id="96201-119">The managed element responsible for the creation of the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96201-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96201-120">Requirements</span></span>



| <span data-ttu-id="96201-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="96201-121">Requirement</span></span> | <span data-ttu-id="96201-122">Value</span><span class="sxs-lookup"><span data-stu-id="96201-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96201-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96201-123">Minimum supported client</span></span><br/> | <span data-ttu-id="96201-124">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="96201-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="96201-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96201-125">Minimum supported server</span></span><br/> | <span data-ttu-id="96201-126">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="96201-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96201-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="96201-127">Namespace</span></span><br/>                | <span data-ttu-id="96201-128">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="96201-128">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="96201-129">MOF</span><span class="sxs-lookup"><span data-stu-id="96201-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96201-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96201-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="96201-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96201-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96201-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="96201-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

