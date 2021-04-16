---
description: Cambia los permisos de seguridad para el archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método ChangeSecurityPermissions y se hereda de CIM \_ LogicalFile).
ms.assetid: 5c1f66ba-9aa1-47ca-8fcf-7663782544cd
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx de la clase CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2d8ddf4c6ffdbd016db1e8c08d89f2dd6476ccf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659531"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_directory-class"></a><span data-ttu-id="6f9f8-103">Método ChangeSecurityPermissionsEx de la \_ clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="6f9f8-103">ChangeSecurityPermissionsEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="6f9f8-104">El método **ChangeSecurityPermissionsEx** cambia los permisos de seguridad para el archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) y se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md)).</span><span class="sxs-lookup"><span data-stu-id="6f9f8-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md)).</span></span> <span data-ttu-id="6f9f8-105">Si el archivo lógico es un directorio, este método actuará de forma recursiva y cambiará los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f9f8-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6f9f8-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6f9f8-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6f9f8-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="6f9f8-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6f9f8-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6f9f8-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f9f8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f9f8-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="6f9f8-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f9f8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f9f8-112">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f9f8-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9f8-113">Especifica la información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="6f9f8-114">Una ACL **nula** en la estructura del [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="6f9f8-115">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6f9f8-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9f8-116">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-116">Security privilege to modify.</span></span> <span data-ttu-id="6f9f8-117">Por ejemplo, para cambiar la seguridad de la DACL y el propietario, use</span><span class="sxs-lookup"><span data-stu-id="6f9f8-117">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="6f9f8-118">or</span><span class="sxs-lookup"><span data-stu-id="6f9f8-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="6f9f8-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="6f9f8-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6f9f8-120">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="6f9f8-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="6f9f8-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6f9f8-122">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="6f9f8-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="6f9f8-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6f9f8-124">Cambie la ACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="6f9f8-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="6f9f8-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6f9f8-126">Cambie la ACL del sistema del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6f9f8-127">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6f9f8-127">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9f8-128">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-128">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="6f9f8-129">Este parámetro tiene un valor **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-129">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="6f9f8-130">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6f9f8-130">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9f8-131">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-131">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="6f9f8-132">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo (o directorio) en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-132">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="6f9f8-133">Si el valor del parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="6f9f8-133">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="6f9f8-134">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6f9f8-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9f8-135">Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ directorio CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="6f9f8-135">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="6f9f8-136">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-136">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f9f8-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f9f8-137">Return value</span></span>

<span data-ttu-id="6f9f8-138">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-138">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-139">0</span><span class="sxs-lookup"><span data-stu-id="6f9f8-139">0</span></span>

<span data-ttu-id="6f9f8-140">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-140">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-141">2</span><span class="sxs-lookup"><span data-stu-id="6f9f8-141">2</span></span>

<span data-ttu-id="6f9f8-142">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-142">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-143">8</span><span class="sxs-lookup"><span data-stu-id="6f9f8-143">8</span></span>

<span data-ttu-id="6f9f8-144">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-144">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-145">9</span><span class="sxs-lookup"><span data-stu-id="6f9f8-145">9</span></span>

<span data-ttu-id="6f9f8-146">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-146">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-147">10</span><span class="sxs-lookup"><span data-stu-id="6f9f8-147">10</span></span>

<span data-ttu-id="6f9f8-148">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-148">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-149">11</span><span class="sxs-lookup"><span data-stu-id="6f9f8-149">11</span></span>

<span data-ttu-id="6f9f8-150">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-150">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-151">12</span><span class="sxs-lookup"><span data-stu-id="6f9f8-151">12</span></span>

<span data-ttu-id="6f9f8-152">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-152">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-153">13</span><span class="sxs-lookup"><span data-stu-id="6f9f8-153">13</span></span>

<span data-ttu-id="6f9f8-154">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-154">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-155">14</span><span class="sxs-lookup"><span data-stu-id="6f9f8-155">14</span></span>

<span data-ttu-id="6f9f8-156">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-156">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-157">15</span><span class="sxs-lookup"><span data-stu-id="6f9f8-157">15</span></span>

<span data-ttu-id="6f9f8-158">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-158">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-159">16</span><span class="sxs-lookup"><span data-stu-id="6f9f8-159">16</span></span>

<span data-ttu-id="6f9f8-160">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-160">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-161">17</span><span class="sxs-lookup"><span data-stu-id="6f9f8-161">17</span></span>

<span data-ttu-id="6f9f8-162">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-162">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6f9f8-163">21</span><span class="sxs-lookup"><span data-stu-id="6f9f8-163">21</span></span>

<span data-ttu-id="6f9f8-164">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f9f8-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f9f8-165">Remarks</span></span>

<span data-ttu-id="6f9f8-166">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6f9f8-167">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6f9f8-168">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6f9f8-169">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f9f8-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f9f8-170">Requirements</span></span>



| <span data-ttu-id="6f9f8-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f9f8-171">Requirement</span></span> | <span data-ttu-id="6f9f8-172">Value</span><span class="sxs-lookup"><span data-stu-id="6f9f8-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f9f8-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f9f8-173">Minimum supported client</span></span><br/> | <span data-ttu-id="6f9f8-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f9f8-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f9f8-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f9f8-175">Minimum supported server</span></span><br/> | <span data-ttu-id="6f9f8-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f9f8-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f9f8-177">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f9f8-177">Namespace</span></span><br/>                | <span data-ttu-id="6f9f8-178">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6f9f8-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6f9f8-179">MOF</span><span class="sxs-lookup"><span data-stu-id="6f9f8-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f9f8-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f9f8-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f9f8-181">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f9f8-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f9f8-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f9f8-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f9f8-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f9f8-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f9f8-184">\_Directorio CIM</span><span class="sxs-lookup"><span data-stu-id="6f9f8-184">CIM\_Directory</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="6f9f8-185">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="6f9f8-185">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

