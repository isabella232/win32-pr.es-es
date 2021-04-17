---
description: Representa los parámetros para copiar un archivo del host en el invitado.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Msvm_CopyFileToGuestSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 05e27340acc9dd341bec7857c164f50344abc36f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688362"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a><span data-ttu-id="dbca4-103">MSVM \_ CopyFileToGuestSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="dbca4-103">Msvm\_CopyFileToGuestSettingData class</span></span>

<span data-ttu-id="dbca4-104">Representa los parámetros para copiar un archivo del host en el invitado.</span><span class="sxs-lookup"><span data-stu-id="dbca4-104">Represents the parameters for copying a file from the host into the guest.</span></span> <span data-ttu-id="dbca4-105">Esta clase se deriva de [**un \_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dbca4-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="dbca4-106">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="dbca4-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbca4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbca4-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="dbca4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dbca4-108">Members</span></span>

<span data-ttu-id="dbca4-109">La clase **MSVM \_ CopyFileToGuestSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dbca4-109">The **Msvm\_CopyFileToGuestSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="dbca4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbca4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbca4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbca4-111">Properties</span></span>

<span data-ttu-id="dbca4-112">La clase **MSVM \_ CopyFileToGuestSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dbca4-112">The **Msvm\_CopyFileToGuestSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbca4-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dbca4-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbca4-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dbca4-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbca4-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbca4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbca4-116">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="dbca4-116">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="dbca4-117">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="dbca4-117">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="dbca4-118">**CreateFullPath**</span><span class="sxs-lookup"><span data-stu-id="dbca4-118">**CreateFullPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbca4-119">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dbca4-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbca4-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbca4-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbca4-121">Indica si los directorios que faltan en la ruta de acceso del archivo de destino deben crearse antes de copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="dbca4-121">Indicates whether missing directories in the destination file's path must be created before copying the file.</span></span>

</dd> <dt>

<span data-ttu-id="dbca4-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dbca4-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbca4-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dbca4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbca4-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbca4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbca4-125">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="dbca4-125">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="dbca4-126">**DestinationPath**</span><span class="sxs-lookup"><span data-stu-id="dbca4-126">**DestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbca4-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dbca4-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbca4-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbca4-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbca4-129">Ruta de acceso completa del archivo de destino que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="dbca4-129">The complete path of the destination file to be copied.</span></span> <span data-ttu-id="dbca4-130">Este archivo de destino debe ser accesible para el invitado y puede contener variables de entorno, que se expanden mediante el invitado.</span><span class="sxs-lookup"><span data-stu-id="dbca4-130">This destination file must be accessible to the guest and can contain environment variables, which are expanded by the guest.</span></span> <span data-ttu-id="dbca4-131">Si la ruta de acceso especificada es un directorio existente en el invitado, el archivo de destino se crea en este directorio.</span><span class="sxs-lookup"><span data-stu-id="dbca4-131">If the path specified is an existing directory in the guest, the destination file is created in this directory.</span></span> <span data-ttu-id="dbca4-132">En este caso, el nombre de archivo de **SourcePath** se utiliza como nombre de archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="dbca4-132">In this case, the file name from **SourcePath** is used as the destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="dbca4-133">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dbca4-133">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbca4-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dbca4-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbca4-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbca4-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbca4-136">Nombre para mostrar de esta instancia de SettingData.</span><span class="sxs-lookup"><span data-stu-id="dbca4-136">The display name for this instance of SettingData.</span></span> <span data-ttu-id="dbca4-137">Además, el nombre para mostrar se puede usar como una propiedad de índice para una búsqueda o una consulta.</span><span class="sxs-lookup"><span data-stu-id="dbca4-137">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="dbca4-138">(Nota: el nombre no tiene que ser único dentro de un espacio de nombres).</span><span class="sxs-lookup"><span data-stu-id="dbca4-138">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="dbca4-139">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dbca4-139">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbca4-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dbca4-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbca4-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbca4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbca4-142">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="dbca4-142">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dbca4-143">Dentro del ámbito del espacio de nombres de la creación de instancias, InstanceID identifica de forma opaca y única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="dbca4-143">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dbca4-144">Para garantizar la unicidad dentro del espacio de nombres, el valor de InstanceID debe construirse con el siguiente algoritmo "preferido": *OrgID*:*LocalID* donde *orgid* y *LocalID* se separan mediante dos puntos (:), y donde *OrgID* debe incluir un nombre con copyright, marca comercial o de otro tipo que sea propiedad de la entidad empresarial que está creando o definiendo el InstanceID o que es un ID</span><span class="sxs-lookup"><span data-stu-id="dbca4-144">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="dbca4-145">(Este requisito es similar al de *SchemaName* \_ Estructura *className* de los nombres de clase de esquema.) Además, para garantizar la exclusividad, *OrgID* no debe contener dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="dbca4-145">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="dbca4-146">Al usar este algoritmo, el primer signo de dos puntos que aparece en InstanceID debe aparecer entre *OrgID* y *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="dbca4-146">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="dbca4-147">La entidad empresarial elige *LocalID* y no se debe volver a usar para identificar distintos elementos subyacentes (del mundo real).</span><span class="sxs-lookup"><span data-stu-id="dbca4-147">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="dbca4-148">Si no se utiliza el algoritmo preferido anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún InstanceIDs producido por este u otros proveedores para el espacio de nombres de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="dbca4-148">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="dbca4-149">En el caso de las instancias definidas por DMTF, el algoritmo "preferido" se debe usar con el valor de *OrgID* establecido en CIM.</span><span class="sxs-lookup"><span data-stu-id="dbca4-149">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="dbca4-150">**OverwriteExisting**</span><span class="sxs-lookup"><span data-stu-id="dbca4-150">**OverwriteExisting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbca4-151">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dbca4-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbca4-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbca4-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbca4-153">Indica si se debe sobrescribir un archivo de destino existente.</span><span class="sxs-lookup"><span data-stu-id="dbca4-153">Indicates whether an existing destination file must be overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="dbca4-154">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="dbca4-154">**SourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbca4-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dbca4-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbca4-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dbca4-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbca4-157">Ruta de acceso completa del archivo de código fuente que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="dbca4-157">The complete path of the source file to be copied.</span></span> <span data-ttu-id="dbca4-158">Este archivo de origen debe ser accesible para el host de Hyper-V y puede contener variables de entorno, que se expanden mediante el host de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="dbca4-158">This source file must be accessible to the Hyper-V host and can contain environment variables, which are expanded by the Hyper-V host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbca4-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbca4-159">Requirements</span></span>



| <span data-ttu-id="dbca4-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbca4-160">Requirement</span></span> | <span data-ttu-id="dbca4-161">Value</span><span class="sxs-lookup"><span data-stu-id="dbca4-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbca4-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbca4-162">Minimum supported client</span></span><br/> | <span data-ttu-id="dbca4-163">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="dbca4-163">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="dbca4-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dbca4-164">Minimum supported server</span></span><br/> | <span data-ttu-id="dbca4-165">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dbca4-165">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dbca4-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dbca4-166">Namespace</span></span><br/>                | <span data-ttu-id="dbca4-167">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="dbca4-167">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dbca4-168">MOF</span><span class="sxs-lookup"><span data-stu-id="dbca4-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbca4-169"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbca4-169"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbca4-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dbca4-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbca4-171"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbca4-171"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dbca4-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbca4-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbca4-173">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="dbca4-173">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="dbca4-174">[**SettingData de CIM \_**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dbca4-174">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

