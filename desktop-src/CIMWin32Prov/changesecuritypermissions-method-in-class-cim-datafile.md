---
description: Cambia los permisos de seguridad para el archivo de datos lógico especificado en la ruta de acceso del objeto.
ms.assetid: b0a66411-f973-42ce-a3fe-25c31234a964
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions de la clase CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faa2e3ce2f2454d76ff9e55cc10cf09e9b5f715e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153248"
---
# <a name="changesecuritypermissions-method-of-the-cim_datafile-class"></a><span data-ttu-id="98f5c-103">Método ChangeSecurityPermissions de la \_ clase de archivo de archivos CIM</span><span class="sxs-lookup"><span data-stu-id="98f5c-103">ChangeSecurityPermissions method of the CIM\_DataFile class</span></span>

<span data-ttu-id="98f5c-104">El método **ChangeSecurityPermissions** cambia los permisos de seguridad para el archivo de datos lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="98f5c-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical data file specified in the object path.</span></span> <span data-ttu-id="98f5c-105">Si el archivo lógico es un directorio, este método actuará de forma recursiva y cambiará los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="98f5c-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="98f5c-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="98f5c-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98f5c-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="98f5c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="98f5c-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="98f5c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="98f5c-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="98f5c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="98f5c-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="98f5c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="98f5c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98f5c-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="98f5c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98f5c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98f5c-113">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98f5c-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-114">Especifica la información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="98f5c-114">Specifies the security information.</span></span>

> [!Note]  
> <span data-ttu-id="98f5c-115">Una lista de control de acceso (ACL) **nula** en la estructura del [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="98f5c-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="98f5c-116">Para obtener información sobre las implicaciones de acceso ilimitado, consulte [crear un descriptor de seguridad para un nuevo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="98f5c-116">For information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="98f5c-117">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="98f5c-117">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-118">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="98f5c-118">Security privilege to modify.</span></span> <span data-ttu-id="98f5c-119">Por ejemplo, para cambiar la seguridad de la DACL y el propietario, use:</span><span class="sxs-lookup"><span data-stu-id="98f5c-119">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="98f5c-120">or</span><span class="sxs-lookup"><span data-stu-id="98f5c-120">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="98f5c-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="98f5c-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="98f5c-122">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="98f5c-122">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="98f5c-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="98f5c-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="98f5c-124">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="98f5c-124">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="98f5c-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="98f5c-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="98f5c-126">Cambie la ACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="98f5c-126">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="98f5c-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="98f5c-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="98f5c-128">Cambie la ACL del sistema del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="98f5c-128">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98f5c-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98f5c-129">Return value</span></span>

<span data-ttu-id="98f5c-130">Devuelve un valor de 0 si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="98f5c-130">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="98f5c-131">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="98f5c-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="98f5c-132">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="98f5c-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="98f5c-133">**Success**</span><span class="sxs-lookup"><span data-stu-id="98f5c-133">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-134">0</span><span class="sxs-lookup"><span data-stu-id="98f5c-134">0</span></span>

<span data-ttu-id="98f5c-135">Correcto.</span><span class="sxs-lookup"><span data-stu-id="98f5c-135">Success.</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-136">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="98f5c-136">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-137">2</span><span class="sxs-lookup"><span data-stu-id="98f5c-137">2</span></span>

<span data-ttu-id="98f5c-138">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="98f5c-138">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-139">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="98f5c-139">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-140">8</span><span class="sxs-lookup"><span data-stu-id="98f5c-140">8</span></span>

<span data-ttu-id="98f5c-141">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="98f5c-141">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-142">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="98f5c-142">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-143">9</span><span class="sxs-lookup"><span data-stu-id="98f5c-143">9</span></span>

<span data-ttu-id="98f5c-144">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="98f5c-144">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-145">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="98f5c-145">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-146">10</span><span class="sxs-lookup"><span data-stu-id="98f5c-146">10</span></span>

<span data-ttu-id="98f5c-147">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="98f5c-147">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-148">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="98f5c-148">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-149">11</span><span class="sxs-lookup"><span data-stu-id="98f5c-149">11</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-150">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="98f5c-150">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-151">12</span><span class="sxs-lookup"><span data-stu-id="98f5c-151">12</span></span>

<span data-ttu-id="98f5c-152">Plataforma no basada en Windows NT.</span><span class="sxs-lookup"><span data-stu-id="98f5c-152">Platform not Windows NT-based.</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-153">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="98f5c-153">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-154">13</span><span class="sxs-lookup"><span data-stu-id="98f5c-154">13</span></span>

<span data-ttu-id="98f5c-155">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="98f5c-155">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-156">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="98f5c-156">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-157">14</span><span class="sxs-lookup"><span data-stu-id="98f5c-157">14</span></span>

<span data-ttu-id="98f5c-158">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="98f5c-158">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-159">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="98f5c-159">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-160">15</span><span class="sxs-lookup"><span data-stu-id="98f5c-160">15</span></span>

<span data-ttu-id="98f5c-161">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="98f5c-161">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-162">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="98f5c-162">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-163">16</span><span class="sxs-lookup"><span data-stu-id="98f5c-163">16</span></span>

<span data-ttu-id="98f5c-164">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="98f5c-164">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-165">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="98f5c-165">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-166">17</span><span class="sxs-lookup"><span data-stu-id="98f5c-166">17</span></span>

<span data-ttu-id="98f5c-167">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="98f5c-167">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="98f5c-168">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="98f5c-168">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="98f5c-169">21</span><span class="sxs-lookup"><span data-stu-id="98f5c-169">21</span></span>

<span data-ttu-id="98f5c-170">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="98f5c-170">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98f5c-171">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98f5c-171">Remarks</span></span>

<span data-ttu-id="98f5c-172">WMI implementa el método **ChangeSecurityPermissions** en el [**archivo de \_ archivos de CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="98f5c-172">The **ChangeSecurityPermissions** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="98f5c-173">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="98f5c-173">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="98f5c-174">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="98f5c-174">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="98f5c-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98f5c-175">Requirements</span></span>



| <span data-ttu-id="98f5c-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="98f5c-176">Requirement</span></span> | <span data-ttu-id="98f5c-177">Value</span><span class="sxs-lookup"><span data-stu-id="98f5c-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98f5c-178">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98f5c-178">Minimum supported client</span></span><br/> | <span data-ttu-id="98f5c-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98f5c-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98f5c-180">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98f5c-180">Minimum supported server</span></span><br/> | <span data-ttu-id="98f5c-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98f5c-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98f5c-182">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="98f5c-182">Namespace</span></span><br/>                | <span data-ttu-id="98f5c-183">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="98f5c-183">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="98f5c-184">MOF</span><span class="sxs-lookup"><span data-stu-id="98f5c-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98f5c-185"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98f5c-185"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="98f5c-186">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98f5c-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98f5c-187"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98f5c-187"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98f5c-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="98f5c-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f5c-189">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="98f5c-189">**CIM\_DataFile**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="98f5c-190">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="98f5c-190">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="98f5c-191">Tareas de WMI: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="98f5c-191">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="98f5c-192">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="98f5c-192">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

