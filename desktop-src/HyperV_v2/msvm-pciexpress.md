---
description: Representa el estado del puerto PCI Express.
ms.assetid: 15d670ee-940a-4737-b2cd-e89dd8a63a5c
title: Msvm_PciExpress (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpress
- Msvm_PciExpress.DeviceInstancePath
- Msvm_PciExpress.LocationPath
- Msvm_PciExpress.FunctionNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7534d09c9c0f3825ca462c342747caa17c8de9c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688556"
---
# <a name="msvm_pciexpress-class"></a><span data-ttu-id="8bb0f-103">MSVM \_ PciExpress (clase)</span><span class="sxs-lookup"><span data-stu-id="8bb0f-103">Msvm\_PciExpress class</span></span>

<span data-ttu-id="8bb0f-104">Representa el estado del puerto PCI Express.</span><span class="sxs-lookup"><span data-stu-id="8bb0f-104">Represents the state of the PCI Express port.</span></span>

<span data-ttu-id="8bb0f-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8bb0f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb0f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bb0f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpress : CIM_LogicalDevice
{
  string DeviceInstancePath;
  string LocationPath;
  uint16 FunctionNumber;
};
```

## <a name="members"></a><span data-ttu-id="8bb0f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8bb0f-107">Members</span></span>

<span data-ttu-id="8bb0f-108">La clase **MSVM \_ PciExpress** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8bb0f-108">The **Msvm\_PciExpress** class has these types of members:</span></span>

-   [<span data-ttu-id="8bb0f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bb0f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bb0f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bb0f-110">Properties</span></span>

<span data-ttu-id="8bb0f-111">La clase **MSVM \_ PciExpress** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8bb0f-111">The **Msvm\_PciExpress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bb0f-112">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="8bb0f-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bb0f-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8bb0f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bb0f-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8bb0f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bb0f-115">Una cadena que contiene la ruta de acceso de la instancia del dispositivo que identifica el dispositivo PCI Express virtual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8bb0f-115">A string containing the device instance path that identifies the device virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="8bb0f-116">**FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="8bb0f-116">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bb0f-117">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bb0f-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bb0f-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8bb0f-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bb0f-119">El número de función del dispositivo virtual PCI Express.</span><span class="sxs-lookup"><span data-stu-id="8bb0f-119">The function number of the virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="8bb0f-120">**LocationPath**</span><span class="sxs-lookup"><span data-stu-id="8bb0f-120">**LocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bb0f-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8bb0f-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bb0f-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8bb0f-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bb0f-123">Una cadena que contiene la ruta de acceso de ubicación del dispositivo que identifica el dispositivo PCI Express virtual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8bb0f-123">A string containing the device location path that identifies the device virtual PCI Express device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bb0f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bb0f-124">Requirements</span></span>



| <span data-ttu-id="8bb0f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bb0f-125">Requirement</span></span> | <span data-ttu-id="8bb0f-126">Value</span><span class="sxs-lookup"><span data-stu-id="8bb0f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb0f-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bb0f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb0f-128">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="8bb0f-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8bb0f-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bb0f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb0f-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8bb0f-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8bb0f-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8bb0f-131">Namespace</span></span><br/>                | <span data-ttu-id="8bb0f-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8bb0f-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8bb0f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8bb0f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bb0f-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bb0f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bb0f-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8bb0f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bb0f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8bb0f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8bb0f-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bb0f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb0f-138">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="8bb0f-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




