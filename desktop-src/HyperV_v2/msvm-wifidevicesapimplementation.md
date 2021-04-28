---
description: 'Msvm_WiFiDeviceSAPImplementation clase : asociación entre un punto de acceso de servicio (SAP) y cómo se implementa.'
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Msvm_WiFiDeviceSAPImplementation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99826ce3a37e19867cef1a6ddf276f5136b21a3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109253"
---
# <a name="msvm_wifidevicesapimplementation-class"></a><span data-ttu-id="1b906-103">Clase Msvm \_ WiFiDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="1b906-103">Msvm\_WiFiDeviceSAPImplementation class</span></span>

<span data-ttu-id="1b906-104">Asociación entre un punto de acceso de servicio (SAP) y cómo se implementa.</span><span class="sxs-lookup"><span data-stu-id="1b906-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="1b906-105">La cardinalidad de esta asociación es de varios a varios.</span><span class="sxs-lookup"><span data-stu-id="1b906-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="1b906-106">Un SAP se puede proporcionar mediante más de un dispositivo lógico, que funciona conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="1b906-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="1b906-107">Cualquier dispositivo puede proporcionar más de un SAP.</span><span class="sxs-lookup"><span data-stu-id="1b906-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="1b906-108">Cuando muchos dispositivos lógicos están asociados a un único SAP, se supone que estos elementos funcionan juntos para proporcionar el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="1b906-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="1b906-109">Si existen implementaciones diferentes de un SAP, cada una de estas implementaciones daría como resultado instancias individuales del objeto de SAP.</span><span class="sxs-lookup"><span data-stu-id="1b906-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="1b906-110">Estas instancias individuales tendrían entonces asociaciones con las implementaciones únicas.</span><span class="sxs-lookup"><span data-stu-id="1b906-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="1b906-111">La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1b906-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b906-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b906-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1b906-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="1b906-113">Members</span></span>

<span data-ttu-id="1b906-114">La **clase \_ WiFiDeviceSAPImplementation de Msvm** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1b906-114">The **Msvm\_WiFiDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="1b906-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1b906-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b906-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1b906-116">Properties</span></span>

<span data-ttu-id="1b906-117">La **clase Msvm \_ WiFiDeviceSAPImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1b906-117">The **Msvm\_WiFiDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b906-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="1b906-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b906-119">Tipo de datos: **[ **Msvm \_ WiFiPort**](msvm-wifiport.md)**</span><span class="sxs-lookup"><span data-stu-id="1b906-119">Data type: **[**Msvm\_WiFiPort**](msvm-wifiport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1b906-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1b906-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b906-121">Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")</span><span class="sxs-lookup"><span data-stu-id="1b906-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1b906-122">Instancia de la [**clase \_ WiFiPort de Msvm**](msvm-wifiport.md) que representa el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1b906-122">An instance of the [**Msvm\_WiFiPort**](msvm-wifiport.md) class that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="1b906-123">**Dependiente**</span><span class="sxs-lookup"><span data-stu-id="1b906-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b906-124">Tipo de datos: **[ **Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="1b906-124">Data type: **[**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1b906-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1b906-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b906-126">Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")</span><span class="sxs-lookup"><span data-stu-id="1b906-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1b906-127">Instancia de la clase [**\_ WiFiEndpoint de Msvm**](msvm-wifiendpoint.md) que representa el punto de acceso de servicio implementado mediante el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1b906-127">An instance of the [**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md) class that represents the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b906-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b906-128">Requirements</span></span>



| <span data-ttu-id="1b906-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b906-129">Requirement</span></span> | <span data-ttu-id="1b906-130">Valor</span><span class="sxs-lookup"><span data-stu-id="1b906-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b906-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b906-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1b906-132">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="1b906-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1b906-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b906-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1b906-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b906-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1b906-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1b906-135">Namespace</span></span><br/>                | <span data-ttu-id="1b906-136">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="1b906-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1b906-137">MOF</span><span class="sxs-lookup"><span data-stu-id="1b906-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b906-138"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b906-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b906-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1b906-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b906-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1b906-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

