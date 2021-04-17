---
description: Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.
ms.assetid: a3caa717-ad37-4e4f-9f4e-f37aed382fa4
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions de la clase CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 929e05047af203d8e2344afa8175228e3bd969fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659661"
---
# <a name="changesecuritypermissions-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="4b320-103">Método ChangeSecurityPermissions de la \_ clase LogicalFile de CIM</span><span class="sxs-lookup"><span data-stu-id="4b320-103">ChangeSecurityPermissions method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="4b320-104">El método **ChangeSecurityPermissions** cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="4b320-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="4b320-105">Si el archivo lógico es un directorio, **ChangeSecurityPermissions** actuará de forma recursiva, lo que cambiará los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="4b320-105">If the logical file is a directory, then **ChangeSecurityPermissions** will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b320-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="4b320-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4b320-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4b320-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4b320-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4b320-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4b320-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4b320-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b320-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b320-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="4b320-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b320-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b320-112">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b320-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b320-113">Especifica la información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4b320-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="4b320-114">Una lista de control de acceso (ACL) **nula** en el [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="4b320-114">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="4b320-115">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4b320-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b320-116">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="4b320-116">Security privilege to modify.</span></span> <span data-ttu-id="4b320-117">Por ejemplo, para cambiar la seguridad de la DACL y el propietario, use:</span><span class="sxs-lookup"><span data-stu-id="4b320-117">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="4b320-118">or</span><span class="sxs-lookup"><span data-stu-id="4b320-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="4b320-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="4b320-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4b320-120">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4b320-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="4b320-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="4b320-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4b320-122">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4b320-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="4b320-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="4b320-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4b320-124">Cambie la ACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4b320-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="4b320-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="4b320-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4b320-126">Cambie la ACL del sistema del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4b320-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b320-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b320-127">Return value</span></span>

<span data-ttu-id="4b320-128">Devuelve un valor de 0 si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="4b320-128">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4b320-129">**Success**</span><span class="sxs-lookup"><span data-stu-id="4b320-129">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-130">0</span><span class="sxs-lookup"><span data-stu-id="4b320-130">0</span></span>

<span data-ttu-id="4b320-131">Correcto.</span><span class="sxs-lookup"><span data-stu-id="4b320-131">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-132">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="4b320-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-133">2</span><span class="sxs-lookup"><span data-stu-id="4b320-133">2</span></span>

<span data-ttu-id="4b320-134">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="4b320-134">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-135">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="4b320-135">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-136">8</span><span class="sxs-lookup"><span data-stu-id="4b320-136">8</span></span>

<span data-ttu-id="4b320-137">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="4b320-137">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-138">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="4b320-138">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-139">9</span><span class="sxs-lookup"><span data-stu-id="4b320-139">9</span></span>

<span data-ttu-id="4b320-140">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="4b320-140">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-141">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="4b320-141">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-142">10</span><span class="sxs-lookup"><span data-stu-id="4b320-142">10</span></span>

<span data-ttu-id="4b320-143">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="4b320-143">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-144">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="4b320-144">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-145">11</span><span class="sxs-lookup"><span data-stu-id="4b320-145">11</span></span>

<span data-ttu-id="4b320-146">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="4b320-146">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-147">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="4b320-147">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-148">12</span><span class="sxs-lookup"><span data-stu-id="4b320-148">12</span></span>

<span data-ttu-id="4b320-149">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="4b320-149">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-150">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="4b320-150">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-151">13</span><span class="sxs-lookup"><span data-stu-id="4b320-151">13</span></span>

<span data-ttu-id="4b320-152">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="4b320-152">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-153">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="4b320-153">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-154">14</span><span class="sxs-lookup"><span data-stu-id="4b320-154">14</span></span>

<span data-ttu-id="4b320-155">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="4b320-155">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-156">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="4b320-156">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-157">15</span><span class="sxs-lookup"><span data-stu-id="4b320-157">15</span></span>

<span data-ttu-id="4b320-158">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="4b320-158">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-159">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="4b320-159">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-160">16</span><span class="sxs-lookup"><span data-stu-id="4b320-160">16</span></span>

<span data-ttu-id="4b320-161">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="4b320-161">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-162">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="4b320-162">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-163">17</span><span class="sxs-lookup"><span data-stu-id="4b320-163">17</span></span>

<span data-ttu-id="4b320-164">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="4b320-164">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="4b320-165">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="4b320-165">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4b320-166">21</span><span class="sxs-lookup"><span data-stu-id="4b320-166">21</span></span>

<span data-ttu-id="4b320-167">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="4b320-167">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b320-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b320-168">Remarks</span></span>

<span data-ttu-id="4b320-169">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="4b320-169">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4b320-170">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="4b320-170">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4b320-171">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="4b320-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4b320-172">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="4b320-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b320-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b320-173">Requirements</span></span>



| <span data-ttu-id="4b320-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b320-174">Requirement</span></span> | <span data-ttu-id="4b320-175">Value</span><span class="sxs-lookup"><span data-stu-id="4b320-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b320-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b320-176">Minimum supported client</span></span><br/> | <span data-ttu-id="4b320-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b320-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b320-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b320-178">Minimum supported server</span></span><br/> | <span data-ttu-id="4b320-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b320-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b320-180">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4b320-180">Namespace</span></span><br/>                | <span data-ttu-id="4b320-181">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4b320-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4b320-182">MOF</span><span class="sxs-lookup"><span data-stu-id="4b320-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b320-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b320-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b320-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b320-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b320-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b320-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b320-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b320-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b320-187">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="4b320-187">**CIM\_LogicalFile**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="4b320-188">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="4b320-188">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

