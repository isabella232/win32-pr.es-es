---
description: Cambia los permisos de seguridad para el archivo de dispositivo lógico especificado en la ruta de acceso del objeto.
ms.assetid: 4b3e1a0e-3c9e-45bb-8c7b-cbbc8f9d1265
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions de la clase CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a772c17695a537e4a9a8518bf05b052c0417f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496421"
---
# <a name="changesecuritypermissions-method-of-the-cim_devicefile-class"></a><span data-ttu-id="57002-103">Método ChangeSecurityPermissions de la \_ clase DeviceFile de CIM</span><span class="sxs-lookup"><span data-stu-id="57002-103">ChangeSecurityPermissions method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="57002-104">El método **ChangeSecurityPermissions** cambia los permisos de seguridad para el archivo de dispositivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="57002-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical device file specified in the object path.</span></span> <span data-ttu-id="57002-105">Si el archivo lógico es un directorio, este método actuará de forma recursiva y cambiará los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="57002-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="57002-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="57002-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57002-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="57002-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="57002-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="57002-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="57002-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="57002-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="57002-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="57002-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="57002-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57002-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="57002-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57002-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57002-113">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57002-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57002-114">Especifica la información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="57002-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="57002-115">Una lista de control de acceso (ACL) **nula** en la estructura del [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="57002-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="57002-116">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="57002-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57002-117">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="57002-117">Security privilege to modify.</span></span> <span data-ttu-id="57002-118">Por ejemplo, para cambiar la seguridad de la DACL y el propietario, use:</span><span class="sxs-lookup"><span data-stu-id="57002-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="57002-119">or</span><span class="sxs-lookup"><span data-stu-id="57002-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="57002-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="57002-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="57002-121">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="57002-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="57002-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="57002-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="57002-123">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="57002-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="57002-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="57002-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="57002-125">Cambie la ACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="57002-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="57002-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="57002-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="57002-127">Cambie la ACL del sistema del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="57002-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57002-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57002-128">Return value</span></span>

<span data-ttu-id="57002-129">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="57002-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="57002-130">**Success**</span><span class="sxs-lookup"><span data-stu-id="57002-130">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="57002-131">0</span><span class="sxs-lookup"><span data-stu-id="57002-131">0</span></span>

<span data-ttu-id="57002-132">Correcto.</span><span class="sxs-lookup"><span data-stu-id="57002-132">Success.</span></span>

</dd> <dt>

<span data-ttu-id="57002-133">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="57002-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="57002-134">2</span><span class="sxs-lookup"><span data-stu-id="57002-134">2</span></span>

<span data-ttu-id="57002-135">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="57002-135">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="57002-136">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="57002-136">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="57002-137">8</span><span class="sxs-lookup"><span data-stu-id="57002-137">8</span></span>

<span data-ttu-id="57002-138">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="57002-138">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="57002-139">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="57002-139">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="57002-140">9</span><span class="sxs-lookup"><span data-stu-id="57002-140">9</span></span>

<span data-ttu-id="57002-141">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="57002-141">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="57002-142">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="57002-142">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="57002-143">10</span><span class="sxs-lookup"><span data-stu-id="57002-143">10</span></span>

<span data-ttu-id="57002-144">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="57002-144">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="57002-145">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="57002-145">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="57002-146">11</span><span class="sxs-lookup"><span data-stu-id="57002-146">11</span></span>

<span data-ttu-id="57002-147">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="57002-147">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="57002-148">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="57002-148">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="57002-149">12</span><span class="sxs-lookup"><span data-stu-id="57002-149">12</span></span>

<span data-ttu-id="57002-150">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="57002-150">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="57002-151">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="57002-151">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="57002-152">13</span><span class="sxs-lookup"><span data-stu-id="57002-152">13</span></span>

<span data-ttu-id="57002-153">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="57002-153">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="57002-154">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="57002-154">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="57002-155">14</span><span class="sxs-lookup"><span data-stu-id="57002-155">14</span></span>

<span data-ttu-id="57002-156">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="57002-156">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="57002-157">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="57002-157">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="57002-158">15</span><span class="sxs-lookup"><span data-stu-id="57002-158">15</span></span>

<span data-ttu-id="57002-159">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="57002-159">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="57002-160">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="57002-160">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="57002-161">16</span><span class="sxs-lookup"><span data-stu-id="57002-161">16</span></span>

<span data-ttu-id="57002-162">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="57002-162">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="57002-163">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="57002-163">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="57002-164">17</span><span class="sxs-lookup"><span data-stu-id="57002-164">17</span></span>

<span data-ttu-id="57002-165">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="57002-165">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="57002-166">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="57002-166">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="57002-167">21</span><span class="sxs-lookup"><span data-stu-id="57002-167">21</span></span>

<span data-ttu-id="57002-168">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="57002-168">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57002-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57002-169">Remarks</span></span>

<span data-ttu-id="57002-170">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="57002-170">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="57002-171">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="57002-171">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="57002-172">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="57002-172">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="57002-173">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="57002-173">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="57002-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57002-174">Requirements</span></span>



| <span data-ttu-id="57002-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="57002-175">Requirement</span></span> | <span data-ttu-id="57002-176">Value</span><span class="sxs-lookup"><span data-stu-id="57002-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57002-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57002-177">Minimum supported client</span></span><br/> | <span data-ttu-id="57002-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57002-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="57002-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57002-179">Minimum supported server</span></span><br/> | <span data-ttu-id="57002-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57002-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="57002-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="57002-181">Namespace</span></span><br/>                | <span data-ttu-id="57002-182">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="57002-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="57002-183">MOF</span><span class="sxs-lookup"><span data-stu-id="57002-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57002-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57002-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="57002-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="57002-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57002-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57002-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57002-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="57002-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57002-188">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="57002-188">**CIM\_DeviceFile**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="57002-189">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="57002-189">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

