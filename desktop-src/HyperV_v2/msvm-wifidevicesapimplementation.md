---
description: Una asociación entre un punto de acceso al servicio (SAP) y cómo se implementa.
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Msvm_WiFiDeviceSAPImplementation (clase)
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
ms.openlocfilehash: 8debec96efb93e60ec18d75b62ffa0d13b0e0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907897"
---
# <a name="msvm_wifidevicesapimplementation-class"></a><span data-ttu-id="cf5f1-103">MSVM \_ WiFiDeviceSAPImplementation (clase)</span><span class="sxs-lookup"><span data-stu-id="cf5f1-103">Msvm\_WiFiDeviceSAPImplementation class</span></span>

<span data-ttu-id="cf5f1-104">Una asociación entre un punto de acceso al servicio (SAP) y cómo se implementa.</span><span class="sxs-lookup"><span data-stu-id="cf5f1-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="cf5f1-105">La cardinalidad de esta asociación es de varios a varios.</span><span class="sxs-lookup"><span data-stu-id="cf5f1-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="cf5f1-106">Un SAP puede ser proporcionado por más de un dispositivo lógico, que funciona conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="cf5f1-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="cf5f1-107">Cualquier dispositivo puede proporcionar más de un SAP.</span><span class="sxs-lookup"><span data-stu-id="cf5f1-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="cf5f1-108">Cuando muchos dispositivos lógicos están asociados a un único SAP, se supone que estos elementos funcionan conjuntamente para proporcionar el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="cf5f1-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="cf5f1-109">Si existen implementaciones diferentes de un SAP, cada una de estas implementaciones produciría instancias individuales del objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="cf5f1-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="cf5f1-110">Estas creaciones de instancias individuales tendrían asociaciones con las implementaciones únicas.</span><span class="sxs-lookup"><span data-stu-id="cf5f1-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="cf5f1-111">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cf5f1-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf5f1-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf5f1-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="cf5f1-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf5f1-113">Members</span></span>

<span data-ttu-id="cf5f1-114">La clase **MSVM \_ WiFiDeviceSAPImplementation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cf5f1-114">The **Msvm\_WiFiDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="cf5f1-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf5f1-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf5f1-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf5f1-116">Properties</span></span>

<span data-ttu-id="cf5f1-117">La clase **MSVM \_ WiFiDeviceSAPImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cf5f1-117">The **Msvm\_WiFiDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf5f1-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="cf5f1-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5f1-119">Tipo de datos: **[ **MSVM \_ WiFiPort**](msvm-wifiport.md)**</span><span class="sxs-lookup"><span data-stu-id="cf5f1-119">Data type: **[**Msvm\_WiFiPort**](msvm-wifiport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cf5f1-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cf5f1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5f1-121">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="cf5f1-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cf5f1-122">Instancia de la clase [**MSVM \_ WiFiPort**](msvm-wifiport.md) que representa el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cf5f1-122">An instance of the [**Msvm\_WiFiPort**](msvm-wifiport.md) class that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="cf5f1-123">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="cf5f1-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf5f1-124">Tipo de datos: **[ **MSVM \_ WiFiEndpoint**](msvm-wifiendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="cf5f1-124">Data type: **[**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cf5f1-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cf5f1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf5f1-126">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="cf5f1-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cf5f1-127">Instancia de la clase [**MSVM \_ WiFiEndpoint**](msvm-wifiendpoint.md) que representa el punto de acceso al servicio implementado mediante el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cf5f1-127">An instance of the [**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md) class that represents the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf5f1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf5f1-128">Requirements</span></span>



| <span data-ttu-id="cf5f1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf5f1-129">Requirement</span></span> | <span data-ttu-id="cf5f1-130">Value</span><span class="sxs-lookup"><span data-stu-id="cf5f1-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf5f1-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf5f1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cf5f1-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf5f1-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cf5f1-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf5f1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cf5f1-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf5f1-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf5f1-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cf5f1-135">Namespace</span></span><br/>                | <span data-ttu-id="cf5f1-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="cf5f1-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cf5f1-137">MOF</span><span class="sxs-lookup"><span data-stu-id="cf5f1-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf5f1-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf5f1-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf5f1-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cf5f1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf5f1-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf5f1-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

