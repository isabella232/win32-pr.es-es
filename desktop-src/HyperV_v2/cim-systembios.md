---
description: Asocia un BIOS a un sistema informático.
ms.assetid: a06af789-75c8-4d58-8a25-572dcf1091e2
title: CIM_SystemBIOS (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemBIOS
- CIM_SystemBIOS.GroupComponent
- CIM_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: faa3130544fdb97bdf216fa266bc9e8cfe1815bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082465"
---
# <a name="cim_systembios-class"></a><span data-ttu-id="21a43-103">\_Clase SystemBIOS de CIM</span><span class="sxs-lookup"><span data-stu-id="21a43-103">CIM\_SystemBIOS class</span></span>

<span data-ttu-id="21a43-104">Asocia un BIOS a un sistema informático.</span><span class="sxs-lookup"><span data-stu-id="21a43-104">Associates a BIOS with a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="21a43-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21a43-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_SystemBIOS : CIM_SystemComponent
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_BIOSElement    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="21a43-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="21a43-106">Members</span></span>

<span data-ttu-id="21a43-107">La clase **CIM \_ SystemBIOS** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="21a43-107">The **CIM\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="21a43-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="21a43-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21a43-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="21a43-109">Properties</span></span>

<span data-ttu-id="21a43-110">La clase **CIM \_ SystemBIOS** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="21a43-110">The **CIM\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21a43-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="21a43-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21a43-112">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="21a43-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="21a43-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="21a43-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21a43-114">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="21a43-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="21a43-115">El equipo que arranca desde el BIOS.</span><span class="sxs-lookup"><span data-stu-id="21a43-115">The computer system that boots from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="21a43-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="21a43-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21a43-117">Tipo de datos: **CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="21a43-117">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="21a43-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="21a43-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21a43-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="21a43-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="21a43-120">BIOS.</span><span class="sxs-lookup"><span data-stu-id="21a43-120">The BIOS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21a43-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21a43-121">Requirements</span></span>



| <span data-ttu-id="21a43-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="21a43-122">Requirement</span></span> | <span data-ttu-id="21a43-123">Value</span><span class="sxs-lookup"><span data-stu-id="21a43-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21a43-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21a43-124">Minimum supported client</span></span><br/> | <span data-ttu-id="21a43-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="21a43-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="21a43-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21a43-126">Minimum supported server</span></span><br/> | <span data-ttu-id="21a43-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21a43-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="21a43-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="21a43-128">Namespace</span></span><br/>                | <span data-ttu-id="21a43-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="21a43-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="21a43-130">MOF</span><span class="sxs-lookup"><span data-stu-id="21a43-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21a43-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21a43-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="21a43-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21a43-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21a43-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="21a43-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="21a43-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="21a43-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a43-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="21a43-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

