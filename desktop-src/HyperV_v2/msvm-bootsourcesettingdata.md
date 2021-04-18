---
description: Representa los parámetros para establecer el origen de arranque de una máquina virtual.
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Msvm_BootSourceSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687030"
---
# <a name="msvm_bootsourcesettingdata-class"></a><span data-ttu-id="3905d-103">MSVM \_ BootSourceSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="3905d-103">Msvm\_BootSourceSettingData class</span></span>

<span data-ttu-id="3905d-104">Representa los parámetros para establecer el origen de arranque de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3905d-104">Represents the parameters to set the boot source of a virtual machine.</span></span> <span data-ttu-id="3905d-105">Esta clase se deriva de [**un \_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3905d-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="3905d-106">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3905d-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3905d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3905d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a><span data-ttu-id="3905d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3905d-108">Members</span></span>

<span data-ttu-id="3905d-109">La clase **MSVM \_ BootSourceSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3905d-109">The **Msvm\_BootSourceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3905d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3905d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3905d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3905d-111">Properties</span></span>

<span data-ttu-id="3905d-112">La clase **MSVM \_ BootSourceSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3905d-112">The **Msvm\_BootSourceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3905d-113">**BootSourceDescription**</span><span class="sxs-lookup"><span data-stu-id="3905d-113">**BootSourceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3905d-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3905d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3905d-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3905d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3905d-116">La descripción del origen de arranque proporcionado por el firmware.</span><span class="sxs-lookup"><span data-stu-id="3905d-116">The description of the boot source provided by the firmware.</span></span>

</dd> <dt>

<span data-ttu-id="3905d-117">**BootSourceType**</span><span class="sxs-lookup"><span data-stu-id="3905d-117">**BootSourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3905d-118">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3905d-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3905d-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3905d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3905d-120">Un valor de enumeración que especifica el tipo del origen de arranque.</span><span class="sxs-lookup"><span data-stu-id="3905d-120">An enumeration value that specifies the type of the boot source.</span></span>

<span data-ttu-id="3905d-121">Estos son los valores válidos:</span><span class="sxs-lookup"><span data-stu-id="3905d-121">These are valid values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3905d-122">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3905d-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

<span data-ttu-id="3905d-123">**Unidad** (1)</span><span class="sxs-lookup"><span data-stu-id="3905d-123">**Drive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="3905d-124">**Red** (2)</span><span class="sxs-lookup"><span data-stu-id="3905d-124">**Network** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

<span data-ttu-id="3905d-125">**Archivo** (3)</span><span class="sxs-lookup"><span data-stu-id="3905d-125">**File** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3905d-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3905d-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3905d-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3905d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3905d-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3905d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3905d-129">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="3905d-129">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="3905d-130">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="3905d-130">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="3905d-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3905d-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3905d-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3905d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3905d-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3905d-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3905d-134">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="3905d-134">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="3905d-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3905d-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3905d-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3905d-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3905d-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3905d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3905d-138">Nombre para mostrar de esta instancia de SettingData.</span><span class="sxs-lookup"><span data-stu-id="3905d-138">The display name for this instance of SettingData.</span></span> <span data-ttu-id="3905d-139">Además, el nombre para mostrar se puede usar como una propiedad de índice para una búsqueda o una consulta.</span><span class="sxs-lookup"><span data-stu-id="3905d-139">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="3905d-140">(Nota: el nombre no tiene que ser único dentro de un espacio de nombres).</span><span class="sxs-lookup"><span data-stu-id="3905d-140">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="3905d-141">**FirmwareDevicePath**</span><span class="sxs-lookup"><span data-stu-id="3905d-141">**FirmwareDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3905d-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3905d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3905d-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3905d-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3905d-144">La ruta de acceso nativa que el firmware utiliza para describir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3905d-144">The native path that the firmware uses to describe the device.</span></span>

</dd> <dt>

<span data-ttu-id="3905d-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3905d-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3905d-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3905d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3905d-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3905d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3905d-148">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="3905d-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3905d-149">Dentro del ámbito del espacio de nombres de la creación de instancias, InstanceID identifica de forma opaca y única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="3905d-149">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3905d-150">Para garantizar la unicidad dentro del espacio de nombres, el valor de InstanceID debe construirse con el siguiente algoritmo "preferido": *OrgID*:*LocalID* donde *orgid* y *LocalID* se separan mediante dos puntos (:), y donde *OrgID* debe incluir un nombre con copyright, marca comercial o de otro tipo que sea propiedad de la entidad empresarial que está creando o definiendo el InstanceID o que es un ID</span><span class="sxs-lookup"><span data-stu-id="3905d-150">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="3905d-151">(Este requisito es similar al de *SchemaName* \_ Estructura *className* de los nombres de clase de esquema.) Además, para garantizar la exclusividad, *OrgID* no debe contener dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="3905d-151">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="3905d-152">Al usar este algoritmo, el primer signo de dos puntos que aparece en InstanceID debe aparecer entre *OrgID* y *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="3905d-152">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="3905d-153">La entidad empresarial elige *LocalID* y no se debe volver a usar para identificar distintos elementos subyacentes (del mundo real).</span><span class="sxs-lookup"><span data-stu-id="3905d-153">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="3905d-154">Si no se utiliza el algoritmo preferido anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún InstanceIDs producido por este u otros proveedores para el espacio de nombres de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="3905d-154">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="3905d-155">En el caso de las instancias definidas por DMTF, el algoritmo "preferido" se debe usar con el valor de *OrgID* establecido en CIM.</span><span class="sxs-lookup"><span data-stu-id="3905d-155">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="3905d-156">**OptionalData**</span><span class="sxs-lookup"><span data-stu-id="3905d-156">**OptionalData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3905d-157">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="3905d-157">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3905d-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3905d-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3905d-159">Calificadores: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="3905d-159">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="3905d-160">Datos opcionales proporcionados por el firmware.</span><span class="sxs-lookup"><span data-stu-id="3905d-160">Optional data provided by the firmware.</span></span>

> [!Note]  
> <span data-ttu-id="3905d-161">Propiedad agregada en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="3905d-161">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="3905d-162">**OtherLocation**</span><span class="sxs-lookup"><span data-stu-id="3905d-162">**OtherLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3905d-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3905d-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3905d-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3905d-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3905d-165">La otra información de ubicación, si la hay, que el firmware usa para identificar de forma única el origen de arranque.</span><span class="sxs-lookup"><span data-stu-id="3905d-165">The other location info, if any, that the firmware uses to further uniquely identify the boot source.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3905d-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3905d-166">Requirements</span></span>



| <span data-ttu-id="3905d-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="3905d-167">Requirement</span></span> | <span data-ttu-id="3905d-168">Value</span><span class="sxs-lookup"><span data-stu-id="3905d-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3905d-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3905d-169">Minimum supported client</span></span><br/> | <span data-ttu-id="3905d-170">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="3905d-170">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3905d-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3905d-171">Minimum supported server</span></span><br/> | <span data-ttu-id="3905d-172">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3905d-172">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3905d-173">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3905d-173">Namespace</span></span><br/>                | <span data-ttu-id="3905d-174">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3905d-174">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3905d-175">MOF</span><span class="sxs-lookup"><span data-stu-id="3905d-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3905d-176"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3905d-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3905d-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3905d-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3905d-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3905d-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3905d-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="3905d-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3905d-180">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3905d-180">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="3905d-181">[**SettingData de CIM \_**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3905d-181">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

