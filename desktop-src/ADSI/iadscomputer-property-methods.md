---
title: Métodos de la propiedad IADsComputer (iAds. h)
description: Los métodos de la interfaz IADsComputer leen y escriben las propiedades descritas en este tema. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: c990b6bb-6256-4216-9435-c85c67db4d13
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsComputer ADSI
topic_type:
- apiref
api_name:
- IADsComputer Property Methods
- IADsComputer.ComputerID
- IADsComputer.get_ComputerID
- IADsComputer.Department
- IADsComputer.get_Department
- IADsComputer.put_Department
- IADsComputer.Description
- IADsComputer.get_Description
- IADsComputer.put_Description
- IADsComputer.Division
- IADsComputer.get_Division
- IADsComputer.put_Division
- IADsComputer.Location
- IADsComputer.get_Location
- IADsComputer.put_Location
- IADsComputer.MemorySize
- IADsComputer.get_MemorySize
- IADsComputer.put_MemorySize
- IADsComputer.Model
- IADsComputer.get_Model
- IADsComputer.put_Model
- IADsComputer.NetAddresses
- IADsComputer.get_NetAddresses
- IADsComputer.put_NetAddresses
- IADsComputer.OperatingSystem
- IADsComputer.get_OperatingSystem
- IADsComputer.put_OperatingSystem
- IADsComputer.OperatingSystemVersion
- IADsComputer.get_OperatingSystemVersion
- IADsComputer.put_OperatingSystemVersion
- IADsComputer.Owner
- IADsComputer.get_Owner
- IADsComputer.put_Owner
- IADsComputer.PrimaryUser
- IADsComputer.get_PrimaryUser
- IADsComputer.put_PrimaryUser
- IADsComputer.Processor
- IADsComputer.get_Processor
- IADsComputer.put_Processor
- IADsComputer.ProcessorCount
- IADsComputer.get_ProcessorCount
- IADsComputer.put_ProcessorCount
- IADsComputer.Role
- IADsComputer.get_Role
- IADsComputer.put_Role
- IADsComputer.Site
- IADsComputer.get_Site
- IADsComputer.StorageCapacity
- IADsComputer.get_StorageCapacity
- IADsComputer.put_StorageCapacity
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f3c455e2e43436627b62d142781bb6a605bef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905466"
---
# <a name="iadscomputer-property-methods"></a><span data-ttu-id="12604-105">Métodos de propiedad IADsComputer</span><span class="sxs-lookup"><span data-stu-id="12604-105">IADsComputer Property Methods</span></span>

<span data-ttu-id="12604-106">Los métodos de la interfaz [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) leen y escriben las propiedades descritas en este tema.</span><span class="sxs-lookup"><span data-stu-id="12604-106">The [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="12604-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="12604-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="12604-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12604-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="12604-109">**ComputerID**</span><span class="sxs-lookup"><span data-stu-id="12604-109">**ComputerID**</span></span>
<span data-ttu-id="12604-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-111">Identificador único global asignado a cada equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-111">The globally unique identifier assigned to each computer.</span></span>

<dt>

<span data-ttu-id="12604-112">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12604-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12604-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerID(
  [out] BSTR* pbstrComputerID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-114">**Departamento**</span><span class="sxs-lookup"><span data-stu-id="12604-114">**Department**</span></span>
<span data-ttu-id="12604-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-116">Unidad organizativa (OU), como Departamento, a la que pertenece este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-116">The organizational unit (OU), such as department, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="12604-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Department(
  [out] BSTR* pbstrDepartment
);
HRESULT put_Department(
  [in] BSTR bstrDepartment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="12604-119">**Description**</span></span>
<span data-ttu-id="12604-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-121">La descripción de este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-121">The description of this computer.</span></span>

<dt>

<span data-ttu-id="12604-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-124">**División**</span><span class="sxs-lookup"><span data-stu-id="12604-124">**Division**</span></span>
<span data-ttu-id="12604-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-126">La división, dentro de una organización, a la que pertenece este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-126">The division, within an organization, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="12604-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-128">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Division(
  [out] BSTR* pbstrDivision
);
HRESULT put_Division(
  [in] BSTR bstrDivision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-129">**Ubicación**</span><span class="sxs-lookup"><span data-stu-id="12604-129">**Location**</span></span>
<span data-ttu-id="12604-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-131">Ubicación física asignada de este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-131">The assigned physical location of this computer.</span></span>

<dt>

<span data-ttu-id="12604-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-133">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-134">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="12604-134">**MemorySize**</span></span>
<span data-ttu-id="12604-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-136">Tamaño, en megabytes, de la memoria de acceso aleatorio para este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-136">The size, in megabytes, of random access memory for this computer.</span></span>

<dt>

<span data-ttu-id="12604-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-138">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MemorySize(
  [out] BSTR* pbstrMemorySize
);
HRESULT put_MemorySize(
  [in] BSTR bstrMemorySize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-139">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="12604-139">**Model**</span></span>
<span data-ttu-id="12604-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-141">Marca y modelo de este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-141">The make and model of this computer.</span></span>

<dt>

<span data-ttu-id="12604-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-143">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-144">**NetAddresses**</span><span class="sxs-lookup"><span data-stu-id="12604-144">**NetAddresses**</span></span>
<span data-ttu-id="12604-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-146">Una matriz de campos NetAddress que representan las direcciones a las que se puede tener acceso a este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-146">An array of NetAddress fields that represent the addresses by which this computer can be reached.</span></span> <span data-ttu-id="12604-147">NetAddress es un **BSTR** específico del proveedor que se compone de dos subcadenas separadas por dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="12604-147">NetAddress is a provider-specific **BSTR** composed of two substrings separated by a colon (:).</span></span> <span data-ttu-id="12604-148">La subcadena izquierda indica el tipo de dirección y la subcadena derecha es una representación de cadena de una dirección de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="12604-148">The left substring indicates the address type, and the right substring is a string representation of an address of that type.</span></span> <span data-ttu-id="12604-149">Por ejemplo, las direcciones TCP/IP tienen el siguiente formato: IP: 100.201.301.45.</span><span class="sxs-lookup"><span data-stu-id="12604-149">For example, TCP/IP addresses are of the form: IP:100.201.301.45.</span></span> <span data-ttu-id="12604-150">Las direcciones de tipo IPX tienen el formato: IPX: 10.123456.80.</span><span class="sxs-lookup"><span data-stu-id="12604-150">IPX type addresses are of the form: IPX:10.123456.80.</span></span>

<dt>

<span data-ttu-id="12604-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-152">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="12604-152">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NetAddresses(
  [out] VARIANT* pvNetAddresses
);
HRESULT put_NetAddresses(
  [in] VARIANT vNetAddresses
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-153">**Identifica**</span><span class="sxs-lookup"><span data-stu-id="12604-153">**OperatingSystem**</span></span>
<span data-ttu-id="12604-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-155">Sistema operativo que se usa en este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-155">The operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="12604-156">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-157">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-157">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystem(
  [out] BSTR* pbstrOperatingSystem
);
HRESULT put_OperatingSystem(
  [in] BSTR bstrOperatingSystem
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-158">**OperatingSystemVersion**</span><span class="sxs-lookup"><span data-stu-id="12604-158">**OperatingSystemVersion**</span></span>
<span data-ttu-id="12604-159"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-159"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-160">La versión del sistema operativo que se usa en este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-160">The version of the operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="12604-161">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-162">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-162">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystemVersion(
  [out] BSTR* pbstrOperatingSystemVersion
);
HRESULT put_OperatingSystemVersion(
  [in] BSTR bstrOperatingSystemVersion
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-163">**Propietario**</span><span class="sxs-lookup"><span data-stu-id="12604-163">**Owner**</span></span>
<span data-ttu-id="12604-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-165">La persona a la que se asigna este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-165">The person to whom this computer is assigned.</span></span> <span data-ttu-id="12604-166">Esta persona también debe tener una licencia para ejecutar el software instalado.</span><span class="sxs-lookup"><span data-stu-id="12604-166">This person should also have a license to run the installed software.</span></span>

<dt>

<span data-ttu-id="12604-167">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-168">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwner
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-169">**PrimaryUser**</span><span class="sxs-lookup"><span data-stu-id="12604-169">**PrimaryUser**</span></span>
<span data-ttu-id="12604-170"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-170"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-171">El nombre de la persona de contacto, como un administrador, para este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-171">The name of the contact person, such as an administrator, for this computer.</span></span>

<dt>

<span data-ttu-id="12604-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-173">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-173">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryUser(
  [out] BSTR* pbstrPrimaryUser
);
HRESULT put_PrimaryUser(
  [in] BSTR bstrPrimaryUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-174">**Procesador**</span><span class="sxs-lookup"><span data-stu-id="12604-174">**Processor**</span></span>
<span data-ttu-id="12604-175"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-175"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-176">Tipo de procesador.</span><span class="sxs-lookup"><span data-stu-id="12604-176">The processor type.</span></span>

<dt>

<span data-ttu-id="12604-177">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-177">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-178">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-178">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Processor(
  [out] BSTR* pbstrProcessor
);
HRESULT put_Processor(
  [in] BSTR bstrProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-179">**ProcessorCount**</span><span class="sxs-lookup"><span data-stu-id="12604-179">**ProcessorCount**</span></span>
<span data-ttu-id="12604-180"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-180"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-181">El número de procesadores instalados.</span><span class="sxs-lookup"><span data-stu-id="12604-181">The number of installed processors.</span></span>

<dt>

<span data-ttu-id="12604-182">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-183">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-183">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProcessorCount(
  [out] BSTR* pbstrProcessorCount
);
HRESULT put_ProcessorCount(
  [in] BSTR bstrProcessorCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-184">**Rol**</span><span class="sxs-lookup"><span data-stu-id="12604-184">**Role**</span></span>
<span data-ttu-id="12604-185"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-185"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-186">El rol de este equipo, por ejemplo, estación de trabajo, servidor o controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="12604-186">The role of this computer, for example, workstation, server, or domain controller.</span></span>

<dt>

<span data-ttu-id="12604-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-187">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-188">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-188">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Role(
  [out] BSTR* pbstrRole
);
HRESULT put_Role(
  [in] BSTR bstrRole
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-189">**Sitio**</span><span class="sxs-lookup"><span data-stu-id="12604-189">**Site**</span></span>
<span data-ttu-id="12604-190"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-190"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-191">Identificador único global que identifica el sitio en el que se instaló este equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-191">The globally unique identifier that identifies the site that this computer was installed in.</span></span> <span data-ttu-id="12604-192">Un sitio es una región física de buena conectividad en una red.</span><span class="sxs-lookup"><span data-stu-id="12604-192">A site is a physical region of good connectivity in a network.</span></span>

<dt>

<span data-ttu-id="12604-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12604-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12604-194">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-194">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Site(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="12604-195">**StorageCapacity**</span><span class="sxs-lookup"><span data-stu-id="12604-195">**StorageCapacity**</span></span>
<span data-ttu-id="12604-196"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12604-196"></dt> <dd> <dl></span></span>

<span data-ttu-id="12604-197">Tamaño, en megabytes, del disco.</span><span class="sxs-lookup"><span data-stu-id="12604-197">The size, in megabytes, of the disk.</span></span>

<dt>

<span data-ttu-id="12604-198">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12604-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12604-199">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12604-199">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StorageCapacity(
  [out] BSTR* pbstrStorageCapacity
);
HRESULT put_StorageCapacity(
  [in] BSTR bstrStorageCapacity
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="12604-200">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12604-200">Remarks</span></span>

<span data-ttu-id="12604-201">Distintos proveedores pueden optar por exponer distintas propiedades de un objeto de equipo.</span><span class="sxs-lookup"><span data-stu-id="12604-201">Different providers may choose to expose different properties of a computer object.</span></span> <span data-ttu-id="12604-202">Para obtener más información, consulte [ADSI System Providers](adsi-system-providers.md).</span><span class="sxs-lookup"><span data-stu-id="12604-202">For more information, see [ADSI System Providers](adsi-system-providers.md).</span></span>

<span data-ttu-id="12604-203">Puede descubrir las propiedades que se admiten mediante la inspección de las propiedades obligatorias y opcionales a través de su clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="12604-203">You can discover what properties are supported by inspecting the mandatory and optional properties through its schema class.</span></span> <span data-ttu-id="12604-204">Para obtener más información, consulte la interfaz [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) .</span><span class="sxs-lookup"><span data-stu-id="12604-204">For more information, see the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface.</span></span>

<span data-ttu-id="12604-205">Para examinar el estado de un equipo o para realizar la operación de apagado a través de la red, debe usar la interfaz [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) .</span><span class="sxs-lookup"><span data-stu-id="12604-205">To examine the status of a computer or to perform the shutdown operation across the network, you must use the [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="12604-206">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="12604-206">Examples</span></span>

<span data-ttu-id="12604-207">En el siguiente ejemplo de código Visual Basic se examinan las propiedades del equipo admitidas por el proveedor WinNT de ADSI.</span><span class="sxs-lookup"><span data-stu-id="12604-207">The following Visual Basic code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```VB
Dim obj As IADs
On Error Resume Next

Set obj = GetObject("WinNT://myMachine,computer")
If (obj.Class = "Computer") Then
    MsgBox "Computer owner: " & obj.owner
    MsgBox "Computer division: " & obj.Division
    MsgBox "Computer operatingSystem: " & obj.OperatingSystem
    MsgBox "Computer operating System Version: " & obj.OperatingSystemVersion
    MsgBox "Computer processor: " & obj.Processor
    MsgBox "Computer processor Count: " & obj.ProcessorCount
End If
```



<span data-ttu-id="12604-208">En el siguiente ejemplo de código de C++ se examinan las propiedades del equipo admitidas por el proveedor WinNT de ADSI.</span><span class="sxs-lookup"><span data-stu-id="12604-208">The following C++ code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```C++
IADsComputer *pComp = NULL;
LPWSTR adspath = L"WinNT://jeffsmith1,computer";
HRESULT hr = S_OK;
BSTR bstr = NULL;

hr = ADsGetObject(adspath,IID_IADsComputer,(void**)&pComp);
if(FAILED(hr)) {goto Cleanup;}

hr = pComp->get_Owner(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Computer owner: %S\n",bstr);
SysFreeString(bstr);

hr = pComp->get_OperatingSystem(&bstr);
if(FAILED(hr)) {goto Cleanup;}
printf("Operating System: %S\n",bstr);
SysFreeString(bstr);

Cleanup:
    if(pComp) pComp->Release();
    if(bstr) SysFreeString(bstr);
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="12604-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12604-209">Requirements</span></span>



| <span data-ttu-id="12604-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="12604-210">Requirement</span></span> | <span data-ttu-id="12604-211">Value</span><span class="sxs-lookup"><span data-stu-id="12604-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12604-212">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12604-212">Minimum supported client</span></span><br/> | <span data-ttu-id="12604-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12604-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12604-214">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12604-214">Minimum supported server</span></span><br/> | <span data-ttu-id="12604-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12604-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12604-216">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12604-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="12604-217"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="12604-217"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="12604-218">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="12604-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12604-219"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12604-219"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="12604-220">IID</span><span class="sxs-lookup"><span data-stu-id="12604-220">IID</span></span><br/>                      | <span data-ttu-id="12604-221">IID \_ IADsComputer se define como EFE3CC70-1D9F-11cf-B1F3-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="12604-221">IID\_IADsComputer is defined as EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="12604-222">Vea también</span><span class="sxs-lookup"><span data-stu-id="12604-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12604-223">**IADsComputer**</span><span class="sxs-lookup"><span data-stu-id="12604-223">**IADsComputer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputer)
</dt> <dt>

[<span data-ttu-id="12604-224">Proveedores de sistema ADSI</span><span class="sxs-lookup"><span data-stu-id="12604-224">ADSI System Providers</span></span>](adsi-system-providers.md)
</dt> <dt>

[<span data-ttu-id="12604-225">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="12604-225">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="12604-226">**IADsComputerOperations**</span><span class="sxs-lookup"><span data-stu-id="12604-226">**IADsComputerOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)
</dt> <dt>

[<span data-ttu-id="12604-227">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="12604-227">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





