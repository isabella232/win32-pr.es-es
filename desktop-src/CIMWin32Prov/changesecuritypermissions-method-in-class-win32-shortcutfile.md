---
description: Cambia los permisos de seguridad para el archivo de método abreviado lógico especificado en la ruta de acceso del objeto.
ms.assetid: abd5aec8-4684-4b8d-8fdf-d3a7a5eec103
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions de la clase Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad2d482e0be93a1abec80fc710a1a43d7873dd99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496379"
---
# <a name="changesecuritypermissions-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="3edd0-103">Método ChangeSecurityPermissions de la \_ clase ShortcutFile de Win32</span><span class="sxs-lookup"><span data-stu-id="3edd0-103">ChangeSecurityPermissions method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="3edd0-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** cambia los permisos de seguridad para el archivo de acceso directo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="3edd0-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="3edd0-105">Si el archivo lógico es un directorio, **ChangeSecurityPermissions** es recursivo y cambia los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="3edd0-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span> <span data-ttu-id="3edd0-106">**ChangeSecurityPermissions** devuelve un valor entero de 0 (cero) si se cambian los permisos y otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="3edd0-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="3edd0-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3edd0-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3edd0-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3edd0-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3edd0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3edd0-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="3edd0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3edd0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3edd0-111">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3edd0-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-112">Expresión que se resuelve como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="3edd0-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="3edd0-113">Este descriptor contiene nuevos permisos de seguridad para la instancia de archivo de [**\_ paginación de Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="3edd0-113">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-114">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3edd0-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-115">Privilegio de seguridad real que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="3edd0-115">Actual security privilege to be modified.</span></span> <span data-ttu-id="3edd0-116">Por ejemplo, para cambiar la seguridad de la DACL y el propietario, use:</span><span class="sxs-lookup"><span data-stu-id="3edd0-116">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="3edd0-117">or</span><span class="sxs-lookup"><span data-stu-id="3edd0-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="3edd0-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="3edd0-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3edd0-119">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3edd0-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="3edd0-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="3edd0-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3edd0-121">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3edd0-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="3edd0-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="3edd0-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3edd0-123">Cambie la lista de control de acceso discrecional (DACL) del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3edd0-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="3edd0-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="3edd0-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3edd0-125">Cambie la lista de control de acceso de sistema (SACL) del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3edd0-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3edd0-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3edd0-126">Return value</span></span>

<span data-ttu-id="3edd0-127">Devuelve un valor de 0 (cero) si se cambian los permisos y un número diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="3edd0-127">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3edd0-128">**Success**</span><span class="sxs-lookup"><span data-stu-id="3edd0-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-129">0</span><span class="sxs-lookup"><span data-stu-id="3edd0-129">0</span></span>

<span data-ttu-id="3edd0-130">La solicitud es correcta.</span><span class="sxs-lookup"><span data-stu-id="3edd0-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-131">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="3edd0-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-132">2</span><span class="sxs-lookup"><span data-stu-id="3edd0-132">2</span></span>

<span data-ttu-id="3edd0-133">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="3edd0-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-134">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="3edd0-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-135">8</span><span class="sxs-lookup"><span data-stu-id="3edd0-135">8</span></span>

<span data-ttu-id="3edd0-136">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="3edd0-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-137">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="3edd0-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-138">9</span><span class="sxs-lookup"><span data-stu-id="3edd0-138">9</span></span>

<span data-ttu-id="3edd0-139">El nombre especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="3edd0-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-140">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="3edd0-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-141">10</span><span class="sxs-lookup"><span data-stu-id="3edd0-141">10</span></span>

<span data-ttu-id="3edd0-142">El objeto especificado ya existe</span><span class="sxs-lookup"><span data-stu-id="3edd0-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-143">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="3edd0-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-144">11</span><span class="sxs-lookup"><span data-stu-id="3edd0-144">11</span></span>

<span data-ttu-id="3edd0-145">El sistema de archivos no es un sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="3edd0-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-146">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="3edd0-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-147">12</span><span class="sxs-lookup"><span data-stu-id="3edd0-147">12</span></span>

<span data-ttu-id="3edd0-148">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="3edd0-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-149">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="3edd0-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-150">13</span><span class="sxs-lookup"><span data-stu-id="3edd0-150">13</span></span>

<span data-ttu-id="3edd0-151">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="3edd0-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-152">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="3edd0-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-153">14</span><span class="sxs-lookup"><span data-stu-id="3edd0-153">14</span></span>

<span data-ttu-id="3edd0-154">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="3edd0-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-155">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="3edd0-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-156">15</span><span class="sxs-lookup"><span data-stu-id="3edd0-156">15</span></span>

<span data-ttu-id="3edd0-157">Hay una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="3edd0-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-158">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="3edd0-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-159">16</span><span class="sxs-lookup"><span data-stu-id="3edd0-159">16</span></span>

<span data-ttu-id="3edd0-160">El archivo de inicio especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="3edd0-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-161">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="3edd0-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-162">17</span><span class="sxs-lookup"><span data-stu-id="3edd0-162">17</span></span>

<span data-ttu-id="3edd0-163">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="3edd0-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="3edd0-164">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="3edd0-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3edd0-165">21</span><span class="sxs-lookup"><span data-stu-id="3edd0-165">21</span></span>

<span data-ttu-id="3edd0-166">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="3edd0-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3edd0-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3edd0-167">Requirements</span></span>



| <span data-ttu-id="3edd0-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="3edd0-168">Requirement</span></span> | <span data-ttu-id="3edd0-169">Value</span><span class="sxs-lookup"><span data-stu-id="3edd0-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3edd0-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3edd0-170">Minimum supported client</span></span><br/> | <span data-ttu-id="3edd0-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3edd0-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3edd0-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3edd0-172">Minimum supported server</span></span><br/> | <span data-ttu-id="3edd0-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3edd0-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3edd0-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3edd0-174">Namespace</span></span><br/>                | <span data-ttu-id="3edd0-175">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3edd0-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3edd0-176">MOF</span><span class="sxs-lookup"><span data-stu-id="3edd0-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3edd0-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3edd0-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3edd0-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3edd0-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3edd0-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3edd0-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3edd0-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="3edd0-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="3edd0-181">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3edd0-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3edd0-182">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="3edd0-182">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

