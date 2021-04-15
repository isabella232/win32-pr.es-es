---
description: Representa el estado configurado de un puerto PCI Express.
ms.assetid: adb03dd7-5a47-47e6-a4e4-28224164150c
title: Msvm_PciExpressSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpressSettingData
- Msvm_PciExpressSettingData.VirtualFunctions
- Msvm_PciExpressSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c092cbc119506c4c52bc0565cd969426feffc481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688555"
---
# <a name="msvm_pciexpresssettingdata-class"></a><span data-ttu-id="fc122-103">MSVM \_ PciExpressSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="fc122-103">Msvm\_PciExpressSettingData class</span></span>

<span data-ttu-id="fc122-104">Representa el estado configurado de un puerto PCI Express.</span><span class="sxs-lookup"><span data-stu-id="fc122-104">Represents the configured state of a PCI Express port.</span></span>

<span data-ttu-id="fc122-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fc122-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc122-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc122-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpressSettingData : CIM_ResourceAllocationSettingData
{
  uint16 VirtualFunctions[];
  string VirtualSystemIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="fc122-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc122-107">Members</span></span>

<span data-ttu-id="fc122-108">La clase **MSVM \_ PciExpressSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fc122-108">The **Msvm\_PciExpressSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fc122-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc122-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc122-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc122-110">Properties</span></span>

<span data-ttu-id="fc122-111">La clase **MSVM \_ PciExpressSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc122-111">The **Msvm\_PciExpressSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc122-112">**VirtualFunctions**</span><span class="sxs-lookup"><span data-stu-id="fc122-112">**VirtualFunctions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc122-113">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc122-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc122-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fc122-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fc122-115">Número de función virtual que se va a asignar a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fc122-115">The virtual function number to assign to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="fc122-116">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="fc122-116">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc122-117">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="fc122-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc122-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc122-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc122-119">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="fc122-119">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="fc122-120">Matriz de cadenas de formato libre de los identificadores de este recurso presentados al sistema operativo del sistema del equipo virtual.</span><span class="sxs-lookup"><span data-stu-id="fc122-120">A free-form string array of identifiers of this resource presented to the virtual computer system's operating system.</span></span> <span data-ttu-id="fc122-121">Los índices y valores por índice se definen por cada recurso (es decir, por cada valor **resourcetype** enumerado).</span><span class="sxs-lookup"><span data-stu-id="fc122-121">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="fc122-122">Esta propiedad se establece en "GUID".</span><span class="sxs-lookup"><span data-stu-id="fc122-122">This property is set to "GUID".</span></span>

<span data-ttu-id="fc122-123">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) de la clase SD.</span><span class="sxs-lookup"><span data-stu-id="fc122-123">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the sd class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc122-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc122-124">Requirements</span></span>



| <span data-ttu-id="fc122-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc122-125">Requirement</span></span> | <span data-ttu-id="fc122-126">Value</span><span class="sxs-lookup"><span data-stu-id="fc122-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc122-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc122-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fc122-128">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc122-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fc122-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc122-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fc122-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fc122-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fc122-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fc122-131">Namespace</span></span><br/>                | <span data-ttu-id="fc122-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="fc122-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fc122-133">MOF</span><span class="sxs-lookup"><span data-stu-id="fc122-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc122-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc122-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc122-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc122-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc122-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc122-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc122-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc122-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc122-138">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="fc122-138">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

