---
description: Cambia los permisos de seguridad para el archivo de paginación lógico especificado en la ruta de acceso del objeto.
ms.assetid: 3abdfa1d-49d8-4676-b7a5-3be528938ec4
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions de la clase Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc30d8780f7c0573b9a63ff83f16ad46b9d2a70f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000654"
---
# <a name="changesecuritypermissions-method-of-the-win32_pagefile-class"></a><span data-ttu-id="3ae71-103">Método ChangeSecurityPermissions de la clase de archivo de \_ paginación Win32</span><span class="sxs-lookup"><span data-stu-id="3ae71-103">ChangeSecurityPermissions method of the Win32\_PageFile class</span></span>

<span data-ttu-id="3ae71-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** cambia los permisos de seguridad para el archivo de paginación lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ae71-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file specified in the object path.</span></span> <span data-ttu-id="3ae71-105">Si el archivo lógico es un directorio, **ChangeSecurityPermissions** es recursivo y cambia los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="3ae71-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="3ae71-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3ae71-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3ae71-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3ae71-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae71-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ae71-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="3ae71-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ae71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ae71-110">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ae71-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-111">Expresión que se resuelve como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="3ae71-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="3ae71-112">Este descriptor contiene nuevos permisos de seguridad para la instancia de archivo de [**\_ paginación de Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="3ae71-112">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-113">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3ae71-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-114">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="3ae71-114">Security privilege to be modified.</span></span> <span data-ttu-id="3ae71-115">Por ejemplo, para cambiar la seguridad de la lista de control de acceso discrecional (DACL) y el propietario, use:</span><span class="sxs-lookup"><span data-stu-id="3ae71-115">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="3ae71-116">O bien</span><span class="sxs-lookup"><span data-stu-id="3ae71-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="3ae71-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae71-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3ae71-118">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3ae71-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="3ae71-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="3ae71-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3ae71-120">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3ae71-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="3ae71-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="3ae71-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3ae71-122">Cambie la DACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3ae71-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="3ae71-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="3ae71-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3ae71-124">Cambie la lista de control de acceso de sistema (SACL) del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3ae71-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ae71-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ae71-125">Return value</span></span>

<span data-ttu-id="3ae71-126">Devuelve un valor de 0 (cero) si se cambian los permisos y un número diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="3ae71-126">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3ae71-127">**Success**</span><span class="sxs-lookup"><span data-stu-id="3ae71-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-128">0</span><span class="sxs-lookup"><span data-stu-id="3ae71-128">0</span></span>

<span data-ttu-id="3ae71-129">La solicitud es correcta.</span><span class="sxs-lookup"><span data-stu-id="3ae71-129">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-130">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="3ae71-130">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-131">2</span><span class="sxs-lookup"><span data-stu-id="3ae71-131">2</span></span>

<span data-ttu-id="3ae71-132">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="3ae71-132">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-133">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="3ae71-133">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-134">8</span><span class="sxs-lookup"><span data-stu-id="3ae71-134">8</span></span>

<span data-ttu-id="3ae71-135">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="3ae71-135">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-136">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="3ae71-136">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-137">9</span><span class="sxs-lookup"><span data-stu-id="3ae71-137">9</span></span>

<span data-ttu-id="3ae71-138">El nombre especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ae71-138">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-139">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="3ae71-139">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-140">10</span><span class="sxs-lookup"><span data-stu-id="3ae71-140">10</span></span>

<span data-ttu-id="3ae71-141">El objeto especificado ya existe</span><span class="sxs-lookup"><span data-stu-id="3ae71-141">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-142">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="3ae71-142">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-143">11</span><span class="sxs-lookup"><span data-stu-id="3ae71-143">11</span></span>

<span data-ttu-id="3ae71-144">El sistema de archivos no es un sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="3ae71-144">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-145">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="3ae71-145">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-146">12</span><span class="sxs-lookup"><span data-stu-id="3ae71-146">12</span></span>

<span data-ttu-id="3ae71-147">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="3ae71-147">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-148">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="3ae71-148">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-149">13</span><span class="sxs-lookup"><span data-stu-id="3ae71-149">13</span></span>

<span data-ttu-id="3ae71-150">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="3ae71-150">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-151">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="3ae71-151">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-152">14</span><span class="sxs-lookup"><span data-stu-id="3ae71-152">14</span></span>

<span data-ttu-id="3ae71-153">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="3ae71-153">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-154">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="3ae71-154">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-155">15</span><span class="sxs-lookup"><span data-stu-id="3ae71-155">15</span></span>

<span data-ttu-id="3ae71-156">Hay una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="3ae71-156">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-157">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="3ae71-157">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-158">16</span><span class="sxs-lookup"><span data-stu-id="3ae71-158">16</span></span>

<span data-ttu-id="3ae71-159">El archivo de inicio especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ae71-159">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-160">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="3ae71-160">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-161">17</span><span class="sxs-lookup"><span data-stu-id="3ae71-161">17</span></span>

<span data-ttu-id="3ae71-162">Falta un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="3ae71-162">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="3ae71-163">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="3ae71-163">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3ae71-164">21</span><span class="sxs-lookup"><span data-stu-id="3ae71-164">21</span></span>

<span data-ttu-id="3ae71-165">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="3ae71-165">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ae71-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ae71-166">Requirements</span></span>



| <span data-ttu-id="3ae71-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ae71-167">Requirement</span></span> | <span data-ttu-id="3ae71-168">Value</span><span class="sxs-lookup"><span data-stu-id="3ae71-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae71-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ae71-169">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae71-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ae71-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ae71-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ae71-171">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae71-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ae71-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ae71-173">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3ae71-173">Namespace</span></span><br/>                | <span data-ttu-id="3ae71-174">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3ae71-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ae71-175">MOF</span><span class="sxs-lookup"><span data-stu-id="3ae71-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ae71-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ae71-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ae71-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ae71-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ae71-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ae71-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ae71-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ae71-179">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ae71-180">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3ae71-180">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3ae71-181">**Archivo de \_ paginación Win32**</span><span class="sxs-lookup"><span data-stu-id="3ae71-181">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

