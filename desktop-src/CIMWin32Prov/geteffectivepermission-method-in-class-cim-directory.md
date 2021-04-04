---
description: Determina si el llamador tiene los permisos agregados en el \_ objeto de directorio CIM y el recurso compartido en el que reside el archivo o directorio, según lo especificado por el argumento Permission. Este método se hereda de \_ LOGICALFILE CIM.
ms.assetid: b3dc1e3c-5c99-46ba-93c4-15fbf18e98e8
ms.tgt_platform: multiple
title: Método GetEffectivePermission de la clase CIM_Directory (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 436a30517b7f3306ef8be2426385fe385947296e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907141"
---
# <a name="geteffectivepermission-method-of-the-cim_directory-class"></a><span data-ttu-id="c35c9-104">Método GetEffectivePermission de la \_ clase de directorio CIM</span><span class="sxs-lookup"><span data-stu-id="c35c9-104">GetEffectivePermission method of the CIM\_Directory class</span></span>

<span data-ttu-id="c35c9-105">El método **GetEffectivePermission** determina si el llamador tiene los permisos agregados en el objeto de [**\_ directorio CIM**](cim-directory.md) y el recurso compartido en el que reside el archivo o directorio, según lo especificado por el argumento **Permission** .</span><span class="sxs-lookup"><span data-stu-id="c35c9-105">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_Directory**](cim-directory.md) object, and the share on which the file or directory resides, as specified by the **Permission** argument.</span></span> <span data-ttu-id="c35c9-106">Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c35c9-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c35c9-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c35c9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c35c9-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c35c9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c35c9-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c35c9-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c35c9-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c35c9-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c35c9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c35c9-111">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="c35c9-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c35c9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c35c9-113">*Permisos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c35c9-113">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c35c9-114">Lista de permisos que el usuario puede consultar.</span><span class="sxs-lookup"><span data-stu-id="c35c9-114">List of permissions that the user can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="c35c9-115"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Archivo \_ de LEER \_ datos (archivo) directorio de lista de archivos ( \_ \_ directorio)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="c35c9-115"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-116">Concede el derecho a leer los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="c35c9-116">Grants the right to read data from the file.</span></span> <span data-ttu-id="c35c9-117">Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.</span><span class="sxs-lookup"><span data-stu-id="c35c9-117">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="c35c9-118"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Archivo \_ de ESCRIBIR archivo de \_ datos (archivo) \_ agregar \_ archivo (directorio)** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="c35c9-118"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-119">Concede el derecho para escribir datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="c35c9-119">Grants the right to write data to the file.</span></span> <span data-ttu-id="c35c9-120">Para un directorio, este valor concede el derecho a crear un archivo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="c35c9-120">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="c35c9-121"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Archivo \_ de ANEXAr \_ archivo de datos (archivo) \_ agregar \_ subdirectorio (directorio)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="c35c9-121"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-122">Concede el derecho para anexar datos al archivo.</span><span class="sxs-lookup"><span data-stu-id="c35c9-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="c35c9-123">Para un directorio, este valor concede el derecho a crear un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="c35c9-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="c35c9-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Archivo \_ de LEER \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="c35c9-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-125">Concede el derecho para leer atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="c35c9-125">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="c35c9-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Archivo \_ de ESCRIBIR \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="c35c9-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-127">Concede el derecho para escribir atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="c35c9-127">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="c35c9-128"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**Archivo \_ de EJECUTAR (archivo) recorrido de archivos ( \_ directorio)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="c35c9-128"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-129">Concede el derecho para ejecutar un archivo.</span><span class="sxs-lookup"><span data-stu-id="c35c9-129">Grants the right to execute a file.</span></span> <span data-ttu-id="c35c9-130">Para un directorio, se puede atravesar el directorio.</span><span class="sxs-lookup"><span data-stu-id="c35c9-130">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="c35c9-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="c35c9-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-132">Concede el derecho para eliminar un directorio y todos los archivos que contiene, aunque los archivos sean de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c35c9-132">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="c35c9-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Archivo \_ de \_Atributos de lectura** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="c35c9-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-134">Concede el derecho a leer los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="c35c9-134">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="c35c9-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Archivo \_ de \_Atributos de escritura** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="c35c9-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-136">Concede el derecho para cambiar los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="c35c9-136">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="c35c9-137"><span id="DELETE"></span><span id="delete"></span>**Eliminar** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="c35c9-137"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-138">Concede acceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="c35c9-138">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="c35c9-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leer \_ CONTROL** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="c35c9-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-140">Concede acceso de lectura al descriptor de seguridad y al propietario.</span><span class="sxs-lookup"><span data-stu-id="c35c9-140">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="c35c9-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Escribir \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="c35c9-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-142">Concede acceso de escritura a la ACL discrecional.</span><span class="sxs-lookup"><span data-stu-id="c35c9-142">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="c35c9-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Escribir \_ PROPIETARIO** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="c35c9-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-144">Asigna el propietario de la escritura.</span><span class="sxs-lookup"><span data-stu-id="c35c9-144">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="c35c9-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="c35c9-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="c35c9-146">Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="c35c9-146">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c35c9-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c35c9-147">Return value</span></span>

<span data-ttu-id="c35c9-148">Devuelve **true** si la llamada tiene el permiso necesario; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="c35c9-148">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c35c9-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c35c9-149">Remarks</span></span>

<span data-ttu-id="c35c9-150">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="c35c9-150">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c35c9-151">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="c35c9-151">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c35c9-152">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c35c9-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c35c9-153">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c35c9-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c35c9-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c35c9-154">Requirements</span></span>



| <span data-ttu-id="c35c9-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="c35c9-155">Requirement</span></span> | <span data-ttu-id="c35c9-156">Value</span><span class="sxs-lookup"><span data-stu-id="c35c9-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c35c9-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c35c9-157">Minimum supported client</span></span><br/> | <span data-ttu-id="c35c9-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c35c9-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c35c9-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c35c9-159">Minimum supported server</span></span><br/> | <span data-ttu-id="c35c9-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c35c9-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c35c9-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c35c9-161">Namespace</span></span><br/>                | <span data-ttu-id="c35c9-162">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c35c9-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c35c9-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c35c9-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="c35c9-164"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="c35c9-164"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="c35c9-165">MOF</span><span class="sxs-lookup"><span data-stu-id="c35c9-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c35c9-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c35c9-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c35c9-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c35c9-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c35c9-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c35c9-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c35c9-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="c35c9-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c35c9-170">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="c35c9-170">**CIM\_Directory**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="c35c9-171">**\_Directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="c35c9-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

