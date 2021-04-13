---
title: Win32_RDMSCollectionProperties (clase)
description: Administra las propiedades de una colección de escritorios virtuales.
ms.assetid: 8c533284-aa7b-4c47-b0a3-33307c4c805b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSCollectionProperties clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDMSCollectionProperties de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties.Alias
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopMachineName
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopHost
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopGuid
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopOsversion
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRamsizeMB
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopArchitecture
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopRemoteFX
- Win32_RDMSCollectionProperties.ReferenceVirtualDesktopAdapters
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7397ccc1afd350689ac1eeb984a62177140f50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422208"
---
# <a name="win32_rdmscollectionproperties-class"></a><span data-ttu-id="3f98d-105">\_Clase Win32 RDMSCollectionProperties</span><span class="sxs-lookup"><span data-stu-id="3f98d-105">Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="3f98d-106">Administra las propiedades de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="3f98d-106">Manages the properties of a virtual desktop collection.</span></span>

<span data-ttu-id="3f98d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3f98d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f98d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f98d-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSCollectionProperties
{
  string  Alias;
  string  ReferenceVirtualDesktopName;
  string  ReferenceVirtualDesktopMachineName;
  string  ReferenceVirtualDesktopHost;
  string  ReferenceVirtualDesktopGuid;
  string  ReferenceVirtualDesktopOsversion;
  uint32  ReferenceVirtualDesktopRamsizeMB;
  string  ReferenceVirtualDesktopArchitecture;
  boolean ReferenceVirtualDesktopRemoteFX = false;
  string  ReferenceVirtualDesktopAdapters[];
};
```

## <a name="members"></a><span data-ttu-id="3f98d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3f98d-109">Members</span></span>

<span data-ttu-id="3f98d-110">La **clase \_ RDMSCollectionProperties de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3f98d-110">The **Win32\_RDMSCollectionProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="3f98d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f98d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3f98d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3f98d-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="3f98d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f98d-113">Methods</span></span>

<span data-ttu-id="3f98d-114">La clase **Win32 \_ RDMSCollectionProperties** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3f98d-114">The **Win32\_RDMSCollectionProperties** class has these methods.</span></span>



| <span data-ttu-id="3f98d-115">Método</span><span class="sxs-lookup"><span data-stu-id="3f98d-115">Method</span></span>                                                                                        | <span data-ttu-id="3f98d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f98d-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f98d-117">**GetProvisioningProperties**</span><span class="sxs-lookup"><span data-stu-id="3f98d-117">**GetProvisioningProperties**</span></span>](getprovisioningproperties-win32-rdmscollectionproperties.md) | <span data-ttu-id="3f98d-118">Recupera las propiedades de aprovisionamiento de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="3f98d-118">Retrieves the provisioning properties of the virtual desktop collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3f98d-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3f98d-119">Properties</span></span>

<span data-ttu-id="3f98d-120">La **clase \_ RDMSCollectionProperties de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3f98d-120">The **Win32\_RDMSCollectionProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f98d-121">**Alias**</span><span class="sxs-lookup"><span data-stu-id="3f98d-121">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f98d-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3f98d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f98d-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3f98d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f98d-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3f98d-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3f98d-125">Obtiene el alias de la colección.</span><span class="sxs-lookup"><span data-stu-id="3f98d-125">Gets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="3f98d-126">**ReferenceVirtualDesktopAdapters**</span><span class="sxs-lookup"><span data-stu-id="3f98d-126">**ReferenceVirtualDesktopAdapters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f98d-127">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3f98d-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3f98d-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f98d-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f98d-129">Obtiene y establece los nombres de los adaptadores de red virtual de la máquina virtual maestra.</span><span class="sxs-lookup"><span data-stu-id="3f98d-129">Gets and sets the names of the virtual network adapters of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="3f98d-130">**ReferenceVirtualDesktopArchitecture**</span><span class="sxs-lookup"><span data-stu-id="3f98d-130">**ReferenceVirtualDesktopArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f98d-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3f98d-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f98d-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f98d-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f98d-133">Obtiene y establece la arquitectura de procesador de la máquina virtual maestra.</span><span class="sxs-lookup"><span data-stu-id="3f98d-133">Gets and sets the processor architecture of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="3f98d-134">**ReferenceVirtualDesktopGuid**</span><span class="sxs-lookup"><span data-stu-id="3f98d-134">**ReferenceVirtualDesktopGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f98d-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3f98d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f98d-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f98d-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f98d-137">Obtiene y establece el GUID de la máquina virtual maestra.</span><span class="sxs-lookup"><span data-stu-id="3f98d-137">Gets and sets the GUID of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="3f98d-138">**ReferenceVirtualDesktopHost**</span><span class="sxs-lookup"><span data-stu-id="3f98d-138">**ReferenceVirtualDesktopHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f98d-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3f98d-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f98d-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f98d-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f98d-141">Obtiene y establece el nombre del servidor host de la máquina virtual maestra.</span><span class="sxs-lookup"><span data-stu-id="3f98d-141">Gets and sets the host server name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="3f98d-142">**ReferenceVirtualDesktopMachineName**</span><span class="sxs-lookup"><span data-stu-id="3f98d-142">**ReferenceVirtualDesktopMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f98d-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3f98d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f98d-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f98d-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f98d-145">Obtiene y establece el nombre de equipo de la máquina virtual maestra.</span><span class="sxs-lookup"><span data-stu-id="3f98d-145">Gets and sets the machine name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="3f98d-146">**ReferenceVirtualDesktopName**</span><span class="sxs-lookup"><span data-stu-id="3f98d-146">**ReferenceVirtualDesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f98d-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3f98d-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f98d-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f98d-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f98d-149">Obtiene y establece el nombre de la máquina virtual maestra.</span><span class="sxs-lookup"><span data-stu-id="3f98d-149">Gets and sets the name of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="3f98d-150">**ReferenceVirtualDesktopOsversion**</span><span class="sxs-lookup"><span data-stu-id="3f98d-150">**ReferenceVirtualDesktopOsversion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f98d-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3f98d-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f98d-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f98d-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f98d-153">Obtiene y establece la versión del sistema operativo de la máquina virtual maestra.</span><span class="sxs-lookup"><span data-stu-id="3f98d-153">Gets and sets the OS version of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="3f98d-154">**ReferenceVirtualDesktopRamsizeMB**</span><span class="sxs-lookup"><span data-stu-id="3f98d-154">**ReferenceVirtualDesktopRamsizeMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f98d-155">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f98d-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f98d-156">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f98d-156">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f98d-157">Obtiene y establece el tamaño de memoria de la máquina virtual maestra.</span><span class="sxs-lookup"><span data-stu-id="3f98d-157">Gets and sets the memory size of the master VM.</span></span>

</dd> <dt>

<span data-ttu-id="3f98d-158">**ReferenceVirtualDesktopRemoteFX**</span><span class="sxs-lookup"><span data-stu-id="3f98d-158">**ReferenceVirtualDesktopRemoteFX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f98d-159">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3f98d-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f98d-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3f98d-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f98d-161">Obtiene y establece un valor que indica si RemoteFX está habilitado para la máquina virtual maestra.</span><span class="sxs-lookup"><span data-stu-id="3f98d-161">Gets and sets a value that indicates whether RemoteFX is enabled for the master VM.</span></span> <span data-ttu-id="3f98d-162">**True** si RemoteFX está habilitado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="3f98d-162">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span> <span data-ttu-id="3f98d-163">El valor predeterminado de esta propiedad es **false**.</span><span class="sxs-lookup"><span data-stu-id="3f98d-163">The default value for this property is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f98d-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f98d-164">Requirements</span></span>



| <span data-ttu-id="3f98d-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f98d-165">Requirement</span></span> | <span data-ttu-id="3f98d-166">Value</span><span class="sxs-lookup"><span data-stu-id="3f98d-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f98d-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f98d-167">Minimum supported client</span></span><br/> | <span data-ttu-id="3f98d-168">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3f98d-168">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3f98d-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f98d-169">Minimum supported server</span></span><br/> | <span data-ttu-id="3f98d-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f98d-170">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="3f98d-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f98d-171">Namespace</span></span><br/>                | <span data-ttu-id="3f98d-172">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="3f98d-172">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3f98d-173">MOF</span><span class="sxs-lookup"><span data-stu-id="3f98d-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f98d-174"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f98d-174"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f98d-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f98d-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f98d-176"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f98d-176"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3f98d-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f98d-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f98d-178">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="3f98d-178">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

