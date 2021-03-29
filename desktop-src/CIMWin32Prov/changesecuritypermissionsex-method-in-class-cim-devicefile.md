---
description: Cambia los permisos de seguridad para el archivo de dispositivo especificado en la ruta de acceso del objeto (este método es una versión extendida del método ChangeSecurityPermissions).
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx de la clase CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f2c7261844542f6414052517432c2e8ff3f1194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153232"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="dca76-103">Método ChangeSecurityPermissionsEx de la \_ clase DeviceFile de CIM</span><span class="sxs-lookup"><span data-stu-id="dca76-103">ChangeSecurityPermissionsEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="dca76-104">El método **ChangeSecurityPermissionsEx** cambia los permisos de seguridad para el archivo de dispositivo especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) ).</span><span class="sxs-lookup"><span data-stu-id="dca76-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the device file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) method).</span></span> <span data-ttu-id="dca76-105">Si el archivo lógico es un directorio, este método actúa de forma recursiva y cambia los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="dca76-105">If the logical file is a directory, then this method acts recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="dca76-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="dca76-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dca76-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="dca76-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dca76-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dca76-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dca76-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="dca76-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dca76-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dca76-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dca76-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dca76-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="dca76-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dca76-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dca76-113">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dca76-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dca76-114">Especifica la información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="dca76-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="dca76-115">Una ACL **nula** en la estructura del [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="dca76-115">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="dca76-116">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="dca76-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dca76-117">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="dca76-117">Security privilege to modify.</span></span> <span data-ttu-id="dca76-118">Por ejemplo, para cambiar la seguridad de la DACL y el propietario, use</span><span class="sxs-lookup"><span data-stu-id="dca76-118">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="dca76-119">or</span><span class="sxs-lookup"><span data-stu-id="dca76-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="dca76-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="dca76-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dca76-121">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dca76-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="dca76-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="dca76-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dca76-123">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dca76-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="dca76-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="dca76-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dca76-125">Cambie la ACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dca76-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="dca76-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="dca76-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="dca76-127">Cambie la ACL del sistema del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dca76-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dca76-128">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dca76-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dca76-129">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="dca76-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="dca76-130">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="dca76-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="dca76-131">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dca76-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dca76-132">Archivo secundario (o directorio) que se va a usar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="dca76-132">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="dca76-133">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="dca76-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="dca76-134">Si este parámetro es **null**, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="dca76-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="dca76-135">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dca76-135">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dca76-136">Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ DeviceFile de CIM**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="dca76-136">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="dca76-137">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="dca76-137">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dca76-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dca76-138">Return value</span></span>

<span data-ttu-id="dca76-139">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="dca76-139">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="dca76-140">0</span><span class="sxs-lookup"><span data-stu-id="dca76-140">0</span></span>

<span data-ttu-id="dca76-141">Correcto.</span><span class="sxs-lookup"><span data-stu-id="dca76-141">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-142">2</span><span class="sxs-lookup"><span data-stu-id="dca76-142">2</span></span>

<span data-ttu-id="dca76-143">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="dca76-143">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-144">8</span><span class="sxs-lookup"><span data-stu-id="dca76-144">8</span></span>

<span data-ttu-id="dca76-145">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="dca76-145">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-146">9</span><span class="sxs-lookup"><span data-stu-id="dca76-146">9</span></span>

<span data-ttu-id="dca76-147">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="dca76-147">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-148">10</span><span class="sxs-lookup"><span data-stu-id="dca76-148">10</span></span>

<span data-ttu-id="dca76-149">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="dca76-149">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-150">11</span><span class="sxs-lookup"><span data-stu-id="dca76-150">11</span></span>

<span data-ttu-id="dca76-151">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="dca76-151">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-152">12</span><span class="sxs-lookup"><span data-stu-id="dca76-152">12</span></span>

<span data-ttu-id="dca76-153">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="dca76-153">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-154">13</span><span class="sxs-lookup"><span data-stu-id="dca76-154">13</span></span>

<span data-ttu-id="dca76-155">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="dca76-155">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-156">14</span><span class="sxs-lookup"><span data-stu-id="dca76-156">14</span></span>

<span data-ttu-id="dca76-157">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="dca76-157">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-158">15</span><span class="sxs-lookup"><span data-stu-id="dca76-158">15</span></span>

<span data-ttu-id="dca76-159">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="dca76-159">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-160">16</span><span class="sxs-lookup"><span data-stu-id="dca76-160">16</span></span>

<span data-ttu-id="dca76-161">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="dca76-161">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-162">17</span><span class="sxs-lookup"><span data-stu-id="dca76-162">17</span></span>

<span data-ttu-id="dca76-163">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="dca76-163">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dca76-164">21</span><span class="sxs-lookup"><span data-stu-id="dca76-164">21</span></span>

<span data-ttu-id="dca76-165">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="dca76-165">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dca76-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dca76-166">Remarks</span></span>

<span data-ttu-id="dca76-167">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="dca76-167">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="dca76-168">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="dca76-168">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="dca76-169">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="dca76-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dca76-170">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="dca76-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dca76-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dca76-171">Requirements</span></span>



| <span data-ttu-id="dca76-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="dca76-172">Requirement</span></span> | <span data-ttu-id="dca76-173">Value</span><span class="sxs-lookup"><span data-stu-id="dca76-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dca76-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dca76-174">Minimum supported client</span></span><br/> | <span data-ttu-id="dca76-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dca76-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dca76-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dca76-176">Minimum supported server</span></span><br/> | <span data-ttu-id="dca76-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dca76-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dca76-178">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dca76-178">Namespace</span></span><br/>                | <span data-ttu-id="dca76-179">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dca76-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dca76-180">MOF</span><span class="sxs-lookup"><span data-stu-id="dca76-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dca76-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dca76-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dca76-182">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dca76-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dca76-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dca76-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dca76-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="dca76-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca76-185">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="dca76-185">CIM\_DeviceFile</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="dca76-186">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="dca76-186">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

