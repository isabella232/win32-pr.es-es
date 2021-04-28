---
description: 'Msvm_EthernetDeviceSAPImplementation clase : representa una asociación entre un punto de acceso de servicio y el dispositivo lógico que lo implementa.'
ms.assetid: C0DDB199-AD97-4DD7-8056-BD6BD0CECFA8
title: Msvm_EthernetDeviceSAPImplementation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetDeviceSAPImplementation
- Msvm_EthernetDeviceSAPImplementation.Antecedent
- Msvm_EthernetDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fddce9505ca2f8692044239d294904eb17c95ffa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111953"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a><span data-ttu-id="8b924-103">Clase Msvm \_ EthernetDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="8b924-103">Msvm\_EthernetDeviceSAPImplementation class</span></span>

<span data-ttu-id="8b924-104">Representa una asociación entre un punto de acceso de servicio y el dispositivo lógico que lo implementa.</span><span class="sxs-lookup"><span data-stu-id="8b924-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="8b924-105">La cardinalidad de esta asociación es de varios a varios.</span><span class="sxs-lookup"><span data-stu-id="8b924-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="8b924-106">Más de un dispositivo lógico puede proporcionar un punto de acceso de servicio (SAP), que funciona conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="8b924-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="8b924-107">Cualquier dispositivo puede proporcionar más de un SAP.</span><span class="sxs-lookup"><span data-stu-id="8b924-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="8b924-108">Cuando muchos dispositivos lógicos están asociados a un único SAP, se supone que estos elementos funcionan juntos para proporcionar el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="8b924-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="8b924-109">Si existen implementaciones diferentes de un SAP, cada una de estas implementaciones daría como resultado instancias individuales del objeto de SAP.</span><span class="sxs-lookup"><span data-stu-id="8b924-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="8b924-110">Estas instancias individuales tendrían entonces asociaciones con las implementaciones únicas.</span><span class="sxs-lookup"><span data-stu-id="8b924-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="8b924-111">La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8b924-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b924-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b924-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8b924-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="8b924-113">Members</span></span>

<span data-ttu-id="8b924-114">La **clase Msvm \_ EthernetDeviceSAPImplementation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8b924-114">The **Msvm\_EthernetDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="8b924-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8b924-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b924-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8b924-116">Properties</span></span>

<span data-ttu-id="8b924-117">La **clase Msvm \_ EthernetDeviceSAPImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8b924-117">The **Msvm\_EthernetDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b924-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="8b924-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b924-119">Tipo de datos: **[ **Cim \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span><span class="sxs-lookup"><span data-stu-id="8b924-119">Data type: **[**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span></span>
</dt> <dt>

<span data-ttu-id="8b924-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b924-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b924-121">Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")</span><span class="sxs-lookup"><span data-stu-id="8b924-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8b924-122">Referencia a una clase derivada de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) que representa el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8b924-122">A reference to a class derived from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="8b924-123">**Dependiente**</span><span class="sxs-lookup"><span data-stu-id="8b924-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b924-124">Tipo de datos: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="8b924-124">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="8b924-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b924-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b924-126">Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")</span><span class="sxs-lookup"><span data-stu-id="8b924-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8b924-127">Referencia a una instancia de la clase [**\_ Msvm LANEndpoint**](msvm-lanendpoint.md) que representa el SAP que usa **el antecedente**.</span><span class="sxs-lookup"><span data-stu-id="8b924-127">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b924-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b924-128">Requirements</span></span>



| <span data-ttu-id="8b924-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b924-129">Requirement</span></span> | <span data-ttu-id="8b924-130">Valor</span><span class="sxs-lookup"><span data-stu-id="8b924-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b924-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b924-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8b924-132">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="8b924-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8b924-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b924-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8b924-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b924-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b924-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8b924-135">Namespace</span></span><br/>                | <span data-ttu-id="8b924-136">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="8b924-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8b924-137">MOF</span><span class="sxs-lookup"><span data-stu-id="8b924-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b924-138"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b924-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b924-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b924-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b924-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b924-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

