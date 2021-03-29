---
description: Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método ChangeSecurityPermissions).
ms.assetid: 29155533-0898-4f8f-af08-f3ea46c8c1d3
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx de la clase CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af2dc82ef54b6f32eee20f17cd61c0769cc64b1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538787"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="fe6d5-103">Método ChangeSecurityPermissionsEx de la \_ clase LogicalFile de CIM</span><span class="sxs-lookup"><span data-stu-id="fe6d5-103">ChangeSecurityPermissionsEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="fe6d5-104">El método **ChangeSecurityPermissionsEx** cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) ).</span><span class="sxs-lookup"><span data-stu-id="fe6d5-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) method).</span></span> <span data-ttu-id="fe6d5-105">Si el archivo lógico es un directorio, este método actuará de forma recursiva y cambiará los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe6d5-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fe6d5-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fe6d5-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fe6d5-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="fe6d5-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fe6d5-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fe6d5-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe6d5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe6d5-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="fe6d5-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe6d5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe6d5-112">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe6d5-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-113">Especifica la información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-113">Specifies the security information.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-114">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fe6d5-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-115">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-115">Security privilege to modify.</span></span> <span data-ttu-id="fe6d5-116">Por ejemplo, para cambiar la seguridad de la DACL y el propietario, use</span><span class="sxs-lookup"><span data-stu-id="fe6d5-116">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="fe6d5-117">or</span><span class="sxs-lookup"><span data-stu-id="fe6d5-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="fe6d5-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="fe6d5-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fe6d5-119">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="fe6d5-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="fe6d5-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fe6d5-121">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="fe6d5-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="fe6d5-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fe6d5-123">Cambie la ACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-123">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="fe6d5-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="fe6d5-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="fe6d5-125">Cambie la ACL del sistema del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-125">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fe6d5-126">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fe6d5-126">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-127">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-127">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="fe6d5-128">Este parámetro tiene un valor **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-128">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-129">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="fe6d5-129">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-130">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-130">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="fe6d5-131">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo (o directorio) en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-131">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="fe6d5-132">Si el valor del parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="fe6d5-132">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-133">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="fe6d5-133">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-134">Si **es true**, los permisos de seguridad se aplican de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="fe6d5-134">If **TRUE**, the security permissions are applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="fe6d5-135">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-135">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe6d5-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe6d5-136">Return value</span></span>

<span data-ttu-id="fe6d5-137">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-137">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="fe6d5-138">**Success**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-138">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-139">0</span><span class="sxs-lookup"><span data-stu-id="fe6d5-139">0</span></span>

<span data-ttu-id="fe6d5-140">Correcto.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-140">Success.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-141">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-141">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-142">2</span><span class="sxs-lookup"><span data-stu-id="fe6d5-142">2</span></span>

<span data-ttu-id="fe6d5-143">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-143">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-144">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-144">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-145">8</span><span class="sxs-lookup"><span data-stu-id="fe6d5-145">8</span></span>

<span data-ttu-id="fe6d5-146">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-146">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-147">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-147">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-148">9</span><span class="sxs-lookup"><span data-stu-id="fe6d5-148">9</span></span>

<span data-ttu-id="fe6d5-149">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-149">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-150">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-150">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-151">10</span><span class="sxs-lookup"><span data-stu-id="fe6d5-151">10</span></span>

<span data-ttu-id="fe6d5-152">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-152">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-153">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-153">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-154">11</span><span class="sxs-lookup"><span data-stu-id="fe6d5-154">11</span></span>

<span data-ttu-id="fe6d5-155">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-155">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-156">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-156">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-157">12</span><span class="sxs-lookup"><span data-stu-id="fe6d5-157">12</span></span>

<span data-ttu-id="fe6d5-158">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-158">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-159">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-159">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-160">13</span><span class="sxs-lookup"><span data-stu-id="fe6d5-160">13</span></span>

<span data-ttu-id="fe6d5-161">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-161">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-162">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-162">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-163">14</span><span class="sxs-lookup"><span data-stu-id="fe6d5-163">14</span></span>

<span data-ttu-id="fe6d5-164">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-164">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-165">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-165">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-166">15</span><span class="sxs-lookup"><span data-stu-id="fe6d5-166">15</span></span>

<span data-ttu-id="fe6d5-167">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-167">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-168">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-168">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-169">16</span><span class="sxs-lookup"><span data-stu-id="fe6d5-169">16</span></span>

<span data-ttu-id="fe6d5-170">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-170">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-171">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-171">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-172">17</span><span class="sxs-lookup"><span data-stu-id="fe6d5-172">17</span></span>

<span data-ttu-id="fe6d5-173">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-173">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="fe6d5-174">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-174">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fe6d5-175">21</span><span class="sxs-lookup"><span data-stu-id="fe6d5-175">21</span></span>

<span data-ttu-id="fe6d5-176">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-176">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe6d5-177">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe6d5-177">Remarks</span></span>

<span data-ttu-id="fe6d5-178">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-178">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fe6d5-179">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="fe6d5-179">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe6d5-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe6d5-180">Requirements</span></span>



| <span data-ttu-id="fe6d5-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe6d5-181">Requirement</span></span> | <span data-ttu-id="fe6d5-182">Value</span><span class="sxs-lookup"><span data-stu-id="fe6d5-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6d5-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe6d5-183">Minimum supported client</span></span><br/> | <span data-ttu-id="fe6d5-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe6d5-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe6d5-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe6d5-185">Minimum supported server</span></span><br/> | <span data-ttu-id="fe6d5-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe6d5-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe6d5-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fe6d5-187">Namespace</span></span><br/>                | <span data-ttu-id="fe6d5-188">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fe6d5-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fe6d5-189">MOF</span><span class="sxs-lookup"><span data-stu-id="fe6d5-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe6d5-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe6d5-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe6d5-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fe6d5-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe6d5-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe6d5-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe6d5-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe6d5-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6d5-194">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-194">**CIM\_LogicalFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="fe6d5-195">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="fe6d5-195">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

