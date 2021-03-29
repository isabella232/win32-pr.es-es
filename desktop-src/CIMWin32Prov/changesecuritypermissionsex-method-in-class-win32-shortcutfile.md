---
description: Cambia los permisos de seguridad para el archivo de método abreviado lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método ChangeSecurityPermissions).
ms.assetid: 9a5c9fa9-ccd9-4792-969f-28f52ab9bc52
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx de la clase Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 124f8d883b89379e4b36c5dd33b029718fbbd469
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538781"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="d6bcf-103">Método ChangeSecurityPermissionsEx de la \_ clase ShortcutFile de Win32</span><span class="sxs-lookup"><span data-stu-id="d6bcf-103">ChangeSecurityPermissionsEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="d6bcf-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** cambia los permisos de seguridad para el archivo de acceso directo lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="d6bcf-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical shortcut file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="d6bcf-105">Si el archivo lógico es un directorio, este método es recursivo y cambia los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="d6bcf-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d6bcf-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d6bcf-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d6bcf-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6bcf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6bcf-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="d6bcf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6bcf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6bcf-110">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d6bcf-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-111">Expresión que se resuelve como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="d6bcf-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="d6bcf-112">Este parámetro contiene nuevos permisos de seguridad para la instancia de archivo de [**\_ paginación de Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="d6bcf-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-113">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d6bcf-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-114">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-114">Security privilege to be modified.</span></span> <span data-ttu-id="d6bcf-115">Por ejemplo, para cambiar el propietario y la seguridad de la lista de control de acceso discrecional (DACL), use lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d6bcf-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="d6bcf-116">or</span><span class="sxs-lookup"><span data-stu-id="d6bcf-116">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="d6bcf-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="d6bcf-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d6bcf-118">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="d6bcf-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="d6bcf-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d6bcf-120">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="d6bcf-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="d6bcf-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d6bcf-122">Cambie la lista de control de acceso discrecional (DACL) del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-122">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="d6bcf-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="d6bcf-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d6bcf-124">Cambie la lista de control de acceso de sistema (SACL) del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d6bcf-125">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d6bcf-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-126">Nombre del archivo o directorio en el que se produjo un error en el método **ChangeSecurityPermissionsEx** .</span><span class="sxs-lookup"><span data-stu-id="d6bcf-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="d6bcf-127">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-127">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-128">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d6bcf-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-129">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **ChangeSecurityPermissionsEx**.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="d6bcf-130">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="d6bcf-131">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="d6bcf-131">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-132">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d6bcf-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-133">Si es **true**, el cambio de propiedad se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="d6bcf-133">If **true**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="d6bcf-134">En el caso de las instancias de archivo, se omite el parámetro *Recursive* .</span><span class="sxs-lookup"><span data-stu-id="d6bcf-134">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6bcf-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6bcf-135">Return value</span></span>

<span data-ttu-id="d6bcf-136">Devuelve un valor de 0 (cero) si se cambian los permisos y un número diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-136">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d6bcf-137">**Success**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-138">0</span><span class="sxs-lookup"><span data-stu-id="d6bcf-138">0</span></span>

<span data-ttu-id="d6bcf-139">La solicitud es correcta.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-140">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-141">2</span><span class="sxs-lookup"><span data-stu-id="d6bcf-141">2</span></span>

<span data-ttu-id="d6bcf-142">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-143">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-144">8</span><span class="sxs-lookup"><span data-stu-id="d6bcf-144">8</span></span>

<span data-ttu-id="d6bcf-145">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-146">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-147">9</span><span class="sxs-lookup"><span data-stu-id="d6bcf-147">9</span></span>

<span data-ttu-id="d6bcf-148">El nombre especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-148">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-149">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-150">10</span><span class="sxs-lookup"><span data-stu-id="d6bcf-150">10</span></span>

<span data-ttu-id="d6bcf-151">El objeto especificado ya existe</span><span class="sxs-lookup"><span data-stu-id="d6bcf-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-152">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-153">11</span><span class="sxs-lookup"><span data-stu-id="d6bcf-153">11</span></span>

<span data-ttu-id="d6bcf-154">El sistema de archivos no es el sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-154">The file system is not NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-155">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-156">12</span><span class="sxs-lookup"><span data-stu-id="d6bcf-156">12</span></span>

<span data-ttu-id="d6bcf-157">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-157">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-158">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-159">13</span><span class="sxs-lookup"><span data-stu-id="d6bcf-159">13</span></span>

<span data-ttu-id="d6bcf-160">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-161">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-162">14</span><span class="sxs-lookup"><span data-stu-id="d6bcf-162">14</span></span>

<span data-ttu-id="d6bcf-163">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-164">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-165">15</span><span class="sxs-lookup"><span data-stu-id="d6bcf-165">15</span></span>

<span data-ttu-id="d6bcf-166">Hay una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-167">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-168">16</span><span class="sxs-lookup"><span data-stu-id="d6bcf-168">16</span></span>

<span data-ttu-id="d6bcf-169">El archivo de inicio especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-170">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-171">17</span><span class="sxs-lookup"><span data-stu-id="d6bcf-171">17</span></span>

<span data-ttu-id="d6bcf-172">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-172">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d6bcf-173">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d6bcf-174">21</span><span class="sxs-lookup"><span data-stu-id="d6bcf-174">21</span></span>

<span data-ttu-id="d6bcf-175">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="d6bcf-175">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6bcf-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6bcf-176">Requirements</span></span>



| <span data-ttu-id="d6bcf-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6bcf-177">Requirement</span></span> | <span data-ttu-id="d6bcf-178">Value</span><span class="sxs-lookup"><span data-stu-id="d6bcf-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6bcf-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6bcf-179">Minimum supported client</span></span><br/> | <span data-ttu-id="d6bcf-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6bcf-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6bcf-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6bcf-181">Minimum supported server</span></span><br/> | <span data-ttu-id="d6bcf-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6bcf-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6bcf-183">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d6bcf-183">Namespace</span></span><br/>                | <span data-ttu-id="d6bcf-184">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d6bcf-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d6bcf-185">MOF</span><span class="sxs-lookup"><span data-stu-id="d6bcf-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6bcf-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6bcf-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6bcf-187">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6bcf-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6bcf-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6bcf-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6bcf-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6bcf-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6bcf-190">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d6bcf-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d6bcf-191">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="d6bcf-191">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

