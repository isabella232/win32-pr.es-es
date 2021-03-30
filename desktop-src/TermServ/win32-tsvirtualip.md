---
title: Win32_TSVirtualIP (clase)
description: Define la configuración de virtualización del Protocolo de Internet (IP) para un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualIP clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSVirtualIP de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f87db04d61dda0c6034b536544362ec09e0aaa66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801286"
---
# <a name="win32_tsvirtualip-class"></a><span data-ttu-id="024d2-105">\_Clase Win32 TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="024d2-105">Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="024d2-106">Define la configuración de virtualización del Protocolo de Internet (IP) para un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="024d2-106">Defines Internet protocol (IP) virtualization settings for a Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="024d2-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="024d2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="024d2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="024d2-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a><span data-ttu-id="024d2-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="024d2-109">Members</span></span>

<span data-ttu-id="024d2-110">La **clase \_ TSVirtualIP de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="024d2-110">The **Win32\_TSVirtualIP** class has these types of members:</span></span>

-   [<span data-ttu-id="024d2-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="024d2-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="024d2-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="024d2-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="024d2-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="024d2-113">Methods</span></span>

<span data-ttu-id="024d2-114">La clase **Win32 \_ TSVirtualIP** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="024d2-114">The **Win32\_TSVirtualIP** class has these methods.</span></span>



| <span data-ttu-id="024d2-115">Método</span><span class="sxs-lookup"><span data-stu-id="024d2-115">Method</span></span>                                                                                                   | <span data-ttu-id="024d2-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="024d2-116">Description</span></span>                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="024d2-117">**AddProgram**</span><span class="sxs-lookup"><span data-stu-id="024d2-117">**AddProgram**</span></span>](addprogram-win32-tsvirtualip.md)                                                       | <span data-ttu-id="024d2-118">Agrega un programa a la lista de programas que utilizan la virtualización de IP.</span><span class="sxs-lookup"><span data-stu-id="024d2-118">Adds a program to the list of programs that use IP virtualization.</span></span><br/>                                                                                                |
| [<span data-ttu-id="024d2-119">**RemoveProgram**</span><span class="sxs-lookup"><span data-stu-id="024d2-119">**RemoveProgram**</span></span>](removeprogram-win32-tsvirtualip.md)                                                 | <span data-ttu-id="024d2-120">Quita un programa de la lista de programas que utilizan la virtualización de IP.</span><span class="sxs-lookup"><span data-stu-id="024d2-120">Removes a program from the list of programs that use IP virtualization.</span></span><br/>                                                                                           |
| [<span data-ttu-id="024d2-121">**SelectNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="024d2-121">**SelectNetworkAdapter**</span></span>](selectnetworkadapter-win32-tsvirtualip.md)                                   | <span data-ttu-id="024d2-122">Establece la dirección MAC del adaptador de red que se va a usar para la virtualización de IP.</span><span class="sxs-lookup"><span data-stu-id="024d2-122">Sets the MAC address of the network adapter to use for IP virtualization.</span></span><br/>                                                                                         |
| [<span data-ttu-id="024d2-123">**SetProgramList**</span><span class="sxs-lookup"><span data-stu-id="024d2-123">**SetProgramList**</span></span>](setprogramlist-win32-tsvirtualip.md)                                               | <span data-ttu-id="024d2-124">Sobrescribe la lista de programas que utilizan la virtualización de IP.</span><span class="sxs-lookup"><span data-stu-id="024d2-124">Overwrites the list of programs that use IP virtualization.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="024d2-125">**SetVirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="024d2-125">**SetVirtualIPActive**</span></span>](setvirtualipactive-win32-tsvirtualip.md)                                       | <span data-ttu-id="024d2-126">Establece el valor de la propiedad **VirtualIPActive** .</span><span class="sxs-lookup"><span data-stu-id="024d2-126">Sets the **VirtualIPActive** property value.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="024d2-127">**SetVirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="024d2-127">**SetVirtualIPMode**</span></span>](setvirtualipmode-win32-tsvirtualip.md)                                           | <span data-ttu-id="024d2-128">Establece el valor de la propiedad **VirtualIPMode** .</span><span class="sxs-lookup"><span data-stu-id="024d2-128">Sets the **VirtualIPMode** property value.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="024d2-129">**SetVirtualizeLoopbackAddressesEnabled**</span><span class="sxs-lookup"><span data-stu-id="024d2-129">**SetVirtualizeLoopbackAddressesEnabled**</span></span>](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | <span data-ttu-id="024d2-130">Establece el valor de la propiedad **VirtualizeLoopbackAddressesEnabled** .</span><span class="sxs-lookup"><span data-stu-id="024d2-130">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span><br/> <span data-ttu-id="024d2-131">**Windows Server 2008 R2:** Este método no está disponible antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="024d2-131">**Windows Server 2008 R2:** This method is not available prior to Windows Server 2012.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="024d2-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="024d2-132">Properties</span></span>

<span data-ttu-id="024d2-133">La **clase \_ TSVirtualIP de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="024d2-133">The **Win32\_TSVirtualIP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="024d2-134">**Caption**</span><span class="sxs-lookup"><span data-stu-id="024d2-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="024d2-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="024d2-137">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="024d2-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="024d2-138">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="024d2-138">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="024d2-139">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="024d2-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="024d2-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="024d2-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="024d2-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-143">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="024d2-143">Description of the object.</span></span>

<span data-ttu-id="024d2-144">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="024d2-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="024d2-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="024d2-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-146">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="024d2-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="024d2-148">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="024d2-148">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="024d2-149">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="024d2-149">The date the object was installed.</span></span> <span data-ttu-id="024d2-150">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="024d2-150">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="024d2-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="024d2-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="024d2-152">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="024d2-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="024d2-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-155">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="024d2-155">The name of the object.</span></span>

<span data-ttu-id="024d2-156">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="024d2-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="024d2-157">**NetworkAdapterDescription**</span><span class="sxs-lookup"><span data-stu-id="024d2-157">**NetworkAdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="024d2-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-160">La descripción del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="024d2-160">The description for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="024d2-161">**NetworkAdapterDescriptionList**</span><span class="sxs-lookup"><span data-stu-id="024d2-161">**NetworkAdapterDescriptionList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-162">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="024d2-162">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="024d2-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-164">Lista de descripciones de los adaptadores de red físicos disponibles.</span><span class="sxs-lookup"><span data-stu-id="024d2-164">The list of descriptions of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="024d2-165">**NetworkAdapterMacAddress**</span><span class="sxs-lookup"><span data-stu-id="024d2-165">**NetworkAdapterMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="024d2-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-168">Dirección MAC del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="024d2-168">The MAC address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="024d2-169">**NetworkAdapterMacList**</span><span class="sxs-lookup"><span data-stu-id="024d2-169">**NetworkAdapterMacList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-170">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="024d2-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="024d2-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-172">La lista de direcciones MAC de los adaptadores de red físicos disponibles.</span><span class="sxs-lookup"><span data-stu-id="024d2-172">The list of MAC addresses of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="024d2-173">**PolicySourceNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="024d2-173">**PolicySourceNetworkAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-174">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="024d2-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-176">Indica si el adaptador de red está configurado por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="024d2-176">Indicates whether the network adapter is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="024d2-177">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="024d2-177">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="024d2-178">Servidor</span><span class="sxs-lookup"><span data-stu-id="024d2-178">Server</span></span>

</dd> <dt>

<span data-ttu-id="024d2-179">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="024d2-179">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="024d2-180">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="024d2-180">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="024d2-181">**PolicySourceProgramList**</span><span class="sxs-lookup"><span data-stu-id="024d2-181">**PolicySourceProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-182">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="024d2-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-184">Indica si la propiedad **ProgramList** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="024d2-184">Indicates whether the **ProgramList** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="024d2-185">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="024d2-185">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="024d2-186">Servidor</span><span class="sxs-lookup"><span data-stu-id="024d2-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="024d2-187">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="024d2-187">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="024d2-188">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="024d2-188">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="024d2-189">**PolicySourceVirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="024d2-189">**PolicySourceVirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-190">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="024d2-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-192">Indica si la propiedad **VirtualIPActive** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="024d2-192">Indicates if the **VirtualIPActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="024d2-193">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="024d2-193">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="024d2-194">Servidor</span><span class="sxs-lookup"><span data-stu-id="024d2-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="024d2-195">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="024d2-195">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="024d2-196">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="024d2-196">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="024d2-197">**PolicySourceVirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="024d2-197">**PolicySourceVirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-198">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="024d2-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-200">Indica si la propiedad **VirtualIPMode** está configurada por el servidor o por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="024d2-200">Indicates if the **VirtualIPMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="024d2-201">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="024d2-201">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="024d2-202">Servidor</span><span class="sxs-lookup"><span data-stu-id="024d2-202">Server</span></span>

</dd> <dt>

<span data-ttu-id="024d2-203">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="024d2-203">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="024d2-204">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="024d2-204">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="024d2-205">**ProgramList**</span><span class="sxs-lookup"><span data-stu-id="024d2-205">**ProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-206">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="024d2-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="024d2-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-208">Especifica los programas que están configurados para usar la virtualización de IP.</span><span class="sxs-lookup"><span data-stu-id="024d2-208">Specifies the programs that are configured to use IP virtualization.</span></span> <span data-ttu-id="024d2-209">Puede ser un nombre de programa o la ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="024d2-209">This may a program name or the full path.</span></span>

</dd> <dt>

<span data-ttu-id="024d2-210">**Estado**</span><span class="sxs-lookup"><span data-stu-id="024d2-210">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-211">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="024d2-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="024d2-213">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="024d2-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="024d2-214">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="024d2-214">Current status of the object.</span></span> <span data-ttu-id="024d2-215">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="024d2-215">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="024d2-216">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="024d2-216">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="024d2-217">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="024d2-217">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="024d2-218">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="024d2-218">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="024d2-219">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="024d2-219">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="024d2-220">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="024d2-220">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="024d2-221">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="024d2-221">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="024d2-222">("Error")</span><span class="sxs-lookup"><span data-stu-id="024d2-222">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="024d2-223">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="024d2-223">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="024d2-224">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="024d2-224">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="024d2-225">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="024d2-225">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="024d2-226">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="024d2-226">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="024d2-227">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="024d2-227">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="024d2-228">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="024d2-228">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="024d2-229">**VirtualIPActive**</span><span class="sxs-lookup"><span data-stu-id="024d2-229">**VirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-230">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="024d2-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="024d2-232">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="024d2-232">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="024d2-233">Especifica si la virtualización de IP está activa en el servidor.</span><span class="sxs-lookup"><span data-stu-id="024d2-233">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="024d2-234">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="024d2-234">This can be one of the following values.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="024d2-235"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="024d2-235"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="024d2-236">La virtualización de IP no está activa.</span><span class="sxs-lookup"><span data-stu-id="024d2-236">IP virtualization is not active.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="024d2-237"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="024d2-237"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="024d2-238">La virtualización de IP está activa.</span><span class="sxs-lookup"><span data-stu-id="024d2-238">IP virtualization is active.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="024d2-239">**VirtualIPMode**</span><span class="sxs-lookup"><span data-stu-id="024d2-239">**VirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-240">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="024d2-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-242">Especifica el modo de virtualización de IP que se utiliza en el servidor.</span><span class="sxs-lookup"><span data-stu-id="024d2-242">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="024d2-243">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="024d2-243">This can be one of the following values.</span></span>

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span data-ttu-id="024d2-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Por sesión** (0)</span><span class="sxs-lookup"><span data-stu-id="024d2-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Per-Session** (0)</span></span>


</dt> <dd>

<span data-ttu-id="024d2-245">El modo de virtualización de IP es por sesión.</span><span class="sxs-lookup"><span data-stu-id="024d2-245">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span data-ttu-id="024d2-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Por programa** (1)</span><span class="sxs-lookup"><span data-stu-id="024d2-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Per-Program** (1)</span></span>


</dt> <dd>

<span data-ttu-id="024d2-247">El modo de virtualización de IP es por usuario.</span><span class="sxs-lookup"><span data-stu-id="024d2-247">The IP virtualization mode is per-user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="024d2-248">**VirtualizeLoopbackAddressesEnabled**</span><span class="sxs-lookup"><span data-stu-id="024d2-248">**VirtualizeLoopbackAddressesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="024d2-249">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="024d2-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="024d2-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="024d2-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="024d2-251">Especifica si está habilitada la virtualización de la dirección de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="024d2-251">Specifies whether loopback address virtualization is enabled.</span></span>

<span data-ttu-id="024d2-252">**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="024d2-252">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="024d2-253"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="024d2-253"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="024d2-254">no habilitado.</span><span class="sxs-lookup"><span data-stu-id="024d2-254">Not enabled</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="024d2-255"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="024d2-255"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="024d2-256">habilitado</span><span class="sxs-lookup"><span data-stu-id="024d2-256">Enabled</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="024d2-257">Observaciones</span><span class="sxs-lookup"><span data-stu-id="024d2-257">Remarks</span></span>

<span data-ttu-id="024d2-258">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="024d2-258">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="024d2-259">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="024d2-259">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="024d2-260">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="024d2-260">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="024d2-261">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="024d2-261">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="024d2-262">Requisitos</span><span class="sxs-lookup"><span data-stu-id="024d2-262">Requirements</span></span>



| <span data-ttu-id="024d2-263">Requisito</span><span class="sxs-lookup"><span data-stu-id="024d2-263">Requirement</span></span> | <span data-ttu-id="024d2-264">Value</span><span class="sxs-lookup"><span data-stu-id="024d2-264">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="024d2-265">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="024d2-265">Minimum supported client</span></span><br/> | <span data-ttu-id="024d2-266">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="024d2-266">None supported</span></span><br/>                                                               |
| <span data-ttu-id="024d2-267">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="024d2-267">Minimum supported server</span></span><br/> | <span data-ttu-id="024d2-268">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="024d2-268">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="024d2-269">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="024d2-269">Namespace</span></span><br/>                | <span data-ttu-id="024d2-270">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="024d2-270">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="024d2-271">MOF</span><span class="sxs-lookup"><span data-stu-id="024d2-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="024d2-272"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="024d2-272"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="024d2-273">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="024d2-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="024d2-274"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="024d2-274"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

