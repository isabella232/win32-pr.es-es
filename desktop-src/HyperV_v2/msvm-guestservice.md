---
description: MSVM \_ GuestService es la clase base abstracta para los servicios del invitado a los que se puede tener acceso desde el host.
ms.assetid: F9E6FFE6-B8C5-4F06-BF22-A4BDB20F813A
title: Msvm_GuestService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService
- Msvm_GuestService.Caption
- Msvm_GuestService.CreationClassName
- Msvm_GuestService.Description
- Msvm_GuestService.InstallDate
- Msvm_GuestService.Name
- Msvm_GuestService.Started
- Msvm_GuestService.StartMode
- Msvm_GuestService.Status
- Msvm_GuestService.SystemCreationClassName
- Msvm_GuestService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99d1936a2678fc2d8357974f9c11a250a1d9bce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423699"
---
# <a name="msvm_guestservice-class"></a><span data-ttu-id="1d012-103">MSVM \_ GuestService (clase)</span><span class="sxs-lookup"><span data-stu-id="1d012-103">Msvm\_GuestService class</span></span>

<span data-ttu-id="1d012-104">**MSVM \_ GuestService** es la clase base abstracta para los servicios del invitado a los que se puede tener acceso desde el host.</span><span class="sxs-lookup"><span data-stu-id="1d012-104">**Msvm\_GuestService** is the abstract base class for services in the guest that can be accessed from the host.</span></span> <span data-ttu-id="1d012-105">Esta clase deriva de la clase [**de \_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service) .</span><span class="sxs-lookup"><span data-stu-id="1d012-105">This class derives from the [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service) class.</span></span>

<span data-ttu-id="1d012-106">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1d012-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d012-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d012-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_GuestService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="1d012-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d012-108">Members</span></span>

<span data-ttu-id="1d012-109">La clase **MSVM \_ GuestService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1d012-109">The **Msvm\_GuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="1d012-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1d012-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1d012-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d012-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1d012-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1d012-112">Methods</span></span>

<span data-ttu-id="1d012-113">La clase **MSVM \_ GuestService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1d012-113">The **Msvm\_GuestService** class has these methods.</span></span>



| <span data-ttu-id="1d012-114">Método</span><span class="sxs-lookup"><span data-stu-id="1d012-114">Method</span></span>                                                             | <span data-ttu-id="1d012-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d012-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d012-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="1d012-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestservice.md) | <span data-ttu-id="1d012-117">Solicita que el estado del servicio invitado cambie al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="1d012-117">Requests that the state of the guest service be changed to the specified value.</span></span><br/> |
| [<span data-ttu-id="1d012-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="1d012-118">**StartService**</span></span>](startservice-msvm-guestservice.md)             | <span data-ttu-id="1d012-119">Pone el servicio invitado en un estado Iniciado.</span><span class="sxs-lookup"><span data-stu-id="1d012-119">Puts the guest service in a started state.</span></span> <br/>                                     |
| [<span data-ttu-id="1d012-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="1d012-120">**StopService**</span></span>](stopservice-msvm-guestservice.md)               | <span data-ttu-id="1d012-121">Detiene el servicio invitado.</span><span class="sxs-lookup"><span data-stu-id="1d012-121">Stops the guest service.</span></span> <br/>                                                       |



 

### <a name="properties"></a><span data-ttu-id="1d012-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d012-122">Properties</span></span>

<span data-ttu-id="1d012-123">La clase **MSVM \_ GuestService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1d012-123">The **Msvm\_GuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d012-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1d012-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d012-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d012-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d012-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d012-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d012-127">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d012-127">Short textual description of the object.</span></span> <span data-ttu-id="1d012-128">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d012-128">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d012-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d012-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d012-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d012-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d012-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d012-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d012-132">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="1d012-132">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1d012-133">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="1d012-133">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="1d012-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d012-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d012-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d012-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d012-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d012-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d012-137">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d012-137">Textual description of the object.</span></span> <span data-ttu-id="1d012-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d012-138">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d012-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1d012-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d012-140">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d012-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d012-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d012-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d012-142">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="1d012-142">Date and time the object was installed.</span></span> <span data-ttu-id="1d012-143">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d012-143">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="1d012-144">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d012-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d012-145">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1d012-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d012-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d012-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d012-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d012-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d012-148">Identificador único para el servicio que también proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="1d012-148">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="1d012-149">Para obtener más información sobre la funcionalidad, vea la propiedad **Description** del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d012-149">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="1d012-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d012-150">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d012-151">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="1d012-151">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d012-152">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1d012-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d012-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d012-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d012-154">Si **es true**, el servicio se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="1d012-154">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="1d012-155">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="1d012-155">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d012-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d012-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d012-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d012-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d012-158">Indica si el servicio se inicia automáticamente (por ejemplo, por un sistema operativo) o solo se inicia después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d012-158">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="1d012-159">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d012-159">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="1d012-160">**Automático**</span><span class="sxs-lookup"><span data-stu-id="1d012-160">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="1d012-161">**Manualmente**</span><span class="sxs-lookup"><span data-stu-id="1d012-161">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d012-162">**Estado**</span><span class="sxs-lookup"><span data-stu-id="1d012-162">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d012-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d012-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d012-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d012-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d012-165">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d012-165">Current status of the object.</span></span> <span data-ttu-id="1d012-166">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d012-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="1d012-167">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d012-167">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="1d012-168">**ACEPTAR**</span><span class="sxs-lookup"><span data-stu-id="1d012-168">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="1d012-169">**Error**</span><span class="sxs-lookup"><span data-stu-id="1d012-169">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="1d012-170">**Degradado**</span><span class="sxs-lookup"><span data-stu-id="1d012-170">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="1d012-171">**Unknown**</span><span class="sxs-lookup"><span data-stu-id="1d012-171">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="1d012-172">**"Pred FAIL"**</span><span class="sxs-lookup"><span data-stu-id="1d012-172">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="1d012-173">**Comenzar**</span><span class="sxs-lookup"><span data-stu-id="1d012-173">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="1d012-174">**Bloqueo**</span><span class="sxs-lookup"><span data-stu-id="1d012-174">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="1d012-175">**Servicio**</span><span class="sxs-lookup"><span data-stu-id="1d012-175">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="1d012-176">**Calca**</span><span class="sxs-lookup"><span data-stu-id="1d012-176">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="1d012-177">**"Recover"**</span><span class="sxs-lookup"><span data-stu-id="1d012-177">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="1d012-178">**"Sin contacto"**</span><span class="sxs-lookup"><span data-stu-id="1d012-178">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="1d012-179">**"Pérdida de comunicación"**</span><span class="sxs-lookup"><span data-stu-id="1d012-179">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d012-180">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d012-180">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d012-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d012-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d012-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d012-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d012-183">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1d012-183">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="1d012-184">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1d012-184">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d012-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d012-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d012-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d012-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d012-187">Nombre del sistema que hospeda el servicio.</span><span class="sxs-lookup"><span data-stu-id="1d012-187">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d012-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d012-188">Requirements</span></span>



| <span data-ttu-id="1d012-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d012-189">Requirement</span></span> | <span data-ttu-id="1d012-190">Value</span><span class="sxs-lookup"><span data-stu-id="1d012-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d012-191">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d012-191">Minimum supported client</span></span><br/> | <span data-ttu-id="1d012-192">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="1d012-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1d012-193">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d012-193">Minimum supported server</span></span><br/> | <span data-ttu-id="1d012-194">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d012-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1d012-195">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d012-195">Namespace</span></span><br/>                | <span data-ttu-id="1d012-196">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1d012-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1d012-197">MOF</span><span class="sxs-lookup"><span data-stu-id="1d012-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d012-198"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d012-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d012-199">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d012-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d012-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d012-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1d012-201">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d012-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d012-202">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="1d012-202">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="1d012-203">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="1d012-203">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

