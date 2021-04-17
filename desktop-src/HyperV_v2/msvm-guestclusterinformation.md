---
description: Se usa en el método QueryGuestClusterInformation de la \_ clase MSVM VssService para recuperar información sobre el clúster invitado del que forma parte la máquina virtual.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Msvm_GuestClusterInformation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686953"
---
# <a name="msvm_guestclusterinformation-class"></a><span data-ttu-id="c4959-103">MSVM \_ GuestClusterInformation (clase)</span><span class="sxs-lookup"><span data-stu-id="c4959-103">Msvm\_GuestClusterInformation class</span></span>

<span data-ttu-id="c4959-104">Se usa en el método [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) de la clase [**MSVM \_ VssService**](msvm-vssservice.md) para recuperar información sobre el clúster invitado del que forma parte la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4959-104">Used in the [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) method in the [**Msvm\_VssService**](msvm-vssservice.md) class to retrieve information about the guest cluster the VM is part of.</span></span>

<span data-ttu-id="c4959-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c4959-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4959-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4959-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a><span data-ttu-id="c4959-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c4959-107">Members</span></span>

<span data-ttu-id="c4959-108">La clase **MSVM \_ GuestClusterInformation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c4959-108">The **Msvm\_GuestClusterInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="c4959-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c4959-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4959-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c4959-110">Properties</span></span>

<span data-ttu-id="c4959-111">La clase **MSVM \_ GuestClusterInformation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c4959-111">The **Msvm\_GuestClusterInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4959-112">**ClusterId**</span><span class="sxs-lookup"><span data-stu-id="c4959-112">**ClusterId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4959-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c4959-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4959-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4959-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4959-115">El identificador del clúster de conmutación por error del que forma parte el sistema operativo invitado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4959-115">The identifier of the failover cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="c4959-116">**ClusterSize**</span><span class="sxs-lookup"><span data-stu-id="c4959-116">**ClusterSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4959-117">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4959-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4959-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4959-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4959-119">Número de nodos del clúster del que forma parte el sistema operativo invitado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4959-119">Number of nodes in the cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="c4959-120">**IsActiveActive**</span><span class="sxs-lookup"><span data-stu-id="c4959-120">**IsActiveActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4959-121">Tipo de datos: matriz **booleana**</span><span class="sxs-lookup"><span data-stu-id="c4959-121">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="c4959-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4959-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4959-123">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c4959-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c4959-124">Matriz de valores booleanos que corresponden a cada disco duro virtual compartido que indica si el recurso de disco correspondiente en el clúster invitado se comparte entre las máquinas virtuales en modo activo/activo.</span><span class="sxs-lookup"><span data-stu-id="c4959-124">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is shared between VMs in active/active mode.</span></span>

</dd> <dt>

<span data-ttu-id="c4959-125">**IsClustered**</span><span class="sxs-lookup"><span data-stu-id="c4959-125">**IsClustered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4959-126">Tipo de datos: matriz **booleana**</span><span class="sxs-lookup"><span data-stu-id="c4959-126">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="c4959-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4959-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4959-128">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c4959-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c4959-129">Matriz de valores booleanos que corresponden a cada disco duro virtual compartido que indica si el disco correspondiente es un recurso de clúster en el clúster invitado.</span><span class="sxs-lookup"><span data-stu-id="c4959-129">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk is a cluster resource in the guest cluster.</span></span>

</dd> <dt>

<span data-ttu-id="c4959-130">**IsOnline**</span><span class="sxs-lookup"><span data-stu-id="c4959-130">**IsOnline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4959-131">Tipo de datos: matriz **booleana**</span><span class="sxs-lookup"><span data-stu-id="c4959-131">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="c4959-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4959-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4959-133">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c4959-133">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c4959-134">Matriz de valores booleanos que corresponden a cada disco duro virtual compartido que indica si el recurso de disco correspondiente en el clúster invitado está en línea.</span><span class="sxs-lookup"><span data-stu-id="c4959-134">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is online.</span></span>

</dd> <dt>

<span data-ttu-id="c4959-135">**IsOwned**</span><span class="sxs-lookup"><span data-stu-id="c4959-135">**IsOwned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4959-136">Tipo de datos: matriz **booleana**</span><span class="sxs-lookup"><span data-stu-id="c4959-136">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="c4959-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4959-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4959-138">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c4959-138">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c4959-139">Matriz de valores booleanos que corresponden a cada disco duro virtual compartido que indica si el recurso de disco correspondiente en el clúster invitado es Currenly propiedad de esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4959-139">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is currenly owned by this VM.</span></span>

</dd> <dt>

<span data-ttu-id="c4959-140">**LastResourceMoveTime**</span><span class="sxs-lookup"><span data-stu-id="c4959-140">**LastResourceMoveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4959-141">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4959-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4959-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4959-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4959-143">El contador del reloj cuando uno de los recursos del disco compartido se desplazó por última vez.</span><span class="sxs-lookup"><span data-stu-id="c4959-143">The clock tick count when one of the shared disk resources last moved.</span></span>

> [!Note]  
> <span data-ttu-id="c4959-144">Esta propiedad se agregó en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="c4959-144">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="c4959-145">**SharedVirtualHardDiskPaths**</span><span class="sxs-lookup"><span data-stu-id="c4959-145">**SharedVirtualHardDiskPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4959-146">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c4959-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4959-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4959-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4959-148">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c4959-148">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c4959-149">Una matriz de rutas de acceso de disco duro virtual compartidas conectadas a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4959-149">An array of shared virtual hard disk paths connected to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="c4959-150">**SharedVirtualHardDisks**</span><span class="sxs-lookup"><span data-stu-id="c4959-150">**SharedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4959-151">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c4959-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4959-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4959-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4959-153">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c4959-153">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c4959-154">Una matriz de datos de configuración de asignación de recursos (RASD) que representa los discos duros virtuales compartidos conectados a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4959-154">An array of Resource Allocation Setting Data (RASD) representing the shared virtual hard disks connected to the VM.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4959-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4959-155">Requirements</span></span>



| <span data-ttu-id="c4959-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4959-156">Requirement</span></span> | <span data-ttu-id="c4959-157">Value</span><span class="sxs-lookup"><span data-stu-id="c4959-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4959-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4959-158">Minimum supported client</span></span><br/> | <span data-ttu-id="c4959-159">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4959-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c4959-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4959-160">Minimum supported server</span></span><br/> | <span data-ttu-id="c4959-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c4959-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c4959-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c4959-162">Namespace</span></span><br/>                | <span data-ttu-id="c4959-163">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c4959-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c4959-164">MOF</span><span class="sxs-lookup"><span data-stu-id="c4959-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4959-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4959-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4959-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4959-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4959-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4959-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

