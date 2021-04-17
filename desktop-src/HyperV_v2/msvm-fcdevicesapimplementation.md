---
description: Representa una asociación entre un punto de acceso al servicio y el dispositivo lógico que lo implementa.
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Msvm_FcDeviceSAPImplementation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc40f25e3b288155e713415aa512d629b538d1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666620"
---
# <a name="msvm_fcdevicesapimplementation-class"></a><span data-ttu-id="a704a-103">MSVM \_ FcDeviceSAPImplementation (clase)</span><span class="sxs-lookup"><span data-stu-id="a704a-103">Msvm\_FcDeviceSAPImplementation class</span></span>

<span data-ttu-id="a704a-104">Representa una asociación entre un punto de acceso al servicio y el dispositivo lógico que lo implementa.</span><span class="sxs-lookup"><span data-stu-id="a704a-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="a704a-105">La cardinalidad de esta asociación es de varios a varios.</span><span class="sxs-lookup"><span data-stu-id="a704a-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="a704a-106">Un punto de acceso al servicio (SAP) puede ser proporcionado por más de un dispositivo lógico, que funciona conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="a704a-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="a704a-107">Cualquier dispositivo puede proporcionar más de un SAP.</span><span class="sxs-lookup"><span data-stu-id="a704a-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="a704a-108">Cuando muchos dispositivos lógicos están asociados a un único SAP, se supone que estos elementos funcionan conjuntamente para proporcionar el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="a704a-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="a704a-109">Si existen implementaciones diferentes de un SAP, cada una de estas implementaciones produciría instancias individuales del objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="a704a-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="a704a-110">Estas creaciones de instancias individuales tendrían asociaciones con las implementaciones únicas.</span><span class="sxs-lookup"><span data-stu-id="a704a-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="a704a-111">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a704a-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a704a-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a704a-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a704a-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="a704a-113">Members</span></span>

<span data-ttu-id="a704a-114">La clase **MSVM \_ FcDeviceSAPImplementation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a704a-114">The **Msvm\_FcDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="a704a-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a704a-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a704a-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a704a-116">Properties</span></span>

<span data-ttu-id="a704a-117">La clase **MSVM \_ FcDeviceSAPImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a704a-117">The **Msvm\_FcDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a704a-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="a704a-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a704a-119">Tipo de datos: **CIM \_ FCPort**</span><span class="sxs-lookup"><span data-stu-id="a704a-119">Data type: **CIM\_FCPort**</span></span>
</dt> <dt>

<span data-ttu-id="a704a-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a704a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a704a-121">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="a704a-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a704a-122">Referencia a una clase derivada de **\_ FCPort de CIM** que representa el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a704a-122">A reference to a class derived from **CIM\_FCPort** that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="a704a-123">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="a704a-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a704a-124">Tipo de datos: **MSVM \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="a704a-124">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="a704a-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a704a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a704a-126">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="a704a-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a704a-127">Una referencia a una instancia de la clase [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) que representa el SAP que usa el **antecedente**.</span><span class="sxs-lookup"><span data-stu-id="a704a-127">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a704a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a704a-128">Requirements</span></span>



| <span data-ttu-id="a704a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a704a-129">Requirement</span></span> | <span data-ttu-id="a704a-130">Value</span><span class="sxs-lookup"><span data-stu-id="a704a-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a704a-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a704a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a704a-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a704a-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a704a-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a704a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a704a-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a704a-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a704a-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a704a-135">Namespace</span></span><br/>                | <span data-ttu-id="a704a-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a704a-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a704a-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a704a-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a704a-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a704a-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a704a-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a704a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a704a-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a704a-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

