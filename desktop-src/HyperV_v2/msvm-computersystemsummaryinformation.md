---
description: Contiene un resumen de información sobre el sistema del equipo virtual especificado.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Msvm_ComputerSystemSummaryInformation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35248bcfa14609e8db25b148088b6feb8d161116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907992"
---
# <a name="msvm_computersystemsummaryinformation-class"></a><span data-ttu-id="20ab3-103">MSVM \_ ComputerSystemSummaryInformation (clase)</span><span class="sxs-lookup"><span data-stu-id="20ab3-103">Msvm\_ComputerSystemSummaryInformation class</span></span>

<span data-ttu-id="20ab3-104">Contiene un resumen de información sobre el sistema del equipo virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="20ab3-104">Contains an information summary about the specified virtual computer system.</span></span>

<span data-ttu-id="20ab3-105">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="20ab3-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ab3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20ab3-106">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="20ab3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="20ab3-107">Members</span></span>

<span data-ttu-id="20ab3-108">La clase **MSVM \_ ComputerSystemSummaryInformation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="20ab3-108">The **Msvm\_ComputerSystemSummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="20ab3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20ab3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20ab3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20ab3-110">Properties</span></span>

<span data-ttu-id="20ab3-111">La clase **MSVM \_ ComputerSystemSummaryInformation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="20ab3-111">The **Msvm\_ComputerSystemSummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20ab3-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="20ab3-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ab3-113">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="20ab3-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="20ab3-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20ab3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ab3-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="20ab3-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="20ab3-116">Un [**objeto \_ ComputerSystem de CIM**](cim-computersystem.md) que es una instancia de la representación normalizada del recurso administrado.</span><span class="sxs-lookup"><span data-stu-id="20ab3-116">A [**CIM\_ComputerSystem**](cim-computersystem.md) object that is an instance in the normalized representation of the managed resource.</span></span>

> [!Note]
>
> <span data-ttu-id="20ab3-117">Tipo de DataType actualizado desde [**MSVM \_ ComputerSystem**](msvm-computersystem.md) en Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="20ab3-117">Datatype upgraded from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="20ab3-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="20ab3-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ab3-119">Tipo de datos: **MSVM \_ SummaryInformationBase**</span><span class="sxs-lookup"><span data-stu-id="20ab3-119">Data type: **Msvm\_SummaryInformationBase**</span></span>
</dt> <dt>

<span data-ttu-id="20ab3-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20ab3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ab3-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="20ab3-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="20ab3-122">Instancia de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) que representa una vista desnormalizada o agregada del recurso administrado representado por el [**MSVM \_ ComputerSystem**](msvm-computersystem.md) al que hace referencia la propiedad antecedente.</span><span class="sxs-lookup"><span data-stu-id="20ab3-122">An instance of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) that represents a de-normalized or aggregate view of the managed resource that is represented by the [**Msvm\_ComputerSystem**](msvm-computersystem.md) referenced by the Antecedent property.</span></span>

> [!Note]
>
> <span data-ttu-id="20ab3-123">DataType actualizado desde [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) en Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="20ab3-123">Datatype updated from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) in Windows 10, version 1703.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20ab3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20ab3-124">Requirements</span></span>



| <span data-ttu-id="20ab3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="20ab3-125">Requirement</span></span> | <span data-ttu-id="20ab3-126">Value</span><span class="sxs-lookup"><span data-stu-id="20ab3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ab3-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20ab3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="20ab3-128">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="20ab3-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="20ab3-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20ab3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="20ab3-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="20ab3-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="20ab3-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="20ab3-131">Namespace</span></span><br/>                | <span data-ttu-id="20ab3-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="20ab3-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="20ab3-133">MOF</span><span class="sxs-lookup"><span data-stu-id="20ab3-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20ab3-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20ab3-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20ab3-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="20ab3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20ab3-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20ab3-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="20ab3-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="20ab3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ab3-138">**\_ELEMENTVIEW CIM**</span><span class="sxs-lookup"><span data-stu-id="20ab3-138">**CIM\_ElementView**</span></span>](cim-elementview.md)
</dt> </dl>

 

