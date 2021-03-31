---
description: Determina si el llamador tiene los permisos agregados en el \_ objeto CIM LogicalFile y el recurso compartido en el que reside el archivo o directorio, según lo especificado por el argumento Permissions.
ms.assetid: 7b6845df-2427-44a8-bd91-9a4ba65caa51
ms.tgt_platform: multiple
title: Método GetEffectivePermission de la clase CIM_LogicalFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cc578436c5d116e202911d2bb68edf7369564a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152995"
---
# <a name="geteffectivepermission-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="e71a4-103">Método GetEffectivePermission de la \_ clase LogicalFile de CIM</span><span class="sxs-lookup"><span data-stu-id="e71a4-103">GetEffectivePermission method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="e71a4-104">El método **GetEffectivePermission** determina si el llamador tiene los permisos agregados en el [**objeto \_ LogicalFile de CIM**](cim-logicalfile.md) y el recurso compartido en el que reside el archivo o directorio, según lo especificado por el argumento *Permissions* .</span><span class="sxs-lookup"><span data-stu-id="e71a4-104">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_LogicalFile**](cim-logicalfile.md) object, and the share on which the file or directory resides, as specified by the *Permissions* argument.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e71a4-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="e71a4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e71a4-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e71a4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e71a4-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e71a4-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e71a4-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e71a4-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e71a4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e71a4-109">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="e71a4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e71a4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71a4-111">*Permisos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e71a4-111">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e71a4-112">Lista de permisos que el usuario puede consultar.</span><span class="sxs-lookup"><span data-stu-id="e71a4-112">List of permissions that the user can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="e71a4-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)</span><span class="sxs-lookup"><span data-stu-id="e71a4-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-114">Concede el derecho a leer los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="e71a4-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="e71a4-115">Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.</span><span class="sxs-lookup"><span data-stu-id="e71a4-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="e71a4-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)</span><span class="sxs-lookup"><span data-stu-id="e71a4-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-117">Concede el derecho para escribir datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="e71a4-117">Grants the right to write data to the file.</span></span> <span data-ttu-id="e71a4-118">Para un directorio, este valor concede el derecho a crear un archivo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="e71a4-118">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="e71a4-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Archivo \_ de ANEXAr \_ datos (archivo) o archivo \_ agregar \_ subdirectorio (directorio)** (4)</span><span class="sxs-lookup"><span data-stu-id="e71a4-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-120">Concede el derecho para anexar datos al archivo.</span><span class="sxs-lookup"><span data-stu-id="e71a4-120">Grants the right to append data to the file.</span></span> <span data-ttu-id="e71a4-121">Para un directorio, este valor concede el derecho a crear un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="e71a4-121">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="e71a4-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Archivo \_ de LEER \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="e71a4-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-123">Concede el derecho para leer atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="e71a4-123">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="e71a4-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Archivo \_ de ESCRIBIR \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="e71a4-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-125">Concede el derecho para escribir atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="e71a4-125">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="e71a4-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)</span><span class="sxs-lookup"><span data-stu-id="e71a4-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-127">Concede el derecho para ejecutar un archivo.</span><span class="sxs-lookup"><span data-stu-id="e71a4-127">Grants the right to execute a file.</span></span> <span data-ttu-id="e71a4-128">Para un directorio, se puede atravesar el directorio.</span><span class="sxs-lookup"><span data-stu-id="e71a4-128">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="e71a4-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)</span><span class="sxs-lookup"><span data-stu-id="e71a4-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-130">Concede el derecho para eliminar un directorio y todos los archivos que contiene, aunque los archivos sean de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e71a4-130">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="e71a4-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Archivo \_ de \_Atributos de lectura** (128)</span><span class="sxs-lookup"><span data-stu-id="e71a4-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-132">Concede el derecho a leer los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="e71a4-132">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="e71a4-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Archivo \_ de \_Atributos de escritura** (256)</span><span class="sxs-lookup"><span data-stu-id="e71a4-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-134">Concede el derecho para cambiar los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="e71a4-134">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="e71a4-135"><span id="DELETE"></span><span id="delete"></span>**Eliminar** (65536)</span><span class="sxs-lookup"><span data-stu-id="e71a4-135"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-136">Concede acceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="e71a4-136">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="e71a4-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leer \_ CONTROL** (131072)</span><span class="sxs-lookup"><span data-stu-id="e71a4-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-138">Concede acceso de lectura al descriptor de seguridad y al propietario.</span><span class="sxs-lookup"><span data-stu-id="e71a4-138">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="e71a4-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Escribir \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="e71a4-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-140">Concede acceso de escritura a la ACL discrecional.</span><span class="sxs-lookup"><span data-stu-id="e71a4-140">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="e71a4-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Escribir \_ PROPIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="e71a4-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-142">Asigna el propietario de la escritura.</span><span class="sxs-lookup"><span data-stu-id="e71a4-142">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="e71a4-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="e71a4-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="e71a4-144">Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="e71a4-144">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e71a4-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e71a4-145">Return value</span></span>

<span data-ttu-id="e71a4-146">Devuelve **true** si la llamada tiene el permiso necesario; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="e71a4-146">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e71a4-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e71a4-147">Remarks</span></span>

<span data-ttu-id="e71a4-148">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="e71a4-148">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e71a4-149">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="e71a4-149">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e71a4-150">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="e71a4-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e71a4-151">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="e71a4-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e71a4-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e71a4-152">Requirements</span></span>



| <span data-ttu-id="e71a4-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="e71a4-153">Requirement</span></span> | <span data-ttu-id="e71a4-154">Value</span><span class="sxs-lookup"><span data-stu-id="e71a4-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e71a4-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e71a4-155">Minimum supported client</span></span><br/> | <span data-ttu-id="e71a4-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e71a4-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e71a4-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e71a4-157">Minimum supported server</span></span><br/> | <span data-ttu-id="e71a4-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e71a4-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e71a4-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e71a4-159">Namespace</span></span><br/>                | <span data-ttu-id="e71a4-160">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e71a4-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e71a4-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e71a4-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="e71a4-162"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="e71a4-162"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="e71a4-163">MOF</span><span class="sxs-lookup"><span data-stu-id="e71a4-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e71a4-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e71a4-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e71a4-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e71a4-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e71a4-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e71a4-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e71a4-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="e71a4-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e71a4-168">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e71a4-168">**CIM\_LogicalFile**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="e71a4-169">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e71a4-169">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

