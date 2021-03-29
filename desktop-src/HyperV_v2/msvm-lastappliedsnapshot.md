---
description: Representa una asociación entre un sistema virtual y los datos de configuración de la instantánea que se aplicó más recientemente al sistema virtual.
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Msvm_LastAppliedSnapshot (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 48854d7b5aaaa6f8026f8dec14745545b0c58806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667172"
---
# <a name="msvm_lastappliedsnapshot-class"></a><span data-ttu-id="ced5c-103">MSVM \_ LastAppliedSnapshot (clase)</span><span class="sxs-lookup"><span data-stu-id="ced5c-103">Msvm\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="ced5c-104">Representa una asociación entre un sistema virtual y los datos de configuración de la instantánea que se aplicó más recientemente al sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="ced5c-104">Represents an association between a virtual system and the setting data of the snapshot that was most recently applied to the virtual system.</span></span>

<span data-ttu-id="ced5c-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ced5c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ced5c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ced5c-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ced5c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ced5c-107">Members</span></span>

<span data-ttu-id="ced5c-108">La clase **MSVM \_ LastAppliedSnapshot** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ced5c-108">The **Msvm\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="ced5c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ced5c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ced5c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ced5c-110">Properties</span></span>

<span data-ttu-id="ced5c-111">La clase **MSVM \_ LastAppliedSnapshot** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ced5c-111">The **Msvm\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ced5c-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ced5c-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ced5c-113">Tipo de datos: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="ced5c-113">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="ced5c-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ced5c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ced5c-115">Calificadores: **override**, **min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="ced5c-115">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="ced5c-116">Referencia a una instancia de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea del sistema virtual que se aplicó por última vez al sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="ced5c-116">Reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that was last applied to the virtual system.</span></span> <span data-ttu-id="ced5c-117">Esta propiedad se hereda de **la \_ dependencia CIM**.</span><span class="sxs-lookup"><span data-stu-id="ced5c-117">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> <dt>

<span data-ttu-id="ced5c-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="ced5c-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ced5c-119">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="ced5c-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="ced5c-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ced5c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ced5c-121">Calificadores: **override**, **min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="ced5c-121">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="ced5c-122">Referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa el sistema virtual en el que la instantánea del sistema virtual representada por la propiedad **Antecedent** se aplicó más recientemente.</span><span class="sxs-lookup"><span data-stu-id="ced5c-122">Reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system upon which the virtual system snapshot represented by the **Antecedent** property was most recently applied.</span></span> <span data-ttu-id="ced5c-123">Esta propiedad se hereda de **la \_ dependencia CIM**.</span><span class="sxs-lookup"><span data-stu-id="ced5c-123">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ced5c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ced5c-124">Requirements</span></span>



| <span data-ttu-id="ced5c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ced5c-125">Requirement</span></span> | <span data-ttu-id="ced5c-126">Value</span><span class="sxs-lookup"><span data-stu-id="ced5c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ced5c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ced5c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ced5c-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ced5c-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ced5c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ced5c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ced5c-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ced5c-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ced5c-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ced5c-131">Namespace</span></span><br/>                | <span data-ttu-id="ced5c-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ced5c-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ced5c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ced5c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ced5c-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ced5c-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ced5c-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ced5c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ced5c-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ced5c-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




