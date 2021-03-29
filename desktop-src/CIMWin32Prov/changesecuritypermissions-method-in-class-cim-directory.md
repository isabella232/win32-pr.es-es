---
description: Cambia los permisos de seguridad para el archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto.
ms.assetid: d3caeec1-fecc-4463-9349-d82869c11927
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions de la clase CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bf767dc45907a90354b2c00fb30c6b31ce6d09a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807621"
---
# <a name="changesecuritypermissions-method-of-the-cim_directory-class"></a><span data-ttu-id="62471-103">Método ChangeSecurityPermissions de la \_ clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="62471-103">ChangeSecurityPermissions method of the CIM\_Directory class</span></span>

<span data-ttu-id="62471-104">El método **ChangeSecurityPermissions** cambia los permisos de seguridad para el archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="62471-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="62471-105">Si el archivo lógico es un directorio, este método actuará de forma recursiva y cambiará los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="62471-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="62471-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="62471-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62471-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="62471-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="62471-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="62471-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="62471-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="62471-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="62471-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="62471-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="62471-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62471-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="62471-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62471-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62471-113">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62471-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62471-114">Especifica la información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="62471-114">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="62471-115">Una lista de control de acceso (ACL) **nula** en la estructura del [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="62471-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="62471-116">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="62471-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62471-117">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="62471-117">Security privilege to modify.</span></span> <span data-ttu-id="62471-118">Por ejemplo, para cambiar la seguridad de la DACL y el propietario, use:</span><span class="sxs-lookup"><span data-stu-id="62471-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="62471-119">or</span><span class="sxs-lookup"><span data-stu-id="62471-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="62471-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="62471-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="62471-121">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62471-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="62471-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="62471-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="62471-123">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62471-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="62471-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="62471-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="62471-125">Cambie la ACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62471-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="62471-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="62471-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="62471-127">Cambie la ACL del sistema del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62471-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62471-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62471-128">Return value</span></span>

<span data-ttu-id="62471-129">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="62471-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="62471-130">0</span><span class="sxs-lookup"><span data-stu-id="62471-130">0</span></span>

<span data-ttu-id="62471-131">Correcto.</span><span class="sxs-lookup"><span data-stu-id="62471-131">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-132">2</span><span class="sxs-lookup"><span data-stu-id="62471-132">2</span></span>

<span data-ttu-id="62471-133">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="62471-133">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-134">8</span><span class="sxs-lookup"><span data-stu-id="62471-134">8</span></span>

<span data-ttu-id="62471-135">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="62471-135">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-136">9</span><span class="sxs-lookup"><span data-stu-id="62471-136">9</span></span>

<span data-ttu-id="62471-137">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="62471-137">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-138">10</span><span class="sxs-lookup"><span data-stu-id="62471-138">10</span></span>

<span data-ttu-id="62471-139">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="62471-139">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-140">11</span><span class="sxs-lookup"><span data-stu-id="62471-140">11</span></span>

<span data-ttu-id="62471-141">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="62471-141">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-142">12</span><span class="sxs-lookup"><span data-stu-id="62471-142">12</span></span>

<span data-ttu-id="62471-143">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="62471-143">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-144">13</span><span class="sxs-lookup"><span data-stu-id="62471-144">13</span></span>

<span data-ttu-id="62471-145">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="62471-145">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-146">14</span><span class="sxs-lookup"><span data-stu-id="62471-146">14</span></span>

<span data-ttu-id="62471-147">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="62471-147">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-148">15</span><span class="sxs-lookup"><span data-stu-id="62471-148">15</span></span>

<span data-ttu-id="62471-149">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="62471-149">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-150">16</span><span class="sxs-lookup"><span data-stu-id="62471-150">16</span></span>

<span data-ttu-id="62471-151">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="62471-151">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-152">17</span><span class="sxs-lookup"><span data-stu-id="62471-152">17</span></span>

<span data-ttu-id="62471-153">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="62471-153">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="62471-154">21</span><span class="sxs-lookup"><span data-stu-id="62471-154">21</span></span>

<span data-ttu-id="62471-155">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="62471-155">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62471-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62471-156">Remarks</span></span>

<span data-ttu-id="62471-157">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="62471-157">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="62471-158">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="62471-158">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="62471-159">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="62471-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="62471-160">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="62471-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="62471-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62471-161">Requirements</span></span>



| <span data-ttu-id="62471-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="62471-162">Requirement</span></span> | <span data-ttu-id="62471-163">Value</span><span class="sxs-lookup"><span data-stu-id="62471-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62471-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62471-164">Minimum supported client</span></span><br/> | <span data-ttu-id="62471-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62471-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62471-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62471-166">Minimum supported server</span></span><br/> | <span data-ttu-id="62471-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62471-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62471-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="62471-168">Namespace</span></span><br/>                | <span data-ttu-id="62471-169">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="62471-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62471-170">MOF</span><span class="sxs-lookup"><span data-stu-id="62471-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62471-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62471-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62471-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62471-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62471-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62471-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62471-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="62471-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62471-175">\_Directorio CIM</span><span class="sxs-lookup"><span data-stu-id="62471-175">CIM\_Directory</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="62471-176">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="62471-176">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

