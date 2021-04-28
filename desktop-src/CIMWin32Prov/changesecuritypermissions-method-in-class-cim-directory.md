---
description: 'Método ChangeSecurityPermissions de la clase CIM_Directory: cambia los permisos de seguridad para el archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto.'
ms.assetid: d3caeec1-fecc-4463-9349-d82869c11927
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions de la CIM_Directory clase
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
ms.openlocfilehash: 389ed5b7b0a43981c5eeb3d66a73bd19cbd99d88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091073"
---
# <a name="changesecuritypermissions-method-of-the-cim_directory-class"></a><span data-ttu-id="1c20a-103">Método ChangeSecurityPermissions de la clase \_ de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="1c20a-103">ChangeSecurityPermissions method of the CIM\_Directory class</span></span>

<span data-ttu-id="1c20a-104">El **método ChangeSecurityPermissions** cambia los permisos de seguridad para el archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="1c20a-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="1c20a-105">Si el archivo lógico es un directorio, este método actuará de forma recursiva, cambiando los permisos de seguridad para todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="1c20a-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="1c20a-106">Este método se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="1c20a-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c20a-107">Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="1c20a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1c20a-108">WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1c20a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1c20a-109">En este tema se usa Managed Object Format sintaxis de MOF.</span><span class="sxs-lookup"><span data-stu-id="1c20a-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1c20a-110">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1c20a-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1c20a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c20a-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="1c20a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c20a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c20a-113">*SecurityDescriptor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1c20a-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c20a-114">Especifica información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1c20a-114">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="1c20a-115">Una **lista de** control de acceso (ACL) NULL en la estructura DESCRIPTOR DE [**\_ SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="1c20a-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="1c20a-116">*Opción* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1c20a-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c20a-117">Privilegio de seguridad que se debe modificar.</span><span class="sxs-lookup"><span data-stu-id="1c20a-117">Security privilege to modify.</span></span> <span data-ttu-id="1c20a-118">Por ejemplo, para cambiar el propietario y la seguridad de DACL, use:</span><span class="sxs-lookup"><span data-stu-id="1c20a-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="1c20a-119">o</span><span class="sxs-lookup"><span data-stu-id="1c20a-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="1c20a-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CAMBIO \_ INFORMACIÓN \_ DE \_ SEGURIDAD DEL** PROPIETARIO (1)</span><span class="sxs-lookup"><span data-stu-id="1c20a-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1c20a-121">Cambie el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1c20a-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="1c20a-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CAMBIO \_ INFORMACIÓN \_ DE \_ SEGURIDAD DE** GRUPO (2)</span><span class="sxs-lookup"><span data-stu-id="1c20a-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1c20a-123">Cambie el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1c20a-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="1c20a-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CAMBIO \_ INFORMACIÓN DE \_ SEGURIDAD \_ DE DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="1c20a-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1c20a-125">Cambie la ACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1c20a-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="1c20a-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CAMBIO \_ INFORMACIÓN DE \_ SEGURIDAD \_ DE SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="1c20a-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1c20a-127">Cambie la ACL del sistema del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1c20a-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c20a-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c20a-128">Return value</span></span>

<span data-ttu-id="1c20a-129">Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="1c20a-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-130">0</span><span class="sxs-lookup"><span data-stu-id="1c20a-130">0</span></span>

<span data-ttu-id="1c20a-131">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1c20a-131">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-132">2</span><span class="sxs-lookup"><span data-stu-id="1c20a-132">2</span></span>

<span data-ttu-id="1c20a-133">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="1c20a-133">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-134">8</span><span class="sxs-lookup"><span data-stu-id="1c20a-134">8</span></span>

<span data-ttu-id="1c20a-135">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="1c20a-135">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-136">9</span><span class="sxs-lookup"><span data-stu-id="1c20a-136">9</span></span>

<span data-ttu-id="1c20a-137">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="1c20a-137">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-138">10</span><span class="sxs-lookup"><span data-stu-id="1c20a-138">10</span></span>

<span data-ttu-id="1c20a-139">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="1c20a-139">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-140">11</span><span class="sxs-lookup"><span data-stu-id="1c20a-140">11</span></span>

<span data-ttu-id="1c20a-141">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="1c20a-141">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-142">12</span><span class="sxs-lookup"><span data-stu-id="1c20a-142">12</span></span>

<span data-ttu-id="1c20a-143">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="1c20a-143">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-144">13</span><span class="sxs-lookup"><span data-stu-id="1c20a-144">13</span></span>

<span data-ttu-id="1c20a-145">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="1c20a-145">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-146">14</span><span class="sxs-lookup"><span data-stu-id="1c20a-146">14</span></span>

<span data-ttu-id="1c20a-147">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="1c20a-147">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-148">15</span><span class="sxs-lookup"><span data-stu-id="1c20a-148">15</span></span>

<span data-ttu-id="1c20a-149">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="1c20a-149">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-150">16</span><span class="sxs-lookup"><span data-stu-id="1c20a-150">16</span></span>

<span data-ttu-id="1c20a-151">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="1c20a-151">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-152">17</span><span class="sxs-lookup"><span data-stu-id="1c20a-152">17</span></span>

<span data-ttu-id="1c20a-153">Privilegios no mantenidos.</span><span class="sxs-lookup"><span data-stu-id="1c20a-153">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1c20a-154">21</span><span class="sxs-lookup"><span data-stu-id="1c20a-154">21</span></span>

<span data-ttu-id="1c20a-155">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="1c20a-155">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c20a-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c20a-156">Remarks</span></span>

<span data-ttu-id="1c20a-157">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="1c20a-157">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1c20a-158">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="1c20a-158">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1c20a-159">Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf.</span><span class="sxs-lookup"><span data-stu-id="1c20a-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1c20a-160">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="1c20a-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c20a-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c20a-161">Requirements</span></span>



| <span data-ttu-id="1c20a-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c20a-162">Requirement</span></span> | <span data-ttu-id="1c20a-163">Valor</span><span class="sxs-lookup"><span data-stu-id="1c20a-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c20a-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c20a-164">Minimum supported client</span></span><br/> | <span data-ttu-id="1c20a-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c20a-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c20a-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c20a-166">Minimum supported server</span></span><br/> | <span data-ttu-id="1c20a-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c20a-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c20a-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1c20a-168">Namespace</span></span><br/>                | <span data-ttu-id="1c20a-169">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="1c20a-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c20a-170">MOF</span><span class="sxs-lookup"><span data-stu-id="1c20a-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c20a-171"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c20a-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c20a-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c20a-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c20a-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c20a-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c20a-174">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1c20a-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c20a-175">Directorio \_ CIM</span><span class="sxs-lookup"><span data-stu-id="1c20a-175">CIM\_Directory</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="1c20a-176">**Directorio \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="1c20a-176">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

