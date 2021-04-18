---
description: Representa un trabajo de operación del servicio de archivos invitados.
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Msvm_CopyFileToGuestJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57e27b4ba610eea4559f3b045b2d823661cf4cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667823"
---
# <a name="msvm_copyfiletoguestjob-class"></a><span data-ttu-id="5582f-103">MSVM \_ CopyFileToGuestJob (clase)</span><span class="sxs-lookup"><span data-stu-id="5582f-103">Msvm\_CopyFileToGuestJob class</span></span>

<span data-ttu-id="5582f-104">Representa un trabajo de operación del servicio de archivos invitados.</span><span class="sxs-lookup"><span data-stu-id="5582f-104">Represents a guest file service operation job.</span></span> <span data-ttu-id="5582f-105">Esta clase deriva de [**MSVM \_ GuestFileService**](msvm-guestfileservice.md).</span><span class="sxs-lookup"><span data-stu-id="5582f-105">This class derives from [**Msvm\_GuestFileService**](msvm-guestfileservice.md).</span></span>

<span data-ttu-id="5582f-106">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5582f-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5582f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5582f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
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
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a><span data-ttu-id="5582f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5582f-108">Members</span></span>

<span data-ttu-id="5582f-109">La clase **MSVM \_ CopyFileToGuestJob** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5582f-109">The **Msvm\_CopyFileToGuestJob** class has these types of members:</span></span>

-   [<span data-ttu-id="5582f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5582f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5582f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5582f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5582f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="5582f-112">Methods</span></span>

<span data-ttu-id="5582f-113">La clase **MSVM \_ CopyFileToGuestJob** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5582f-113">The **Msvm\_CopyFileToGuestJob** class has these methods.</span></span>



| <span data-ttu-id="5582f-114">Método</span><span class="sxs-lookup"><span data-stu-id="5582f-114">Method</span></span>                                                                   | <span data-ttu-id="5582f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5582f-115">Description</span></span>                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="5582f-116">**CopyFilesToGuest**</span><span class="sxs-lookup"><span data-stu-id="5582f-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md)       | <span data-ttu-id="5582f-117">Copia archivos del host de Hyper-V a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5582f-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> |
| [<span data-ttu-id="5582f-118">**GetError**</span><span class="sxs-lookup"><span data-stu-id="5582f-118">**GetError**</span></span>](geterror-msvm-copyfiletoguestjob.md)                     | <span data-ttu-id="5582f-119">Recupera el objeto de error del trabajo.</span><span class="sxs-lookup"><span data-stu-id="5582f-119">Retrieves the error object for the job.</span></span><br/>                    |
| [<span data-ttu-id="5582f-120">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="5582f-120">**GetErrorEx**</span></span>](geterrorex-msvm-copyfiletoguestjob.md)                 | <span data-ttu-id="5582f-121">Recupera los objetos de error del trabajo.</span><span class="sxs-lookup"><span data-stu-id="5582f-121">Retrieves the error objects for the job.</span></span><br/>                   |
| [<span data-ttu-id="5582f-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="5582f-122">**RequestStateChange**</span></span>](requeststatechange-msvm-copyfiletoguestjob.md) | <span data-ttu-id="5582f-123">Cambia el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="5582f-123">Changes the state of the job.</span></span><br/>                              |
| <span data-ttu-id="5582f-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="5582f-124">**StartService**</span></span>                                                         | <span data-ttu-id="5582f-125">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="5582f-125">This method is not supported.</span></span><br/>                              |
| <span data-ttu-id="5582f-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="5582f-126">**StopService**</span></span>                                                          | <span data-ttu-id="5582f-127">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="5582f-127">This method is not supported.</span></span><br/>                              |



 

### <a name="properties"></a><span data-ttu-id="5582f-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5582f-128">Properties</span></span>

<span data-ttu-id="5582f-129">La clase **MSVM \_ CopyFileToGuestJob** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5582f-129">The **Msvm\_CopyFileToGuestJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5582f-130">**Cancelable**</span><span class="sxs-lookup"><span data-stu-id="5582f-130">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-131">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5582f-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-133">Indica si se puede cancelar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="5582f-133">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="5582f-134">El valor de esta propiedad no garantiza que una solicitud para cancelar el trabajo se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="5582f-134">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span> <span data-ttu-id="5582f-135">Si **es true**, el trabajo se puede cancelar; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="5582f-135">If **TRUE**, the job can be cancelled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5582f-136">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5582f-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5582f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-139">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5582f-139">Short textual description of the object.</span></span> <span data-ttu-id="5582f-140">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5582f-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5582f-141">**CopyFileToGuestSettingData**</span><span class="sxs-lookup"><span data-stu-id="5582f-141">**CopyFileToGuestSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-142">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="5582f-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5582f-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-144">Establecer los datos que se usan para copiar un archivo.</span><span class="sxs-lookup"><span data-stu-id="5582f-144">Setting data that is used to copy a file.</span></span>

</dd> <dt>

<span data-ttu-id="5582f-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5582f-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5582f-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-148">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="5582f-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5582f-149">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="5582f-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="5582f-150">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5582f-150">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5582f-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-153">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5582f-153">Textual description of the object.</span></span> <span data-ttu-id="5582f-154">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5582f-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5582f-155">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="5582f-155">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5582f-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5582f-158">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabajo de CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="5582f-158">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="5582f-159">Descripción breve del error, si está presente.</span><span class="sxs-lookup"><span data-stu-id="5582f-159">A summary description of the error, if present.</span></span> <span data-ttu-id="5582f-160">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="5582f-160">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="5582f-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5582f-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-162">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5582f-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-164">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="5582f-164">Date and time the object was installed.</span></span> <span data-ttu-id="5582f-165">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5582f-165">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="5582f-166">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5582f-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5582f-167">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5582f-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5582f-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-170">Identificador único para el servicio que también proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="5582f-170">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="5582f-171">Para obtener más información sobre la funcionalidad, vea la propiedad **Description** del objeto.</span><span class="sxs-lookup"><span data-stu-id="5582f-171">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="5582f-172">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5582f-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5582f-173">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="5582f-173">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-174">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5582f-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-176">Si **es true**, el servicio se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="5582f-176">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="5582f-177">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="5582f-177">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5582f-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-180">Indica si el servicio se inicia automáticamente (por ejemplo, por un sistema operativo) o solo se inicia después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5582f-180">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="5582f-181">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5582f-181">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="5582f-182">**Automático**</span><span class="sxs-lookup"><span data-stu-id="5582f-182">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="5582f-183">**Manualmente**</span><span class="sxs-lookup"><span data-stu-id="5582f-183">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5582f-184">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5582f-184">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5582f-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-187">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5582f-187">Current status of the object.</span></span> <span data-ttu-id="5582f-188">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5582f-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="5582f-189">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5582f-189">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="5582f-190">**ACEPTAR**</span><span class="sxs-lookup"><span data-stu-id="5582f-190">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="5582f-191">**Error**</span><span class="sxs-lookup"><span data-stu-id="5582f-191">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="5582f-192">**Degradado**</span><span class="sxs-lookup"><span data-stu-id="5582f-192">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="5582f-193">**Unknown**</span><span class="sxs-lookup"><span data-stu-id="5582f-193">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="5582f-194">**"Pred FAIL"**</span><span class="sxs-lookup"><span data-stu-id="5582f-194">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="5582f-195">**Comenzar**</span><span class="sxs-lookup"><span data-stu-id="5582f-195">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="5582f-196">**Bloqueo**</span><span class="sxs-lookup"><span data-stu-id="5582f-196">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="5582f-197">**Servicio**</span><span class="sxs-lookup"><span data-stu-id="5582f-197">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="5582f-198">**Calca**</span><span class="sxs-lookup"><span data-stu-id="5582f-198">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="5582f-199">**"Recover"**</span><span class="sxs-lookup"><span data-stu-id="5582f-199">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="5582f-200">**"Sin contacto"**</span><span class="sxs-lookup"><span data-stu-id="5582f-200">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="5582f-201">**"Pérdida de comunicación"**</span><span class="sxs-lookup"><span data-stu-id="5582f-201">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5582f-202">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5582f-202">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5582f-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-205">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5582f-205">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="5582f-206">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5582f-206">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5582f-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-209">Nombre del sistema que hospeda el servicio.</span><span class="sxs-lookup"><span data-stu-id="5582f-209">Name of the system that hosts the service.</span></span>

</dd> <dt>

<span data-ttu-id="5582f-210">**VirtualSystemName**</span><span class="sxs-lookup"><span data-stu-id="5582f-210">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5582f-211">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5582f-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5582f-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5582f-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5582f-213">GUID del sistema virtual afectado.</span><span class="sxs-lookup"><span data-stu-id="5582f-213">GUID of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5582f-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5582f-214">Requirements</span></span>



| <span data-ttu-id="5582f-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="5582f-215">Requirement</span></span> | <span data-ttu-id="5582f-216">Value</span><span class="sxs-lookup"><span data-stu-id="5582f-216">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5582f-217">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5582f-217">Minimum supported client</span></span><br/> | <span data-ttu-id="5582f-218">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="5582f-218">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5582f-219">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5582f-219">Minimum supported server</span></span><br/> | <span data-ttu-id="5582f-220">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5582f-220">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5582f-221">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5582f-221">Namespace</span></span><br/>                | <span data-ttu-id="5582f-222">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5582f-222">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5582f-223">MOF</span><span class="sxs-lookup"><span data-stu-id="5582f-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5582f-224"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5582f-224"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5582f-225">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5582f-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5582f-226"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5582f-226"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5582f-227">Vea también</span><span class="sxs-lookup"><span data-stu-id="5582f-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5582f-228">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="5582f-228">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

[<span data-ttu-id="5582f-229">**MSVM \_ GuestFileService**</span><span class="sxs-lookup"><span data-stu-id="5582f-229">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> <dt>

[<span data-ttu-id="5582f-230">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="5582f-230">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

