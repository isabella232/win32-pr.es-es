---
description: Proporciona información detallada acerca de una imagen de almacenamiento montada manualmente.
ms.assetid: 40b94c5f-c277-40c8-a55d-ebc64cb231ca
title: Msvm_MountedStorageImage (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage
- Msvm_MountedStorageImage.InstanceID
- Msvm_MountedStorageImage.Caption
- Msvm_MountedStorageImage.Description
- Msvm_MountedStorageImage.ElementName
- Msvm_MountedStorageImage.InstallDate
- Msvm_MountedStorageImage.Name
- Msvm_MountedStorageImage.OperationalStatus
- Msvm_MountedStorageImage.StatusDescriptions
- Msvm_MountedStorageImage.Status
- Msvm_MountedStorageImage.HealthState
- Msvm_MountedStorageImage.CommunicationStatus
- Msvm_MountedStorageImage.DetailedStatus
- Msvm_MountedStorageImage.OperatingStatus
- Msvm_MountedStorageImage.PrimaryStatus
- Msvm_MountedStorageImage.Type
- Msvm_MountedStorageImage.Access
- Msvm_MountedStorageImage.PortNumber
- Msvm_MountedStorageImage.PathId
- Msvm_MountedStorageImage.TargetId
- Msvm_MountedStorageImage.Lun
- Msvm_MountedStorageImage.PnpDevicePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1b6f00b137fc73bcf8f79d39e6f7bfb5a6d7c944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817891"
---
# <a name="msvm_mountedstorageimage-class"></a><span data-ttu-id="5040e-103">MSVM \_ MountedStorageImage (clase)</span><span class="sxs-lookup"><span data-stu-id="5040e-103">Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="5040e-104">Proporciona información detallada acerca de una imagen de almacenamiento montada manualmente.</span><span class="sxs-lookup"><span data-stu-id="5040e-104">Provides detailed information about a manually mounted storage image.</span></span>

<span data-ttu-id="5040e-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5040e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5040e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5040e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MountedStorageImage : CIM_LogicalElement
{
  string   InstanceID;
  string   Caption = "Mounted Storage Image";
  string   Description = "Information about a mounted storage image.";
  string   ElementName = "Mounted Storage Image";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   Type;
  uint16   Access;
  UINT8    PortNumber;
  UINT8    PathId;
  UINT8    TargetId;
  UINT8    Lun;
  string   PnpDevicePath;
};
```

## <a name="members"></a><span data-ttu-id="5040e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5040e-107">Members</span></span>

<span data-ttu-id="5040e-108">La clase **MSVM \_ MountedStorageImage** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5040e-108">The **Msvm\_MountedStorageImage** class has these types of members:</span></span>

-   [<span data-ttu-id="5040e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5040e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5040e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5040e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5040e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5040e-111">Methods</span></span>

<span data-ttu-id="5040e-112">La clase **MSVM \_ MountedStorageImage** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5040e-112">The **Msvm\_MountedStorageImage** class has these methods.</span></span>



| <span data-ttu-id="5040e-113">Método</span><span class="sxs-lookup"><span data-stu-id="5040e-113">Method</span></span>                                                                          | <span data-ttu-id="5040e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5040e-114">Description</span></span>                                    |
|:--------------------------------------------------------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="5040e-115">**DetachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="5040e-115">**DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md) | <span data-ttu-id="5040e-116">Desasocia la imagen de almacenamiento montada.</span><span class="sxs-lookup"><span data-stu-id="5040e-116">Detaches the mounted storage image.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5040e-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5040e-117">Properties</span></span>

<span data-ttu-id="5040e-118">La clase **MSVM \_ MountedStorageImage** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5040e-118">The **Msvm\_MountedStorageImage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5040e-119">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="5040e-119">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-120">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5040e-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-122">Acceso en el que se monta la imagen de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5040e-122">The access under which the storage image is mounted.</span></span>

<dt>

<span id="Read-only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="5040e-123">**Solo lectura** (1)</span><span class="sxs-lookup"><span data-stu-id="5040e-123">**Read-only** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="5040e-124">**Lectura y escritura** (2)</span><span class="sxs-lookup"><span data-stu-id="5040e-124">**Read/Write** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5040e-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5040e-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5040e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-128">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5040e-128">A short description of the object.</span></span> <span data-ttu-id="5040e-129">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre contiene "imagen de almacenamiento montada".</span><span class="sxs-lookup"><span data-stu-id="5040e-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="5040e-130">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="5040e-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-131">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5040e-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-133">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="5040e-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5040e-134">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="5040e-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5040e-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5040e-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-138">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5040e-138">A description of the object.</span></span> <span data-ttu-id="5040e-139">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre contiene "información acerca de una imagen de almacenamiento montada".</span><span class="sxs-lookup"><span data-stu-id="5040e-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Information about a mounted storage image.".</span></span>

</dd> <dt>

<span data-ttu-id="5040e-140">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5040e-140">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-141">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5040e-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-143">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="5040e-143">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5040e-144">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="5040e-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5040e-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5040e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-148">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="5040e-148">A display name for the object.</span></span> <span data-ttu-id="5040e-149">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre contiene "imagen de almacenamiento montada".</span><span class="sxs-lookup"><span data-stu-id="5040e-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="5040e-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5040e-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5040e-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-153">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="5040e-153">The current health of the element.</span></span> <span data-ttu-id="5040e-154">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="5040e-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="5040e-155">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="5040e-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="5040e-156">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5.</span><span class="sxs-lookup"><span data-stu-id="5040e-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5040e-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-158">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5040e-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-160">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5040e-160">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="5040e-161">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5040e-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5040e-162">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5040e-162">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5040e-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5040e-165">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="5040e-165">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5040e-166">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="5040e-166">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5040e-167">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre es **null**.</span><span class="sxs-lookup"><span data-stu-id="5040e-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-168">**LUN**</span><span class="sxs-lookup"><span data-stu-id="5040e-168">**Lun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-169">Tipo de datos: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="5040e-169">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5040e-171">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5040e-171">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5040e-172">IDENTIFICADOR de LUN de dirección SCSI.</span><span class="sxs-lookup"><span data-stu-id="5040e-172">The SCSI address LUN ID.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-173">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5040e-173">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5040e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-176">La ruta de acceso al VHD que se monta.</span><span class="sxs-lookup"><span data-stu-id="5040e-176">The path to the VHD that is mounted.</span></span> <span data-ttu-id="5040e-177">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5040e-177">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5040e-178">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="5040e-178">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-179">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5040e-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-181">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="5040e-181">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5040e-182">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="5040e-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-183">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5040e-183">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-184">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5040e-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5040e-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-186">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5040e-186">The current status of the object.</span></span> <span data-ttu-id="5040e-187">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="5040e-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-188">**PathId**</span><span class="sxs-lookup"><span data-stu-id="5040e-188">**PathId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-189">Tipo de datos: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="5040e-189">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5040e-191">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5040e-191">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5040e-192">IDENTIFICADOR de la ruta de acceso de dirección SCSI.</span><span class="sxs-lookup"><span data-stu-id="5040e-192">The SCSI address path ID.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-193">**PnpDevicePath**</span><span class="sxs-lookup"><span data-stu-id="5040e-193">**PnpDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5040e-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-196">La ruta de acceso del dispositivo PNP.</span><span class="sxs-lookup"><span data-stu-id="5040e-196">The PNP device path.</span></span>

<span data-ttu-id="5040e-197">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="5040e-197">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-198">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="5040e-198">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-199">Tipo de datos: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="5040e-199">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5040e-201">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5040e-201">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5040e-202">El número de puerto de la dirección SCSI.</span><span class="sxs-lookup"><span data-stu-id="5040e-202">The SCSI address port number.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-203">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="5040e-203">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-204">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5040e-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-206">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="5040e-206">Provides high level status information.</span></span> <span data-ttu-id="5040e-207">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="5040e-207">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="5040e-208">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="5040e-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-209">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5040e-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5040e-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-212">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en "OK".</span><span class="sxs-lookup"><span data-stu-id="5040e-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="5040e-213">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5040e-213">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-214">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="5040e-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5040e-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-216">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="5040e-216">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="5040e-217">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="5040e-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="5040e-218">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="5040e-218">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-219">Tipo de datos: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="5040e-219">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5040e-221">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5040e-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5040e-222">IDENTIFICADOR de destino de la dirección SCSI.</span><span class="sxs-lookup"><span data-stu-id="5040e-222">The SCSI address target ID.</span></span>

</dd> <dt>

<span data-ttu-id="5040e-223">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5040e-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5040e-224">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5040e-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5040e-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5040e-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5040e-226">El tipo de imagen de almacenamiento montada.</span><span class="sxs-lookup"><span data-stu-id="5040e-226">The type of storage image mounted.</span></span>

<dt>

<span id="Virtual_Hard_Disk"></span><span id="virtual_hard_disk"></span><span id="VIRTUAL_HARD_DISK"></span>

<span data-ttu-id="5040e-227">**Disco duro virtual** (0)</span><span class="sxs-lookup"><span data-stu-id="5040e-227">**Virtual Hard Disk** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_Image"></span><span id="iso_image"></span><span id="ISO_IMAGE"></span>

<span data-ttu-id="5040e-228">**Imagen ISO** (1)</span><span class="sxs-lookup"><span data-stu-id="5040e-228">**ISO Image** (1)</span></span>


<span data-ttu-id="5040e-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5040e-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5040e-230">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5040e-230">Remarks</span></span>

<span data-ttu-id="5040e-231">El acceso a la clase **MSVM \_ MountedStorageImage** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="5040e-231">Access to the **Msvm\_MountedStorageImage** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5040e-232">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5040e-232">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5040e-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5040e-233">Requirements</span></span>



| <span data-ttu-id="5040e-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="5040e-234">Requirement</span></span> | <span data-ttu-id="5040e-235">Value</span><span class="sxs-lookup"><span data-stu-id="5040e-235">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5040e-236">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5040e-236">Minimum supported client</span></span><br/> | <span data-ttu-id="5040e-237">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5040e-237">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5040e-238">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5040e-238">Minimum supported server</span></span><br/> | <span data-ttu-id="5040e-239">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5040e-239">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5040e-240">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5040e-240">Namespace</span></span><br/>                | <span data-ttu-id="5040e-241">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5040e-241">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5040e-242">MOF</span><span class="sxs-lookup"><span data-stu-id="5040e-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5040e-243"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5040e-243"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5040e-244">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5040e-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5040e-245"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5040e-245"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5040e-246">Vea también</span><span class="sxs-lookup"><span data-stu-id="5040e-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5040e-247">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="5040e-247">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="5040e-248">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="5040e-248">**CIM\_LogicalElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalelement)
</dt> <dt>

[<span data-ttu-id="5040e-249">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="5040e-249">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

