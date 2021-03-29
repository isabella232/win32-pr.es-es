---
description: Cambia los permisos de seguridad para el archivo de códec especificado en la ruta de acceso del objeto (este método es una versión extendida del método ChangeSecurityPermissions).
ms.assetid: 3eac4ae1-3c0e-4e81-8b23-9ad8698f723c
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx de la clase Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 549c55a5066bdaba4699ec76ed3b7be23eb28b96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907185"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="e6973-103">Método ChangeSecurityPermissionsEx de la \_ clase CodecFile de Win32</span><span class="sxs-lookup"><span data-stu-id="e6973-103">ChangeSecurityPermissionsEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="e6973-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** cambia los permisos de seguridad para el archivo de códec especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="e6973-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the codec file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="e6973-105">Si el archivo lógico es un directorio, este método es recursivo y cambia los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="e6973-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="e6973-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e6973-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e6973-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e6973-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6973-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6973-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="e6973-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6973-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6973-110">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6973-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6973-111">Expresión que se resuelve como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="e6973-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="e6973-112">Este descriptor contiene nuevos permisos de seguridad para la instancia de [**Win32 \_ CodecFile**](win32-codecfile.md).</span><span class="sxs-lookup"><span data-stu-id="e6973-112">This descriptor contains new security permissions for the instance of [**Win32\_CodecFile**](win32-codecfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6973-113">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e6973-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6973-114">Privilegio de seguridad real que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="e6973-114">Actual security privilege to be modified.</span></span> <span data-ttu-id="e6973-115">Por ejemplo, para cambiar el propietario y la seguridad de la lista de control de acceso discrecional (DACL), use lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e6973-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="e6973-116">O bien</span><span class="sxs-lookup"><span data-stu-id="e6973-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="e6973-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="e6973-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="e6973-118">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e6973-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="e6973-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="e6973-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="e6973-120">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e6973-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="e6973-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="e6973-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="e6973-122">Cambie la lista de control de acceso discrecional (DACL) del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e6973-122">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="e6973-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="e6973-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="e6973-124">Cambie la lista de control de acceso de sistema (SACL) del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e6973-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e6973-125">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e6973-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6973-126">Nombre del archivo o directorio en el que se produjo un error en el método **ChangeSecurityPermissionsEx** .</span><span class="sxs-lookup"><span data-stu-id="e6973-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="e6973-127">Este parámetro es NULL cuando el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="e6973-127">This parameter is null when the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-128">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e6973-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e6973-129">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **ChangeSecurityPermissionsEx**.</span><span class="sxs-lookup"><span data-stu-id="e6973-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="e6973-130">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="e6973-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="e6973-131">Si este parámetro es null, la operación se realiza en el archivo o directorio especificado en la llamada [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="e6973-131">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-132">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e6973-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e6973-133">Si **es true**, los cambios de propiedad se aplican de forma recursiva a los archivos y directorios del directorio que especifica la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="e6973-133">If **true**, the changes of ownership are applied recursively to files and directories in the directory that the [**CIM\_LogicalFile**](cim-logicalfile.md) instance specifies.</span></span> <span data-ttu-id="e6973-134">En el caso de las instancias de archivo, se omite el parámetro de entrada *recursivo* .</span><span class="sxs-lookup"><span data-stu-id="e6973-134">For file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6973-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6973-135">Return value</span></span>

<span data-ttu-id="e6973-136">Devuelve un valor de 0 (cero) si se cambian los permisos y un número diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="e6973-136">Returns an value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e6973-137">**Success**</span><span class="sxs-lookup"><span data-stu-id="e6973-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-138">0</span><span class="sxs-lookup"><span data-stu-id="e6973-138">0</span></span>

<span data-ttu-id="e6973-139">La solicitud es correcta.</span><span class="sxs-lookup"><span data-stu-id="e6973-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-140">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="e6973-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-141">2</span><span class="sxs-lookup"><span data-stu-id="e6973-141">2</span></span>

<span data-ttu-id="e6973-142">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="e6973-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-143">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="e6973-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-144">8</span><span class="sxs-lookup"><span data-stu-id="e6973-144">8</span></span>

<span data-ttu-id="e6973-145">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="e6973-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-146">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="e6973-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-147">9</span><span class="sxs-lookup"><span data-stu-id="e6973-147">9</span></span>

<span data-ttu-id="e6973-148">El nombre especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="e6973-148">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-149">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="e6973-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-150">10</span><span class="sxs-lookup"><span data-stu-id="e6973-150">10</span></span>

<span data-ttu-id="e6973-151">El objeto especificado ya existe</span><span class="sxs-lookup"><span data-stu-id="e6973-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-152">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="e6973-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-153">11</span><span class="sxs-lookup"><span data-stu-id="e6973-153">11</span></span>

<span data-ttu-id="e6973-154">El sistema de archivos no es un sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="e6973-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-155">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="e6973-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-156">12</span><span class="sxs-lookup"><span data-stu-id="e6973-156">12</span></span>

<span data-ttu-id="e6973-157">La plataforma no es Windows NT ni Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e6973-157">The platform is not Windows NT or Windows 2000.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-158">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="e6973-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-159">13</span><span class="sxs-lookup"><span data-stu-id="e6973-159">13</span></span>

<span data-ttu-id="e6973-160">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="e6973-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-161">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="e6973-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-162">14</span><span class="sxs-lookup"><span data-stu-id="e6973-162">14</span></span>

<span data-ttu-id="e6973-163">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="e6973-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-164">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="e6973-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-165">15</span><span class="sxs-lookup"><span data-stu-id="e6973-165">15</span></span>

<span data-ttu-id="e6973-166">Hay una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="e6973-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-167">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="e6973-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-168">16</span><span class="sxs-lookup"><span data-stu-id="e6973-168">16</span></span>

<span data-ttu-id="e6973-169">El archivo de inicio especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="e6973-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-170">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="e6973-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-171">17</span><span class="sxs-lookup"><span data-stu-id="e6973-171">17</span></span>

<span data-ttu-id="e6973-172">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="e6973-172">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="e6973-173">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="e6973-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e6973-174">21</span><span class="sxs-lookup"><span data-stu-id="e6973-174">21</span></span>

<span data-ttu-id="e6973-175">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="e6973-175">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6973-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6973-176">Requirements</span></span>



| <span data-ttu-id="e6973-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6973-177">Requirement</span></span> | <span data-ttu-id="e6973-178">Value</span><span class="sxs-lookup"><span data-stu-id="e6973-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6973-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6973-179">Minimum supported client</span></span><br/> | <span data-ttu-id="e6973-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6973-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e6973-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6973-181">Minimum supported server</span></span><br/> | <span data-ttu-id="e6973-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6973-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e6973-183">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e6973-183">Namespace</span></span><br/>                | <span data-ttu-id="e6973-184">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e6973-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e6973-185">MOF</span><span class="sxs-lookup"><span data-stu-id="e6973-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6973-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6973-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6973-187">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e6973-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6973-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6973-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6973-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6973-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6973-190">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e6973-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e6973-191">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="e6973-191">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

