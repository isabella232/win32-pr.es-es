---
description: Representa una asociación entre un trabajo y el elemento administrado que creó el trabajo.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: CIM_OwningJobElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9d3879104a8f7406ff24dc2f63b79b51eb2fa58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668431"
---
# <a name="cim_owningjobelement-class"></a><span data-ttu-id="09147-103">\_Clase OwningJobElement de CIM</span><span class="sxs-lookup"><span data-stu-id="09147-103">CIM\_OwningJobElement class</span></span>

<span data-ttu-id="09147-104">Representa una asociación entre un trabajo y el elemento administrado que creó el trabajo.</span><span class="sxs-lookup"><span data-stu-id="09147-104">Represents an association between a job and the managed element that created the job.</span></span> <span data-ttu-id="09147-105">Dado que un trabajo puede moverse entre sistemas y el elemento administrado podría no existir durante toda la duración del trabajo, en algunos casos, es posible que esta asociación no sea posible o que solo exista para una parte de la existencia del trabajo.</span><span class="sxs-lookup"><span data-stu-id="09147-105">Since a job might move between systems, and the managed element might not exist for the entire duration of the job, in some cases, this association might not be possible or might only exist for a portion of the existence of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="09147-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09147-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="09147-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="09147-107">Members</span></span>

<span data-ttu-id="09147-108">La clase **CIM \_ OwningJobElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="09147-108">The **CIM\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="09147-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09147-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09147-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09147-110">Properties</span></span>

<span data-ttu-id="09147-111">La clase **CIM \_ OwningJobElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="09147-111">The **CIM\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09147-112">**OwnedElement**</span><span class="sxs-lookup"><span data-stu-id="09147-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09147-113">Tipo de datos **: \_ trabajo CIM**</span><span class="sxs-lookup"><span data-stu-id="09147-113">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="09147-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="09147-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09147-115">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="09147-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="09147-116">Referencia al trabajo creado por el elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="09147-116">A reference to the job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="09147-117">**OwningElement**</span><span class="sxs-lookup"><span data-stu-id="09147-117">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09147-118">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="09147-118">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="09147-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="09147-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09147-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="09147-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="09147-121">Referencia al elemento administrado que creó el trabajo.</span><span class="sxs-lookup"><span data-stu-id="09147-121">A reference to the managed element that created the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09147-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09147-122">Requirements</span></span>



| <span data-ttu-id="09147-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="09147-123">Requirement</span></span> | <span data-ttu-id="09147-124">Value</span><span class="sxs-lookup"><span data-stu-id="09147-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09147-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09147-125">Minimum supported client</span></span><br/> | <span data-ttu-id="09147-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="09147-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="09147-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09147-127">Minimum supported server</span></span><br/> | <span data-ttu-id="09147-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09147-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="09147-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="09147-129">Namespace</span></span><br/>                | <span data-ttu-id="09147-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="09147-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="09147-131">MOF</span><span class="sxs-lookup"><span data-stu-id="09147-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09147-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09147-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09147-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09147-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09147-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09147-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

