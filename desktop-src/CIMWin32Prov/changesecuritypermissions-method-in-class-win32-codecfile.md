---
description: Cambia los permisos de seguridad para el archivo de códec lógico especificado en la ruta de acceso del objeto.
ms.assetid: d7945666-e514-4bfc-81bc-8e98aa90bcf0
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions de la clase Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b0789164b2bb28b5c3c84e907cf7ae2acb96e01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659334"
---
# <a name="changesecuritypermissions-method-of-the-win32_codecfile-class"></a><span data-ttu-id="c60ae-103">Método ChangeSecurityPermissions de la \_ clase CodecFile de Win32</span><span class="sxs-lookup"><span data-stu-id="c60ae-103">ChangeSecurityPermissions method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="c60ae-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** cambia los permisos de seguridad para el archivo de códec lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c60ae-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical codec file specified in the object path.</span></span> <span data-ttu-id="c60ae-105">Si el archivo lógico es un directorio, **ChangeSecurityPermissions** es recursivo y cambia los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="c60ae-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories the directory contains.</span></span> <span data-ttu-id="c60ae-106">**ChangeSecurityPermissions** devuelve un valor entero de 0 (cero) si se cambian los permisos y otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c60ae-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="c60ae-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c60ae-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c60ae-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c60ae-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c60ae-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c60ae-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="c60ae-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c60ae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c60ae-111">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c60ae-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-112">Expresión que se resuelve como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="c60ae-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="c60ae-113">Este descriptor contiene nuevos permisos de seguridad para la instancia de [**Win32 \_ CodecFile**](win32-codecfile.md).</span><span class="sxs-lookup"><span data-stu-id="c60ae-113">This descriptor contains new security permissions for the instance of [**Win32\_CodecFile**](win32-codecfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-114">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c60ae-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-115">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="c60ae-115">Security privilege to be modified.</span></span> <span data-ttu-id="c60ae-116">Por ejemplo, para cambiar la seguridad de la lista de control de acceso discrecional (DACL) y el propietario, use:</span><span class="sxs-lookup"><span data-stu-id="c60ae-116">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="c60ae-117">O bien</span><span class="sxs-lookup"><span data-stu-id="c60ae-117">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="c60ae-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="c60ae-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="c60ae-119">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c60ae-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="c60ae-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="c60ae-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="c60ae-121">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c60ae-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="c60ae-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="c60ae-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="c60ae-123">Cambie la lista de control de acceso discrecional (DACL) del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c60ae-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="c60ae-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="c60ae-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="c60ae-125">Cambie la lista de control de acceso de sistema (SACL) del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c60ae-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c60ae-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c60ae-126">Return value</span></span>

<span data-ttu-id="c60ae-127">Devuelve un valor de 0 (cero) si se cambian los permisos y un número diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c60ae-127">Returns an value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c60ae-128">**Success**</span><span class="sxs-lookup"><span data-stu-id="c60ae-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-129">0</span><span class="sxs-lookup"><span data-stu-id="c60ae-129">0</span></span>

<span data-ttu-id="c60ae-130">La solicitud es correcta.</span><span class="sxs-lookup"><span data-stu-id="c60ae-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-131">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="c60ae-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-132">2</span><span class="sxs-lookup"><span data-stu-id="c60ae-132">2</span></span>

<span data-ttu-id="c60ae-133">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="c60ae-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-134">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="c60ae-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-135">8</span><span class="sxs-lookup"><span data-stu-id="c60ae-135">8</span></span>

<span data-ttu-id="c60ae-136">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="c60ae-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-137">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="c60ae-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-138">9</span><span class="sxs-lookup"><span data-stu-id="c60ae-138">9</span></span>

<span data-ttu-id="c60ae-139">El nombre especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="c60ae-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-140">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="c60ae-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-141">10</span><span class="sxs-lookup"><span data-stu-id="c60ae-141">10</span></span>

<span data-ttu-id="c60ae-142">El objeto especificado ya existe</span><span class="sxs-lookup"><span data-stu-id="c60ae-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-143">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="c60ae-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-144">11</span><span class="sxs-lookup"><span data-stu-id="c60ae-144">11</span></span>

<span data-ttu-id="c60ae-145">El sistema de archivos no es un sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="c60ae-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-146">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="c60ae-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-147">12</span><span class="sxs-lookup"><span data-stu-id="c60ae-147">12</span></span>

<span data-ttu-id="c60ae-148">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="c60ae-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-149">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="c60ae-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-150">13</span><span class="sxs-lookup"><span data-stu-id="c60ae-150">13</span></span>

<span data-ttu-id="c60ae-151">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="c60ae-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-152">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="c60ae-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-153">14</span><span class="sxs-lookup"><span data-stu-id="c60ae-153">14</span></span>

<span data-ttu-id="c60ae-154">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="c60ae-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-155">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="c60ae-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-156">15</span><span class="sxs-lookup"><span data-stu-id="c60ae-156">15</span></span>

<span data-ttu-id="c60ae-157">Hay una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="c60ae-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-158">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="c60ae-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-159">16</span><span class="sxs-lookup"><span data-stu-id="c60ae-159">16</span></span>

<span data-ttu-id="c60ae-160">El archivo de inicio especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="c60ae-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-161">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="c60ae-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-162">17</span><span class="sxs-lookup"><span data-stu-id="c60ae-162">17</span></span>

<span data-ttu-id="c60ae-163">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="c60ae-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="c60ae-164">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="c60ae-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c60ae-165">21</span><span class="sxs-lookup"><span data-stu-id="c60ae-165">21</span></span>

<span data-ttu-id="c60ae-166">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="c60ae-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c60ae-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c60ae-167">Requirements</span></span>



| <span data-ttu-id="c60ae-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="c60ae-168">Requirement</span></span> | <span data-ttu-id="c60ae-169">Value</span><span class="sxs-lookup"><span data-stu-id="c60ae-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c60ae-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c60ae-170">Minimum supported client</span></span><br/> | <span data-ttu-id="c60ae-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c60ae-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c60ae-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c60ae-172">Minimum supported server</span></span><br/> | <span data-ttu-id="c60ae-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c60ae-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c60ae-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c60ae-174">Namespace</span></span><br/>                | <span data-ttu-id="c60ae-175">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c60ae-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c60ae-176">MOF</span><span class="sxs-lookup"><span data-stu-id="c60ae-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c60ae-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c60ae-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c60ae-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c60ae-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c60ae-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c60ae-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c60ae-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="c60ae-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="c60ae-181">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c60ae-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c60ae-182">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="c60ae-182">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

