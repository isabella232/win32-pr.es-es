---
description: Cambia los permisos de seguridad para el archivo de datos lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método ChangeSecurityPermissions).
ms.assetid: baf50a6e-f624-464e-946d-975aeba88ac2
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx de la clase CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c97f9b17fd148a0686a96fb46f77694a2b78b21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538998"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_datafile-class"></a><span data-ttu-id="4d207-103">Método ChangeSecurityPermissionsEx de la \_ clase de archivo de archivos CIM</span><span class="sxs-lookup"><span data-stu-id="4d207-103">ChangeSecurityPermissionsEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="4d207-104">El método **ChangeSecurityPermissionsEx** cambia los permisos de seguridad para el archivo de datos lógico especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) ).</span><span class="sxs-lookup"><span data-stu-id="4d207-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical data file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) method).</span></span> <span data-ttu-id="4d207-105">Si el archivo lógico es realmente un directorio, este método actuará de forma recursiva y cambiará los permisos de seguridad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="4d207-105">If the logical file is actually a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d207-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="4d207-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4d207-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4d207-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4d207-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4d207-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4d207-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4d207-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d207-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d207-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="4d207-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d207-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d207-112">*SecurityDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d207-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d207-113">Especifica la información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4d207-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="4d207-114">Una ACL **nula** en la estructura del [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="4d207-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="4d207-115">Para obtener más información sobre las implicaciones de acceso ilimitado, vea [crear un descriptor de seguridad para un nuevo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="4d207-115">For more information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="4d207-116">*Opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4d207-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d207-117">Privilegio de seguridad que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="4d207-117">Security privilege to modify.</span></span> <span data-ttu-id="4d207-118">Por ejemplo, para cambiar la seguridad de la DACL y el propietario, use:</span><span class="sxs-lookup"><span data-stu-id="4d207-118">For example, to change the owner and DACL security, use:</span></span>

<span data-ttu-id="4d207-119">`Option = 1 + 4` o `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span><span class="sxs-lookup"><span data-stu-id="4d207-119">`Option = 1 + 4` or `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span></span>

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="4d207-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad del propietario** (1)</span><span class="sxs-lookup"><span data-stu-id="4d207-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4d207-121">Cambiar el propietario del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4d207-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="4d207-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="4d207-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4d207-123">Cambiar el grupo del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4d207-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="4d207-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="4d207-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4d207-125">Cambie la ACL del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4d207-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="4d207-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Cambiar \_ \_ \_ Información de seguridad de SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="4d207-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4d207-127">Cambie la ACL del sistema del archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="4d207-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4d207-128">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4d207-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d207-129">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="4d207-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="4d207-130">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="4d207-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-131">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4d207-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d207-132">Cadena que representa el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="4d207-132">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="4d207-133">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="4d207-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="4d207-134">Si este parámetro es **null**, la operación se realiza en el archivo (o directorio) especificado en la llamada **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="4d207-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="4d207-135">Si se utiliza *StartFileName* , *Recursive* también debe establecerse en true.</span><span class="sxs-lookup"><span data-stu-id="4d207-135">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-136">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4d207-136">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d207-137">Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**archivo de \_ archivos CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="4d207-137">If **True**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="4d207-138">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="4d207-138">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d207-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d207-139">Return value</span></span>

<span data-ttu-id="4d207-140">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="4d207-140">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="4d207-141">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="4d207-141">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4d207-142">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4d207-142">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4d207-143">**Success**</span><span class="sxs-lookup"><span data-stu-id="4d207-143">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-144">0</span><span class="sxs-lookup"><span data-stu-id="4d207-144">0</span></span>

<span data-ttu-id="4d207-145">Correcto.</span><span class="sxs-lookup"><span data-stu-id="4d207-145">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-146">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="4d207-146">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-147">2</span><span class="sxs-lookup"><span data-stu-id="4d207-147">2</span></span>

<span data-ttu-id="4d207-148">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="4d207-148">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-149">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="4d207-149">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-150">8</span><span class="sxs-lookup"><span data-stu-id="4d207-150">8</span></span>

<span data-ttu-id="4d207-151">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="4d207-151">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-152">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="4d207-152">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-153">9</span><span class="sxs-lookup"><span data-stu-id="4d207-153">9</span></span>

<span data-ttu-id="4d207-154">El nombre de objeto especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="4d207-154">Object name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-155">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="4d207-155">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-156">10</span><span class="sxs-lookup"><span data-stu-id="4d207-156">10</span></span>

<span data-ttu-id="4d207-157">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="4d207-157">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-158">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="4d207-158">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-159">11</span><span class="sxs-lookup"><span data-stu-id="4d207-159">11</span></span>

<span data-ttu-id="4d207-160">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="4d207-160">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-161">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="4d207-161">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-162">12</span><span class="sxs-lookup"><span data-stu-id="4d207-162">12</span></span>

<span data-ttu-id="4d207-163">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="4d207-163">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-164">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="4d207-164">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-165">13</span><span class="sxs-lookup"><span data-stu-id="4d207-165">13</span></span>

<span data-ttu-id="4d207-166">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="4d207-166">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-167">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="4d207-167">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-168">14</span><span class="sxs-lookup"><span data-stu-id="4d207-168">14</span></span>

<span data-ttu-id="4d207-169">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="4d207-169">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-170">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="4d207-170">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-171">15</span><span class="sxs-lookup"><span data-stu-id="4d207-171">15</span></span>

<span data-ttu-id="4d207-172">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="4d207-172">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-173">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="4d207-173">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-174">16</span><span class="sxs-lookup"><span data-stu-id="4d207-174">16</span></span>

<span data-ttu-id="4d207-175">El archivo de inicio no es válido.</span><span class="sxs-lookup"><span data-stu-id="4d207-175">The start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-176">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="4d207-176">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-177">17</span><span class="sxs-lookup"><span data-stu-id="4d207-177">17</span></span>

<span data-ttu-id="4d207-178">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="4d207-178">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="4d207-179">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="4d207-179">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4d207-180">21</span><span class="sxs-lookup"><span data-stu-id="4d207-180">21</span></span>

<span data-ttu-id="4d207-181">Un parámetro no es válido.</span><span class="sxs-lookup"><span data-stu-id="4d207-181">A parameter is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d207-182">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d207-182">Remarks</span></span>

<span data-ttu-id="4d207-183">WMI implementa el método **ChangeSecurityPermissionsEx** en el [**archivo de \_ archivos de CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="4d207-183">The **ChangeSecurityPermissionsEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="4d207-184">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="4d207-184">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4d207-185">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="4d207-185">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d207-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d207-186">Requirements</span></span>



| <span data-ttu-id="4d207-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d207-187">Requirement</span></span> | <span data-ttu-id="4d207-188">Value</span><span class="sxs-lookup"><span data-stu-id="4d207-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d207-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d207-189">Minimum supported client</span></span><br/> | <span data-ttu-id="4d207-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d207-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d207-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d207-191">Minimum supported server</span></span><br/> | <span data-ttu-id="4d207-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d207-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d207-193">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d207-193">Namespace</span></span><br/>                | <span data-ttu-id="4d207-194">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4d207-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4d207-195">MOF</span><span class="sxs-lookup"><span data-stu-id="4d207-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d207-196"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d207-196"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d207-197">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d207-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d207-198"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d207-198"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d207-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d207-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d207-200">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="4d207-200">**CIM\_DataFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="4d207-201">**\_Archivo de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="4d207-201">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="4d207-202">Tareas de WMI: archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="4d207-202">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="4d207-203">**Constantes de derechos de acceso a archivos y directorios**</span><span class="sxs-lookup"><span data-stu-id="4d207-203">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

