---
description: Representa un intervalo contiguo de bloques lógicos que un sistema de archivos identifica mediante el campo DeviceID (clave) de los discos.
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: CIM_LogicalDisk (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7305d0fa6ef45b5a97eb0fb6ab9ea740c98a392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002491"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a><span data-ttu-id="52bd6-103">CIM_LogicalDisk (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="52bd6-103">CIM_LogicalDisk class (Hyper-V management)</span></span>

<span data-ttu-id="52bd6-104">Representa un intervalo contiguo de bloques lógicos que un sistema de archivos identifica mediante el campo de **DeviceID** (clave) del disco.</span><span class="sxs-lookup"><span data-stu-id="52bd6-104">Represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="52bd6-105">Por ejemplo, en un entorno de Windows, el campo **DeviceID** contiene una letra de unidad; en un entorno de UNIX, contiene la ruta de acceso; y en un entorno de NetWare, contiene el nombre del volumen.</span><span class="sxs-lookup"><span data-stu-id="52bd6-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

## <a name="syntax"></a><span data-ttu-id="52bd6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52bd6-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a><span data-ttu-id="52bd6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="52bd6-107">Members</span></span>

<span data-ttu-id="52bd6-108">La clase de **\_ LogicalDisk de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="52bd6-108">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="52bd6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="52bd6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52bd6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="52bd6-110">Properties</span></span>

<span data-ttu-id="52bd6-111">La clase de **\_ LogicalDisk de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="52bd6-111">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52bd6-112">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="52bd6-112">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52bd6-113">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52bd6-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52bd6-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52bd6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52bd6-115">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="52bd6-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="52bd6-116">Indica si el dispositivo lógico usa el formato de nombre del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="52bd6-116">Indicates whether the logical device uses the name format of the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="52bd6-117">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="52bd6-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="52bd6-118">**Nombre del dispositivo de SO** (12)</span><span class="sxs-lookup"><span data-stu-id="52bd6-118">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="52bd6-119">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="52bd6-119">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52bd6-120">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52bd6-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52bd6-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52bd6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52bd6-122">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")</span><span class="sxs-lookup"><span data-stu-id="52bd6-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")</span></span>
</dt> </dl>

<span data-ttu-id="52bd6-123">Indica si el dispositivo lógico tiene el mismo espacio de nombres que el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="52bd6-123">Indicates whether the logical device has the same namespace as the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="52bd6-124">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="52bd6-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="52bd6-125">**Espacio de nombres de dispositivo de SO** (8)</span><span class="sxs-lookup"><span data-stu-id="52bd6-125">**OS Device Namespace** (8)</span></span>


<span data-ttu-id="52bd6-126"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="52bd6-126"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="52bd6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52bd6-127">Requirements</span></span>



| <span data-ttu-id="52bd6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="52bd6-128">Requirement</span></span> | <span data-ttu-id="52bd6-129">Value</span><span class="sxs-lookup"><span data-stu-id="52bd6-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52bd6-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52bd6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="52bd6-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="52bd6-131">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="52bd6-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52bd6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="52bd6-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52bd6-133">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="52bd6-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="52bd6-134">Namespace</span></span><br/>                | <span data-ttu-id="52bd6-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="52bd6-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="52bd6-136">MOF</span><span class="sxs-lookup"><span data-stu-id="52bd6-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52bd6-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52bd6-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="52bd6-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52bd6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52bd6-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="52bd6-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="52bd6-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="52bd6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52bd6-141">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="52bd6-141">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

