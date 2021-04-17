---
description: MSVM \_ GuestFileService contiene un método que se puede usar para copiar un archivo en una máquina virtual desde el host de Hyper-V.
ms.assetid: 3599d5a8-415f-48f8-b887-00a93b7abb83
title: Msvm_GuestFileService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService
- Msvm_GuestFileService.StartService
- Msvm_GuestFileService.StopService
- Msvm_GuestFileService.Caption
- Msvm_GuestFileService.CreationClassName
- Msvm_GuestFileService.Description
- Msvm_GuestFileService.InstallDate
- Msvm_GuestFileService.Name
- Msvm_GuestFileService.Started
- Msvm_GuestFileService.StartMode
- Msvm_GuestFileService.Status
- Msvm_GuestFileService.SystemCreationClassName
- Msvm_GuestFileService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ee0f235d7549428ecf02e9c758c83bcea33efe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666336"
---
# <a name="msvm_guestfileservice-class"></a><span data-ttu-id="70b2e-103">MSVM \_ GuestFileService (clase)</span><span class="sxs-lookup"><span data-stu-id="70b2e-103">Msvm\_GuestFileService class</span></span>

<span data-ttu-id="70b2e-104">**MSVM \_ GuestFileService** contiene un método que se puede usar para copiar un archivo en una máquina virtual desde el host de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="70b2e-104">**Msvm\_GuestFileService** contains a method that can be used to copy a file to a virtual machine from the Hyper-V host.</span></span> <span data-ttu-id="70b2e-105">Esta clase deriva de [**MSVM \_ GuestService**](msvm-guestservice.md).</span><span class="sxs-lookup"><span data-stu-id="70b2e-105">This class derives from [**Msvm\_GuestService**](msvm-guestservice.md).</span></span>

<span data-ttu-id="70b2e-106">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="70b2e-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b2e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70b2e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestFileService : Msvm_GuestService
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="70b2e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="70b2e-108">Members</span></span>

<span data-ttu-id="70b2e-109">La clase **MSVM \_ GuestFileService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="70b2e-109">The **Msvm\_GuestFileService** class has these types of members:</span></span>

-   [<span data-ttu-id="70b2e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="70b2e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="70b2e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70b2e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="70b2e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="70b2e-112">Methods</span></span>

<span data-ttu-id="70b2e-113">La clase **MSVM \_ GuestFileService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="70b2e-113">The **Msvm\_GuestFileService** class has these methods.</span></span>



| <span data-ttu-id="70b2e-114">Método</span><span class="sxs-lookup"><span data-stu-id="70b2e-114">Method</span></span>                                                             | <span data-ttu-id="70b2e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="70b2e-115">Description</span></span>                                                                                                                                                                  |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70b2e-116">**CopyFilesToGuest**</span><span class="sxs-lookup"><span data-stu-id="70b2e-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md) | <span data-ttu-id="70b2e-117">Copia archivos del host de Hyper-V a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="70b2e-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> <span data-ttu-id="70b2e-118">**Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="70b2e-118">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| <span data-ttu-id="70b2e-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="70b2e-119">**StartService**</span></span>                                                   | <span data-ttu-id="70b2e-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="70b2e-120">This method is not supported.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="70b2e-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="70b2e-121">**StopService**</span></span>                                                    | <span data-ttu-id="70b2e-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="70b2e-122">This method is not supported.</span></span><br/>                                                                                                                                     |



 

### <a name="properties"></a><span data-ttu-id="70b2e-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70b2e-123">Properties</span></span>

<span data-ttu-id="70b2e-124">La clase **MSVM \_ GuestFileService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="70b2e-124">The **Msvm\_GuestFileService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70b2e-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="70b2e-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b2e-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70b2e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b2e-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70b2e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70b2e-128">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="70b2e-128">Short textual description of the object.</span></span> <span data-ttu-id="70b2e-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70b2e-129">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="70b2e-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="70b2e-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b2e-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70b2e-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b2e-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70b2e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70b2e-133">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="70b2e-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="70b2e-134">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="70b2e-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="70b2e-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="70b2e-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b2e-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70b2e-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b2e-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70b2e-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70b2e-138">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="70b2e-138">Textual description of the object.</span></span> <span data-ttu-id="70b2e-139">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70b2e-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="70b2e-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="70b2e-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b2e-141">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70b2e-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70b2e-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70b2e-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70b2e-143">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="70b2e-143">Date and time the object was installed.</span></span> <span data-ttu-id="70b2e-144">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="70b2e-144">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="70b2e-145">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70b2e-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="70b2e-146">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="70b2e-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b2e-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70b2e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b2e-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70b2e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70b2e-149">Identificador único para el servicio que también proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="70b2e-149">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="70b2e-150">Para obtener más información sobre la funcionalidad, vea la propiedad **Description** del objeto.</span><span class="sxs-lookup"><span data-stu-id="70b2e-150">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="70b2e-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70b2e-151">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="70b2e-152">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="70b2e-152">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b2e-153">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="70b2e-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70b2e-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70b2e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70b2e-155">Si **es true**, el servicio se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="70b2e-155">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="70b2e-156">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="70b2e-156">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b2e-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70b2e-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b2e-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70b2e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70b2e-159">Indica si el servicio se inicia automáticamente (por ejemplo, por un sistema operativo) o solo se inicia después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70b2e-159">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="70b2e-160">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="70b2e-160">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="70b2e-161">**Automático**</span><span class="sxs-lookup"><span data-stu-id="70b2e-161">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="70b2e-162">**Manualmente**</span><span class="sxs-lookup"><span data-stu-id="70b2e-162">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70b2e-163">**Estado**</span><span class="sxs-lookup"><span data-stu-id="70b2e-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b2e-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70b2e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b2e-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70b2e-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70b2e-166">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="70b2e-166">Current status of the object.</span></span> <span data-ttu-id="70b2e-167">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70b2e-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="70b2e-168">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="70b2e-168">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="70b2e-169">**ACEPTAR**</span><span class="sxs-lookup"><span data-stu-id="70b2e-169">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="70b2e-170">**Error**</span><span class="sxs-lookup"><span data-stu-id="70b2e-170">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="70b2e-171">**Degradado**</span><span class="sxs-lookup"><span data-stu-id="70b2e-171">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="70b2e-172">**Unknown**</span><span class="sxs-lookup"><span data-stu-id="70b2e-172">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="70b2e-173">**"Pred FAIL"**</span><span class="sxs-lookup"><span data-stu-id="70b2e-173">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="70b2e-174">**Comenzar**</span><span class="sxs-lookup"><span data-stu-id="70b2e-174">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="70b2e-175">**Bloqueo**</span><span class="sxs-lookup"><span data-stu-id="70b2e-175">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="70b2e-176">**Servicio**</span><span class="sxs-lookup"><span data-stu-id="70b2e-176">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="70b2e-177">**Calca**</span><span class="sxs-lookup"><span data-stu-id="70b2e-177">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="70b2e-178">**"Recover"**</span><span class="sxs-lookup"><span data-stu-id="70b2e-178">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="70b2e-179">**"Sin contacto"**</span><span class="sxs-lookup"><span data-stu-id="70b2e-179">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="70b2e-180">**"Pérdida de comunicación"**</span><span class="sxs-lookup"><span data-stu-id="70b2e-180">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70b2e-181">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="70b2e-181">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b2e-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70b2e-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b2e-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70b2e-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70b2e-184">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="70b2e-184">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="70b2e-185">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="70b2e-185">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70b2e-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70b2e-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70b2e-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70b2e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70b2e-188">Nombre del sistema que hospeda el servicio.</span><span class="sxs-lookup"><span data-stu-id="70b2e-188">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70b2e-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70b2e-189">Requirements</span></span>



| <span data-ttu-id="70b2e-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="70b2e-190">Requirement</span></span> | <span data-ttu-id="70b2e-191">Value</span><span class="sxs-lookup"><span data-stu-id="70b2e-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b2e-192">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70b2e-192">Minimum supported client</span></span><br/> | <span data-ttu-id="70b2e-193">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="70b2e-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="70b2e-194">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70b2e-194">Minimum supported server</span></span><br/> | <span data-ttu-id="70b2e-195">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="70b2e-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="70b2e-196">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="70b2e-196">Namespace</span></span><br/>                | <span data-ttu-id="70b2e-197">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="70b2e-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="70b2e-198">MOF</span><span class="sxs-lookup"><span data-stu-id="70b2e-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70b2e-199"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70b2e-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70b2e-200">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70b2e-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70b2e-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70b2e-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="70b2e-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="70b2e-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b2e-203">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="70b2e-203">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

