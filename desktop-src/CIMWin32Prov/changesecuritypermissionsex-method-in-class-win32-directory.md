---
description: Cambia los permisos de seguridad para el archivo de entrada de directorio especificado en la ruta de acceso del objeto (este método es una versión extendida del método ChangeSecurityPermissions).
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4bcadd4a4ad115a1a367db4f2a2f645eb6a4742c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274935"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a><span data-ttu-id="f8858-103">Método ChangeSecurityPermissionsEx de la \_ clase de directorio Win32</span><span class="sxs-lookup"><span data-stu-id="f8858-103">ChangeSecurityPermissionsEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="f8858-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** cambia los permisos de seguridad para el archivo de entrada de directorio especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="f8858-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="f8858-105">Si el archivo lógico es un directorio, este método es recursivo y cambia los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="f8858-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="f8858-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f8858-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f8858-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f8858-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8858-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8858-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="f8858-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8858-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8858-110">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8858-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8858-111">Expresión que se resuelve como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="f8858-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="f8858-112">Este parámetro contiene nuevos permisos de seguridad para la instancia de archivo de [**\_ paginación de Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="f8858-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8858-113">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f8858-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8858-114">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="f8858-114">Security privilege to be modified.</span></span> <span data-ttu-id="f8858-115">Por ejemplo, para cambiar el propietario y la seguridad de la lista de control de acceso discrecional (DACL), use lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f8858-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="f8858-116">O bien</span><span class="sxs-lookup"><span data-stu-id="f8858-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="f8858-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="f8858-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f8858-118">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f8858-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="f8858-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="f8858-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f8858-120">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f8858-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="f8858-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="f8858-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f8858-122">Cambiar la lista de DACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f8858-122">Change the DACL list of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="f8858-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="f8858-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f8858-124">Cambie la lista de control de acceso de sistema (SACL) del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f8858-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f8858-125">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f8858-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8858-126">Nombre del archivo o directorio en el que se produjo un error en el método **ChangeSecurityPermissionsEx** .</span><span class="sxs-lookup"><span data-stu-id="f8858-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="f8858-127">Este parámetro es NULL si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="f8858-127">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-128">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f8858-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8858-129">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **ChangeSecurityPermissionsEx**.</span><span class="sxs-lookup"><span data-stu-id="f8858-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="f8858-130">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="f8858-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="f8858-131">Si este parámetro es null, la operación se realiza en el archivo o directorio especificado en la llamada **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="f8858-131">If this parameter is null, the operation is performed on the file or directory that is specified in the **ExecMethod** call.</span></span> <span data-ttu-id="f8858-132">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="f8858-132">This parameter is optional.</span></span>

<span data-ttu-id="f8858-133">Si se utiliza *StartFileName* , *Recursive* también debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="f8858-133">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-134">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f8858-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8858-135">Si es **true**, el cambio de propiedad se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="f8858-135">If **true**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="f8858-136">En el caso de las instancias de archivo, se omite el parámetro de entrada *recursivo* .</span><span class="sxs-lookup"><span data-stu-id="f8858-136">For file instances, the *Recursive* input parameter is ignored.</span></span> <span data-ttu-id="f8858-137">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="f8858-137">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8858-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8858-138">Return value</span></span>

<span data-ttu-id="f8858-139">Devuelve un valor de 0 (cero) si se cambian los permisos y un número diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="f8858-139">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f8858-140">**Success**</span><span class="sxs-lookup"><span data-stu-id="f8858-140">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-141">0</span><span class="sxs-lookup"><span data-stu-id="f8858-141">0</span></span>

<span data-ttu-id="f8858-142">La solicitud es correcta.</span><span class="sxs-lookup"><span data-stu-id="f8858-142">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-143">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="f8858-143">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-144">2</span><span class="sxs-lookup"><span data-stu-id="f8858-144">2</span></span>

<span data-ttu-id="f8858-145">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="f8858-145">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-146">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="f8858-146">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-147">8</span><span class="sxs-lookup"><span data-stu-id="f8858-147">8</span></span>

<span data-ttu-id="f8858-148">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f8858-148">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-149">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="f8858-149">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-150">9</span><span class="sxs-lookup"><span data-stu-id="f8858-150">9</span></span>

<span data-ttu-id="f8858-151">El nombre especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="f8858-151">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-152">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="f8858-152">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-153">10</span><span class="sxs-lookup"><span data-stu-id="f8858-153">10</span></span>

<span data-ttu-id="f8858-154">El objeto especificado ya existe</span><span class="sxs-lookup"><span data-stu-id="f8858-154">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-155">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="f8858-155">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-156">11</span><span class="sxs-lookup"><span data-stu-id="f8858-156">11</span></span>

<span data-ttu-id="f8858-157">El sistema de archivos no es un sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="f8858-157">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-158">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="f8858-158">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-159">12</span><span class="sxs-lookup"><span data-stu-id="f8858-159">12</span></span>

<span data-ttu-id="f8858-160">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="f8858-160">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-161">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="f8858-161">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-162">13</span><span class="sxs-lookup"><span data-stu-id="f8858-162">13</span></span>

<span data-ttu-id="f8858-163">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="f8858-163">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-164">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="f8858-164">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-165">14</span><span class="sxs-lookup"><span data-stu-id="f8858-165">14</span></span>

<span data-ttu-id="f8858-166">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="f8858-166">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-167">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="f8858-167">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-168">15</span><span class="sxs-lookup"><span data-stu-id="f8858-168">15</span></span>

<span data-ttu-id="f8858-169">Hay una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="f8858-169">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-170">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="f8858-170">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-171">16</span><span class="sxs-lookup"><span data-stu-id="f8858-171">16</span></span>

<span data-ttu-id="f8858-172">El archivo de inicio especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="f8858-172">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-173">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="f8858-173">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-174">17</span><span class="sxs-lookup"><span data-stu-id="f8858-174">17</span></span>

<span data-ttu-id="f8858-175">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="f8858-175">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f8858-176">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="f8858-176">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f8858-177">21</span><span class="sxs-lookup"><span data-stu-id="f8858-177">21</span></span>

<span data-ttu-id="f8858-178">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="f8858-178">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8858-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8858-179">Requirements</span></span>



| <span data-ttu-id="f8858-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8858-180">Requirement</span></span> | <span data-ttu-id="f8858-181">Value</span><span class="sxs-lookup"><span data-stu-id="f8858-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8858-182">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8858-182">Minimum supported client</span></span><br/> | <span data-ttu-id="f8858-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8858-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8858-184">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8858-184">Minimum supported server</span></span><br/> | <span data-ttu-id="f8858-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8858-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8858-186">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f8858-186">Namespace</span></span><br/>                | <span data-ttu-id="f8858-187">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f8858-187">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8858-188">MOF</span><span class="sxs-lookup"><span data-stu-id="f8858-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8858-189"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8858-189"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8858-190">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8858-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8858-191"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8858-191"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8858-192">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8858-192">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8858-193">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8858-193">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f8858-194">**\_Directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="f8858-194">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

