---
description: Una relación que indica que dos o más dispositivos están conectados juntos.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: CIM_DeviceConnection (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.NegotiatedSpeed
- CIM_DeviceConnection.NegotiatedDataWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f58c66199abeb5b3586f52e91828b8b194bdbbd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687041"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a><span data-ttu-id="b6718-103">CIM_DeviceConnection (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="b6718-103">CIM_DeviceConnection class (Hyper-V management)</span></span>

<span data-ttu-id="b6718-104">Una relación que indica que dos o más dispositivos están conectados juntos.</span><span class="sxs-lookup"><span data-stu-id="b6718-104">A relationship that indicates that two or more devices are connected together.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6718-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6718-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::DeviceElements"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint64                NegotiatedSpeed;
  uint32                NegotiatedDataWidth;
};
```

## <a name="members"></a><span data-ttu-id="b6718-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6718-106">Members</span></span>

<span data-ttu-id="b6718-107">La **clase \_ de CIM de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b6718-107">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="b6718-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6718-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6718-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6718-109">Properties</span></span>

<span data-ttu-id="b6718-110">La **clase \_ DeviceConnection de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b6718-110">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6718-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b6718-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6718-112">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="b6718-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b6718-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6718-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6718-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="b6718-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b6718-115">Un dispositivo</span><span class="sxs-lookup"><span data-stu-id="b6718-115">A device.</span></span>

</dd> <dt>

<span data-ttu-id="b6718-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="b6718-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6718-117">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="b6718-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b6718-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6718-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6718-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="b6718-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b6718-120">Un segundo dispositivo que está conectado al otro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6718-120">A second device that is connected to the other device.</span></span>

</dd> <dt>

<span data-ttu-id="b6718-121">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="b6718-121">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6718-122">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b6718-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6718-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6718-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6718-124">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Asociación de puerto de bus DMTF \| 001,3 "), **punitivo** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="b6718-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.3"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="b6718-125">Cuando se pueden usar varios buses y anchos de datos de conexión, la propiedad NegotiatedDataWidth define el que está en uso entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b6718-125">When several bus and connection data widths are possible, the NegotiatedDataWidth property defines the one that is in use between the Devices.</span></span> <span data-ttu-id="b6718-126">El ancho de los datos se especifica en bits.</span><span class="sxs-lookup"><span data-stu-id="b6718-126">Data width is specified in bits.</span></span> <span data-ttu-id="b6718-127">Si no se negocia el ancho de los datos, o si esta información no está disponible o no es importante para la administración de dispositivos, la propiedad debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="b6718-127">If data width is not negotiated, or if this information is not available or not important to Device management, the property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="b6718-128">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="b6718-128">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6718-129">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b6718-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b6718-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6718-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6718-131">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Asociación de puerto de bus DMTF \| 001,2 "), **punitivo** (" bit por segundo ")</span><span class="sxs-lookup"><span data-stu-id="b6718-131">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.2"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="b6718-132">Cuando se pueden realizar varias velocidades de conexión y bus, esta propiedad define la velocidad que se utiliza entre los dispositivos, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="b6718-132">When several bus and connection speeds are possible, this property defines the speed that is in use between the devices, in bits per second.</span></span> <span data-ttu-id="b6718-133">Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o no es importante para la administración de dispositivos, la propiedad debe establecerse en "0".</span><span class="sxs-lookup"><span data-stu-id="b6718-133">If connection or bus speeds are not negotiated, or if this information is not available, or not important to device management, the property should be set to "0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6718-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6718-134">Requirements</span></span>



| <span data-ttu-id="b6718-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6718-135">Requirement</span></span> | <span data-ttu-id="b6718-136">Value</span><span class="sxs-lookup"><span data-stu-id="b6718-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6718-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6718-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b6718-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b6718-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b6718-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6718-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b6718-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b6718-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b6718-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b6718-141">Namespace</span></span><br/>                | <span data-ttu-id="b6718-142">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b6718-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b6718-143">MOF</span><span class="sxs-lookup"><span data-stu-id="b6718-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6718-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6718-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6718-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6718-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6718-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b6718-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b6718-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6718-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6718-148">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b6718-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

