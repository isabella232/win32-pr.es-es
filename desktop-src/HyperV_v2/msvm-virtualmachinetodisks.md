---
description: Establecer los datos que se van a pasar como una matriz a la \_ clase MSVM CollectionReferencePointExportSettingData.
ms.assetid: f127880f-f917-4069-a283-a6f9427c5e07
title: Msvm_VirtualMachineToDisks (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualMachineToDisks
- Msvm_VirtualMachineToDisks.VirtualMachineId
- Msvm_VirtualMachineToDisks.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cad5de9389b9cb1d5e7db0573f3a4e3fc271ba31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907699"
---
# <a name="msvm_virtualmachinetodisks-class"></a><span data-ttu-id="128ca-103">MSVM \_ VirtualMachineToDisks (clase)</span><span class="sxs-lookup"><span data-stu-id="128ca-103">Msvm\_VirtualMachineToDisks class</span></span>

<span data-ttu-id="128ca-104">Establecer los datos que se van a pasar como una matriz a la clase [**MSVM \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="128ca-104">Setting data to be passed as an array to the [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) class.</span></span>

<span data-ttu-id="128ca-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="128ca-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="128ca-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="128ca-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualMachineToDisks
{
  string VirtualMachineId;
  string DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="128ca-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="128ca-107">Members</span></span>

<span data-ttu-id="128ca-108">La clase **MSVM \_ VirtualMachineToDisks** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="128ca-108">The **Msvm\_VirtualMachineToDisks** class has these types of members:</span></span>

-   [<span data-ttu-id="128ca-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="128ca-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="128ca-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="128ca-110">Properties</span></span>

<span data-ttu-id="128ca-111">La clase **MSVM \_ VirtualMachineToDisks** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="128ca-111">The **Msvm\_VirtualMachineToDisks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="128ca-112">**DisksToExport**</span><span class="sxs-lookup"><span data-stu-id="128ca-112">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="128ca-113">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="128ca-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="128ca-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="128ca-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="128ca-115">Los identificadores de instancia de WMI de los discos que pertenecen a un ID. de máquina virtual determinado para el que se deben exportar los datos.</span><span class="sxs-lookup"><span data-stu-id="128ca-115">The WMI instance IDs of the disks those belong to given Virtual Machine ID for which data needs to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="128ca-116">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="128ca-116">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="128ca-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="128ca-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="128ca-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="128ca-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="128ca-119">Un ID. de máquina virtual al que están asociados los discos virtuales.</span><span class="sxs-lookup"><span data-stu-id="128ca-119">A Virtual Machine ID that virtual disks are associated with.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="128ca-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="128ca-120">Requirements</span></span>



| <span data-ttu-id="128ca-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="128ca-121">Requirement</span></span> | <span data-ttu-id="128ca-122">Value</span><span class="sxs-lookup"><span data-stu-id="128ca-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="128ca-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="128ca-123">Minimum supported client</span></span><br/> | <span data-ttu-id="128ca-124">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="128ca-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="128ca-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="128ca-125">Minimum supported server</span></span><br/> | <span data-ttu-id="128ca-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="128ca-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="128ca-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="128ca-127">Namespace</span></span><br/>                | <span data-ttu-id="128ca-128">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="128ca-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="128ca-129">MOF</span><span class="sxs-lookup"><span data-stu-id="128ca-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="128ca-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="128ca-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="128ca-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="128ca-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="128ca-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="128ca-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




