---
description: Proporciona datos de configuración para un disco duro virtual.
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Msvm_VirtualHardDiskSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e13efbb068d15ca4051995e7d9f317eb2ccacab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153892"
---
# <a name="msvm_virtualharddisksettingdata-class"></a><span data-ttu-id="add2b-103">MSVM \_ VirtualHardDiskSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="add2b-103">Msvm\_VirtualHardDiskSettingData class</span></span>

<span data-ttu-id="add2b-104">Proporciona datos de configuración para un disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="add2b-104">Provides setting data for a virtual hard disk.</span></span>

<span data-ttu-id="add2b-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="add2b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="add2b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="add2b-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a><span data-ttu-id="add2b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="add2b-107">Members</span></span>

<span data-ttu-id="add2b-108">La clase **MSVM \_ VirtualHardDiskSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="add2b-108">The **Msvm\_VirtualHardDiskSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="add2b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="add2b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="add2b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="add2b-110">Properties</span></span>

<span data-ttu-id="add2b-111">La clase **MSVM \_ VirtualHardDiskSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="add2b-111">The **Msvm\_VirtualHardDiskSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="add2b-112">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="add2b-112">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="add2b-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-115">Tamaño de bloque usado por el disco duro virtual, en bytes.</span><span class="sxs-lookup"><span data-stu-id="add2b-115">The block size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="add2b-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="add2b-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="add2b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="add2b-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="add2b-119">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="add2b-119">A short description of the object.</span></span> <span data-ttu-id="add2b-120">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "datos de configuración de disco duro virtual".</span><span class="sxs-lookup"><span data-stu-id="add2b-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Hard Disk Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="add2b-121">**Alineación de los mismos**</span><span class="sxs-lookup"><span data-stu-id="add2b-121">**DataAlignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-122">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="add2b-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-124">Especifica la alineación deseada, en bytes, para la carga de datos del disco virtual.</span><span class="sxs-lookup"><span data-stu-id="add2b-124">Specifies the desired alignment, in bytes, for the data payload of the virtual disk</span></span>

> [!Note]  
> <span data-ttu-id="add2b-125">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="add2b-125">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="add2b-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="add2b-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="add2b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="add2b-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="add2b-129">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="add2b-129">A description of the object.</span></span> <span data-ttu-id="add2b-130">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "establecer datos para un disco duro virtual".</span><span class="sxs-lookup"><span data-stu-id="add2b-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Setting Data for a Virtual Hard Disk".</span></span>

</dd> <dt>

<span data-ttu-id="add2b-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="add2b-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="add2b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="add2b-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="add2b-134">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="add2b-134">A display name for the object.</span></span> <span data-ttu-id="add2b-135">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="add2b-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="add2b-136">**Format**</span><span class="sxs-lookup"><span data-stu-id="add2b-136">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-137">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="add2b-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-139">El formato del disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="add2b-139">The format for the virtual hard disk.</span></span> <span data-ttu-id="add2b-140">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="add2b-140">This will be one of the following values.</span></span>

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span data-ttu-id="add2b-141"><span id="VHD"></span><span id="vhd"></span>**VHD** (2)</span><span class="sxs-lookup"><span data-stu-id="add2b-141"><span id="VHD"></span><span id="vhd"></span>**VHD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span data-ttu-id="add2b-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span><span class="sxs-lookup"><span data-stu-id="add2b-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span data-ttu-id="add2b-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)</span><span class="sxs-lookup"><span data-stu-id="add2b-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="add2b-144">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="add2b-144">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="add2b-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="add2b-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="add2b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="add2b-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="add2b-148">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="add2b-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="add2b-149">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="add2b-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="add2b-150">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="add2b-150">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="add2b-151">**IsPmemCompatible**</span><span class="sxs-lookup"><span data-stu-id="add2b-151">**IsPmemCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-152">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="add2b-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-154">Especifica si el disco virtual se puede usar como memoria auxiliar para un dispositivo de memoria persistente.</span><span class="sxs-lookup"><span data-stu-id="add2b-154">Specifies whether the virtual disk can be used as the backing store for a persistent memory device.</span></span>

> [!Note]  
> <span data-ttu-id="add2b-155">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="add2b-155">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="add2b-156">**LogicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="add2b-156">**LogicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="add2b-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-159">Tamaño del sector lógico usado por el disco duro virtual, en bytes.</span><span class="sxs-lookup"><span data-stu-id="add2b-159">The logical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="add2b-160">**MaxInternalSize**</span><span class="sxs-lookup"><span data-stu-id="add2b-160">**MaxInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-161">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="add2b-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-162">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-163">El tamaño máximo del disco duro virtual tal como lo ve la máquina virtual, en bytes.</span><span class="sxs-lookup"><span data-stu-id="add2b-163">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="add2b-164">Este tamaño se redondeará al siguiente múltiplo más grande del tamaño del sector.</span><span class="sxs-lookup"><span data-stu-id="add2b-164">This size will be rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="add2b-165">**ParentIdentifier**</span><span class="sxs-lookup"><span data-stu-id="add2b-165">**ParentIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="add2b-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="add2b-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="add2b-168">GUID que se usa para identificar de forma única el elemento primario del disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="add2b-168">The GUID used to uniquely identify the parent of the virtual hard disk.</span></span> <span data-ttu-id="add2b-169">Si el disco duro virtual no tiene un elemento primario, este campo estará vacío.</span><span class="sxs-lookup"><span data-stu-id="add2b-169">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="add2b-170">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="add2b-170">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="add2b-171">**ParentPath**</span><span class="sxs-lookup"><span data-stu-id="add2b-171">**ParentPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="add2b-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-174">El elemento primario del disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="add2b-174">The parent of the virtual hard disk.</span></span> <span data-ttu-id="add2b-175">Si el disco duro virtual no tiene un elemento primario, esta propiedad está vacía.</span><span class="sxs-lookup"><span data-stu-id="add2b-175">If the virtual hard disk does not have a parent, then this property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="add2b-176">**ParentTimestamp**</span><span class="sxs-lookup"><span data-stu-id="add2b-176">**ParentTimestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-177">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="add2b-177">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="add2b-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="add2b-179">Marca de tiempo del elemento primario del disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="add2b-179">The timestamp of the parent of the virtual hard disk.</span></span> <span data-ttu-id="add2b-180">Si el disco duro virtual no tiene un elemento primario, este campo estará vacío.</span><span class="sxs-lookup"><span data-stu-id="add2b-180">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="add2b-181">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="add2b-181">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="add2b-182">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="add2b-182">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="add2b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-185">Ruta de acceso completa del disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="add2b-185">The fully qualified path of the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="add2b-186">**PhysicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="add2b-186">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-187">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="add2b-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-188">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-189">Tamaño de sector físico utilizado por el disco duro virtual, en bytes.</span><span class="sxs-lookup"><span data-stu-id="add2b-189">The physical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="add2b-190">**PmemAddressAbstractionType**</span><span class="sxs-lookup"><span data-stu-id="add2b-190">**PmemAddressAbstractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-191">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="add2b-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-192">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-193">Método de abstracción de dirección de memoria persistente que se va a usar con este disco virtual.</span><span class="sxs-lookup"><span data-stu-id="add2b-193">The persistent memory address abstraction method to be used with this virtual disk.</span></span>

> [!Note]  
> <span data-ttu-id="add2b-194">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="add2b-194">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="add2b-195">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="add2b-195">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

<span data-ttu-id="add2b-196">**BTT** (1)</span><span class="sxs-lookup"><span data-stu-id="add2b-196">**BTT** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="add2b-197">**Desconocido** (65535)</span><span class="sxs-lookup"><span data-stu-id="add2b-197">**Unknown** (65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="add2b-198">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="add2b-198">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-199">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="add2b-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-200">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-201">El tipo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="add2b-201">The type of virtual hard disk.</span></span> <span data-ttu-id="add2b-202">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="add2b-202">This will be one of the following values.</span></span>

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="add2b-203">**Fijo** (2)</span><span class="sxs-lookup"><span data-stu-id="add2b-203">**Fixed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

<span data-ttu-id="add2b-204">**Dinámico** (3)</span><span class="sxs-lookup"><span data-stu-id="add2b-204">**Dynamic** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

<span data-ttu-id="add2b-205">**Diferenciación** (4)</span><span class="sxs-lookup"><span data-stu-id="add2b-205">**Differencing** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="add2b-206">**VirtualDiskId**</span><span class="sxs-lookup"><span data-stu-id="add2b-206">**VirtualDiskId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="add2b-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="add2b-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="add2b-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="add2b-208">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="add2b-209">GUID que se usa para identificar de forma única el disco virtual.</span><span class="sxs-lookup"><span data-stu-id="add2b-209">The GUID that is used to uniquely identify the virtual disk.</span></span>

<span data-ttu-id="add2b-210">Cuando el método [**MSVM \_ ImageManagementService. GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) devuelve una instancia de **MSVM \_ VirtualHardDiskSettingData**, el cliente puede usar esta propiedad para obtener el identificador de disco único del VHD.</span><span class="sxs-lookup"><span data-stu-id="add2b-210">When the [**Msvm\_ImageManagementService.GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) method returns an instance of **Msvm\_VirtualHardDiskSettingData**, the client can use this property to get the unique disk ID of the VHD.</span></span>

<span data-ttu-id="add2b-211">En la detección de conflictos o de lo contrario, un cliente puede establecer el valor de **VirtualDiskId** en un nuevo GUID y pasar esta instancia de **MSVM \_ VirtualHardDiskSettingData** al método [**MSVM \_ ImageManagementService. SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) para cambiar el identificador de disco del VHD.</span><span class="sxs-lookup"><span data-stu-id="add2b-211">On conflict detection or otherwise, a client can set the **VirtualDiskId** value to a new GUID and pass this **Msvm\_VirtualHardDiskSettingData** instance to the [**Msvm\_ImageManagementService.SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) method to change the disk ID of the VHD.</span></span> <span data-ttu-id="add2b-212">Si el disco duro virtual no es un VHD VHDX o si el VHD está conectado, se produce un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="add2b-212">If the VHD is not a VHDX VHD, or if the VHD is attached, the operation fails.</span></span> <span data-ttu-id="add2b-213">También se produce un error en la operación si el valor pasado tiene un formato incorrecto, es decir, no un GUID o tiene todos 0.</span><span class="sxs-lookup"><span data-stu-id="add2b-213">The operation also fails if the passed value is malformed, that is, not a GUID or has all 0s.</span></span> <span data-ttu-id="add2b-214">La operación se realiza de forma silenciosa si el valor pasado es igual que el identificador de disco actual.</span><span class="sxs-lookup"><span data-stu-id="add2b-214">The operation silently succeeds if the passed value is the same as the current disk ID.</span></span>

<span data-ttu-id="add2b-215">Los errores generados por la función [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) se propagan a través de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="add2b-215">Errors generated by the [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) function are bubbled up through this property.</span></span> <span data-ttu-id="add2b-216">Un cliente también puede usar el mismo mecanismo para proporcionar el valor de **VirtualDiskId** en el VHD que se crea mediante el método [**MSVM \_ ImageManagementService. CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) en el mismo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="add2b-216">A client can also use the same mechanism to provide the **VirtualDiskId** value at VHD creation via the [**Msvm\_ImageManagementService.CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) method in the same namespace.</span></span> <span data-ttu-id="add2b-217">Se puede usar para crear VHD de VHD1 o VHD2.</span><span class="sxs-lookup"><span data-stu-id="add2b-217">This can be used to create VHD1 or VHD2 VHDs.</span></span>

<span data-ttu-id="add2b-218">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="add2b-218">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="add2b-219">Requisitos</span><span class="sxs-lookup"><span data-stu-id="add2b-219">Requirements</span></span>



| <span data-ttu-id="add2b-220">Requisito</span><span class="sxs-lookup"><span data-stu-id="add2b-220">Requirement</span></span> | <span data-ttu-id="add2b-221">Value</span><span class="sxs-lookup"><span data-stu-id="add2b-221">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="add2b-222">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="add2b-222">Minimum supported client</span></span><br/> | <span data-ttu-id="add2b-223">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="add2b-223">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="add2b-224">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="add2b-224">Minimum supported server</span></span><br/> | <span data-ttu-id="add2b-225">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="add2b-225">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="add2b-226">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="add2b-226">Namespace</span></span><br/>                | <span data-ttu-id="add2b-227">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="add2b-227">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="add2b-228">MOF</span><span class="sxs-lookup"><span data-stu-id="add2b-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="add2b-229"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="add2b-229"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="add2b-230">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="add2b-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="add2b-231"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="add2b-231"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="add2b-232">Vea también</span><span class="sxs-lookup"><span data-stu-id="add2b-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add2b-233">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="add2b-233">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="add2b-234">**GetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="add2b-234">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

