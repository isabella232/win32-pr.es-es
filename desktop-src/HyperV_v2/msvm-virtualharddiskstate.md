---
description: Proporciona información de estado de una imagen de disco duro virtual existente.
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Msvm_VirtualHardDiskState (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15d0a8b150e83c17946a6d1b66c7086383f08466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497020"
---
# <a name="msvm_virtualharddiskstate-class"></a><span data-ttu-id="c809c-103">MSVM \_ VirtualHardDiskState (clase)</span><span class="sxs-lookup"><span data-stu-id="c809c-103">Msvm\_VirtualHardDiskState class</span></span>

<span data-ttu-id="c809c-104">Proporciona información de estado de una imagen de disco duro virtual existente.</span><span class="sxs-lookup"><span data-stu-id="c809c-104">Provides state information for an existing virtual hard disk image.</span></span>

<span data-ttu-id="c809c-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c809c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c809c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c809c-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a><span data-ttu-id="c809c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c809c-107">Members</span></span>

<span data-ttu-id="c809c-108">La clase **MSVM \_ VirtualHardDiskState** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c809c-108">The **Msvm\_VirtualHardDiskState** class has these types of members:</span></span>

-   [<span data-ttu-id="c809c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c809c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c809c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c809c-110">Properties</span></span>

<span data-ttu-id="c809c-111">La clase **MSVM \_ VirtualHardDiskState** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c809c-111">The **Msvm\_VirtualHardDiskState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c809c-112">**Alineación**</span><span class="sxs-lookup"><span data-stu-id="c809c-112">**Alignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c809c-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c809c-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c809c-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c809c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c809c-115">Especifica el tipo de alineación del disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="c809c-115">Specifies the type of alignment of the virtual hard disk.</span></span> <span data-ttu-id="c809c-116">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c809c-116">This will be one of the following values.</span></span>



| <span data-ttu-id="c809c-117">Value</span><span class="sxs-lookup"><span data-stu-id="c809c-117">Value</span></span>                                                                        | <span data-ttu-id="c809c-118">Significado</span><span class="sxs-lookup"><span data-stu-id="c809c-118">Meaning</span></span>                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="c809c-119"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c809c-119"><dt>0</dt></span></span> </dl> | <span data-ttu-id="c809c-120">alineación de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="c809c-120">512 byte alignment.</span></span><br/> |
| <dl> <span data-ttu-id="c809c-121"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c809c-121"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c809c-122">alineación de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="c809c-122">4 KB alignment.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="c809c-123">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="c809c-123">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c809c-124">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c809c-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c809c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c809c-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c809c-126">El tamaño del archivo de disco duro virtual (la cantidad real de almacenamiento utilizado por el archivo), en bytes.</span><span class="sxs-lookup"><span data-stu-id="c809c-126">The size of the virtual hard disk file (the actual amount of storage being consumed by the file), in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c809c-127">**FragmentationPercentage**</span><span class="sxs-lookup"><span data-stu-id="c809c-127">**FragmentationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c809c-128">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c809c-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c809c-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c809c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c809c-130">Una aproximación del porcentaje de bloques de disco virtual que se fragmentan en el archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="c809c-130">An approximation of the percentage of virtual disk blocks that are fragmented in the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="c809c-131">**Property**</span><span class="sxs-lookup"><span data-stu-id="c809c-131">**InUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c809c-132">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c809c-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c809c-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c809c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c809c-134">Esta propiedad está reservada para un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c809c-134">This property is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="c809c-135">**MinInternalSize**</span><span class="sxs-lookup"><span data-stu-id="c809c-135">**MinInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c809c-136">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c809c-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c809c-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c809c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c809c-138">El tamaño mínimo que puede reducir el disco duro virtual, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c809c-138">The minimum size that the virtual hard disk can be shrunk to, in bytes.</span></span> <span data-ttu-id="c809c-139">Este tamaño se redondea hasta el siguiente múltiplo más grande del tamaño del sector.</span><span class="sxs-lookup"><span data-stu-id="c809c-139">This size is rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="c809c-140">**PhysicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="c809c-140">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c809c-141">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c809c-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c809c-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c809c-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c809c-143">Tamaño de sector físico utilizado por el disco físico subyacente, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c809c-143">The physical sector size used by the underlying physical disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c809c-144">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="c809c-144">**Timestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c809c-145">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c809c-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="c809c-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c809c-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c809c-147">La marca de tiempo del disco duro virtual</span><span class="sxs-lookup"><span data-stu-id="c809c-147">The timestamp of the virtual hard disk</span></span>

> [!Note]  
> <span data-ttu-id="c809c-148">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="c809c-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c809c-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c809c-149">Requirements</span></span>



| <span data-ttu-id="c809c-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="c809c-150">Requirement</span></span> | <span data-ttu-id="c809c-151">Value</span><span class="sxs-lookup"><span data-stu-id="c809c-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c809c-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c809c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c809c-153">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c809c-153">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c809c-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c809c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c809c-155">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c809c-155">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c809c-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c809c-156">Namespace</span></span><br/>                | <span data-ttu-id="c809c-157">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c809c-157">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c809c-158">MOF</span><span class="sxs-lookup"><span data-stu-id="c809c-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c809c-159"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c809c-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c809c-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c809c-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c809c-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c809c-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c809c-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="c809c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c809c-163">**GetVirtualHardDiskState**</span><span class="sxs-lookup"><span data-stu-id="c809c-163">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




