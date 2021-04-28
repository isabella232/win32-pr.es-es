---
description: 'Msvm_FcDeviceSAPImplementation clase : representa una asociación entre un punto de acceso de servicio y el dispositivo lógico que lo implementa.'
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Msvm_FcDeviceSAPImplementation clase
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
ms.openlocfilehash: b0df7a198b3ee52d131800073f8be30d51d93181
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119033"
---
# <a name="msvm_fcdevicesapimplementation-class"></a><span data-ttu-id="79300-103">Clase Msvm \_ FcDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="79300-103">Msvm\_FcDeviceSAPImplementation class</span></span>

<span data-ttu-id="79300-104">Representa una asociación entre un punto de acceso de servicio y el dispositivo lógico que lo implementa.</span><span class="sxs-lookup"><span data-stu-id="79300-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="79300-105">La cardinalidad de esta asociación es de varios a varios.</span><span class="sxs-lookup"><span data-stu-id="79300-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="79300-106">Más de un dispositivo lógico puede proporcionar un punto de acceso de servicio (SAP), que funciona conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="79300-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="79300-107">Cualquier dispositivo puede proporcionar más de un SAP.</span><span class="sxs-lookup"><span data-stu-id="79300-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="79300-108">Cuando muchos dispositivos lógicos están asociados a un único SAP, se supone que estos elementos funcionan juntos para proporcionar el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="79300-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="79300-109">Si existen implementaciones diferentes de un SAP, cada una de estas implementaciones daría lugar a instancias individuales del objeto de SAP.</span><span class="sxs-lookup"><span data-stu-id="79300-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="79300-110">Estas instancias individuales tendrían asociaciones con las implementaciones únicas.</span><span class="sxs-lookup"><span data-stu-id="79300-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="79300-111">La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="79300-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="79300-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79300-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="79300-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="79300-113">Members</span></span>

<span data-ttu-id="79300-114">La **clase Msvm \_ FcDeviceSAPImplementation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="79300-114">The **Msvm\_FcDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="79300-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79300-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79300-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79300-116">Properties</span></span>

<span data-ttu-id="79300-117">La **clase Msvm \_ FcDeviceSAPImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="79300-117">The **Msvm\_FcDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79300-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="79300-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79300-119">Tipo de datos: **\_ CIM FCPort**</span><span class="sxs-lookup"><span data-stu-id="79300-119">Data type: **CIM\_FCPort**</span></span>
</dt> <dt>

<span data-ttu-id="79300-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79300-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79300-121">Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")</span><span class="sxs-lookup"><span data-stu-id="79300-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="79300-122">Referencia a una clase derivada de **CIM \_ FCPort** que representa el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79300-122">A reference to a class derived from **CIM\_FCPort** that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="79300-123">**Dependiente**</span><span class="sxs-lookup"><span data-stu-id="79300-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79300-124">Tipo de datos: **Msvm \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="79300-124">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="79300-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79300-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79300-126">Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")</span><span class="sxs-lookup"><span data-stu-id="79300-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="79300-127">Referencia a una instancia de la clase [**\_ FcEndpoint de Msvm**](msvm-fcendpoint.md) que representa el SAP que usa **el antecedente**.</span><span class="sxs-lookup"><span data-stu-id="79300-127">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79300-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79300-128">Requirements</span></span>



| <span data-ttu-id="79300-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="79300-129">Requirement</span></span> | <span data-ttu-id="79300-130">Valor</span><span class="sxs-lookup"><span data-stu-id="79300-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79300-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79300-131">Minimum supported client</span></span><br/> | <span data-ttu-id="79300-132">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="79300-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="79300-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79300-133">Minimum supported server</span></span><br/> | <span data-ttu-id="79300-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="79300-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79300-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="79300-135">Namespace</span></span><br/>                | <span data-ttu-id="79300-136">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="79300-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="79300-137">MOF</span><span class="sxs-lookup"><span data-stu-id="79300-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79300-138"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="79300-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79300-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79300-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79300-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79300-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

