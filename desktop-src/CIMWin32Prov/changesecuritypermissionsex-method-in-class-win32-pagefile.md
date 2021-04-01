---
description: Cambia los permisos de seguridad del archivo de paginación lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método ChangeSecurityPermissions).
ms.assetid: a852a7e6-f26a-4bd9-bb15-e4cdd577697c
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx de la clase Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a01a214e626f9c64ccf460eb3f8c031d1b45ff85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907184"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="b17fe-103">Método ChangeSecurityPermissionsEx de la clase de archivo de \_ paginación Win32</span><span class="sxs-lookup"><span data-stu-id="b17fe-103">ChangeSecurityPermissionsEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="b17fe-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** cambia los permisos de seguridad para el archivo de paginación lógica que se especifica en la ruta de acceso del objeto (este método es una versión extendida del método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="b17fe-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file that is specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="b17fe-105">Si el archivo lógico es un directorio, este método es recursivo y cambia los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="b17fe-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="b17fe-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b17fe-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b17fe-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b17fe-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b17fe-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b17fe-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="b17fe-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b17fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b17fe-110">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b17fe-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-111">Expresión que se resuelve como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="b17fe-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="b17fe-112">Este parámetro contiene nuevos permisos de seguridad para la instancia de archivo de [**\_ paginación de Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="b17fe-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-113">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b17fe-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-114">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="b17fe-114">Security privilege to be modified.</span></span> <span data-ttu-id="b17fe-115">Por ejemplo, para cambiar el propietario y la seguridad de la lista de control de acceso discrecional (DACL), use lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b17fe-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="b17fe-116">O bien</span><span class="sxs-lookup"><span data-stu-id="b17fe-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="b17fe-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="b17fe-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b17fe-118">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b17fe-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="b17fe-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="b17fe-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b17fe-120">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b17fe-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="b17fe-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="b17fe-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b17fe-122">Cambie la DACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b17fe-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="b17fe-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="b17fe-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b17fe-124">Cambie la lista de control de acceso del sistema (SACL) del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b17fe-124">Change the system access control (SACL) list of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b17fe-125">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b17fe-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-126">Nombre del archivo o directorio en el que se produjo un error en el método **ChangeSecurityPermissionsEx** .</span><span class="sxs-lookup"><span data-stu-id="b17fe-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="b17fe-127">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="b17fe-127">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-128">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b17fe-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-129">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **ChangeSecurityPermissionsEx**.</span><span class="sxs-lookup"><span data-stu-id="b17fe-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="b17fe-130">Normalmente, el parámetro *StartFileName* es el parámetro *StartFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="b17fe-130">Typically, the *StartFileName* parameter is the *StartFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="b17fe-131">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="b17fe-131">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-132">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b17fe-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-133">Si es **true**, el cambio de propiedad se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="b17fe-133">If **true**, the change of ownership is applied recursively to files and directories in the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="b17fe-134">En el caso de las instancias de archivo, se omite el parámetro *Recursive* .</span><span class="sxs-lookup"><span data-stu-id="b17fe-134">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b17fe-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b17fe-135">Return value</span></span>

<span data-ttu-id="b17fe-136">Devuelve un valor de 0 (cero) si se cambian los permisos y un número diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="b17fe-136">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="b17fe-137">**Success**</span><span class="sxs-lookup"><span data-stu-id="b17fe-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-138">0</span><span class="sxs-lookup"><span data-stu-id="b17fe-138">0</span></span>

<span data-ttu-id="b17fe-139">La solicitud es correcta.</span><span class="sxs-lookup"><span data-stu-id="b17fe-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-140">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="b17fe-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-141">2</span><span class="sxs-lookup"><span data-stu-id="b17fe-141">2</span></span>

<span data-ttu-id="b17fe-142">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="b17fe-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-143">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="b17fe-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-144">8</span><span class="sxs-lookup"><span data-stu-id="b17fe-144">8</span></span>

<span data-ttu-id="b17fe-145">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="b17fe-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-146">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="b17fe-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-147">9</span><span class="sxs-lookup"><span data-stu-id="b17fe-147">9</span></span>

<span data-ttu-id="b17fe-148">El nombre especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b17fe-148">The name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-149">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="b17fe-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-150">10</span><span class="sxs-lookup"><span data-stu-id="b17fe-150">10</span></span>

<span data-ttu-id="b17fe-151">El objeto especificado ya existe</span><span class="sxs-lookup"><span data-stu-id="b17fe-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-152">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="b17fe-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-153">11</span><span class="sxs-lookup"><span data-stu-id="b17fe-153">11</span></span>

<span data-ttu-id="b17fe-154">El sistema de archivos no es un sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="b17fe-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-155">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="b17fe-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-156">12</span><span class="sxs-lookup"><span data-stu-id="b17fe-156">12</span></span>

<span data-ttu-id="b17fe-157">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="b17fe-157">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-158">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="b17fe-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-159">13</span><span class="sxs-lookup"><span data-stu-id="b17fe-159">13</span></span>

<span data-ttu-id="b17fe-160">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="b17fe-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-161">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="b17fe-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-162">14</span><span class="sxs-lookup"><span data-stu-id="b17fe-162">14</span></span>

<span data-ttu-id="b17fe-163">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="b17fe-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-164">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="b17fe-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-165">15</span><span class="sxs-lookup"><span data-stu-id="b17fe-165">15</span></span>

<span data-ttu-id="b17fe-166">Hay una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="b17fe-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-167">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="b17fe-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-168">16</span><span class="sxs-lookup"><span data-stu-id="b17fe-168">16</span></span>

<span data-ttu-id="b17fe-169">El archivo de inicio especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b17fe-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-170">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="b17fe-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-171">17</span><span class="sxs-lookup"><span data-stu-id="b17fe-171">17</span></span>

<span data-ttu-id="b17fe-172">Falta un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="b17fe-172">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="b17fe-173">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="b17fe-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b17fe-174">21</span><span class="sxs-lookup"><span data-stu-id="b17fe-174">21</span></span>

<span data-ttu-id="b17fe-175">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b17fe-175">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b17fe-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b17fe-176">Requirements</span></span>



| <span data-ttu-id="b17fe-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="b17fe-177">Requirement</span></span> | <span data-ttu-id="b17fe-178">Value</span><span class="sxs-lookup"><span data-stu-id="b17fe-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b17fe-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b17fe-179">Minimum supported client</span></span><br/> | <span data-ttu-id="b17fe-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b17fe-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b17fe-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b17fe-181">Minimum supported server</span></span><br/> | <span data-ttu-id="b17fe-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b17fe-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b17fe-183">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b17fe-183">Namespace</span></span><br/>                | <span data-ttu-id="b17fe-184">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b17fe-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b17fe-185">MOF</span><span class="sxs-lookup"><span data-stu-id="b17fe-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b17fe-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b17fe-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b17fe-187">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b17fe-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b17fe-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b17fe-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b17fe-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="b17fe-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="b17fe-190">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b17fe-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b17fe-191">**Archivo de \_ paginación Win32**</span><span class="sxs-lookup"><span data-stu-id="b17fe-191">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

