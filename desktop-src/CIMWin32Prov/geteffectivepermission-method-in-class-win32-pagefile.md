---
description: Determina si el usuario tiene todos los permisos necesarios especificados en el parámetro de permisos identificado para el objeto de archivo de \_ paginación Win32, el directorio y el recurso compartido en el que se encuentra el archivo de paginación, si el archivo o el directorio está en un recurso compartido.
ms.assetid: 1c417ac2-6968-4faf-b596-8df9308f8647
ms.tgt_platform: multiple
title: Método GetEffectivePermission de la clase Win32_PageFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3b9985d18e93f3a3dbcc8f65484bf3fd72284fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998232"
---
# <a name="geteffectivepermission-method-of-the-win32_pagefile-class"></a><span data-ttu-id="e19b9-103">Método GetEffectivePermission de la clase de archivo de \_ paginación Win32</span><span class="sxs-lookup"><span data-stu-id="e19b9-103">GetEffectivePermission method of the Win32\_PageFile class</span></span>

<span data-ttu-id="e19b9-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) determina si el usuario tiene todos los permisos necesarios especificados en el parámetro de *permisos* identificado para el objeto de archivo de [**\_ paginación Win32**](win32-pagefile.md) , el directorio y el recurso compartido en el que se encuentra el archivo de paginación, si el archivo o el directorio están en un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="e19b9-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method determines whether the user has all of the required permissions specified in the *Permissions* parameter identified for the [**Win32\_PageFile**](win32-pagefile.md) object, directory, and share where the paging file is located, if the file or directory are on a share.</span></span>

<span data-ttu-id="e19b9-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e19b9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e19b9-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e19b9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e19b9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e19b9-107">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="e19b9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e19b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e19b9-109">*Permisos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e19b9-109">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e19b9-110">Mapa de bits de los permisos que puede consultar el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e19b9-110">Bitmap of permissions that the caller can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="e19b9-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Archivo \_ de LEER \_ datos (archivo) directorio de lista de archivos ( \_ \_ directorio)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="e19b9-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-112">Concede el derecho a leer los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="e19b9-112">Grants the right to read data from the file.</span></span> <span data-ttu-id="e19b9-113">Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.</span><span class="sxs-lookup"><span data-stu-id="e19b9-113">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="e19b9-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Archivo \_ de ESCRIBIR archivo de \_ datos (archivo) \_ agregar \_ archivo (directorio)** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="e19b9-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-115">Concede el derecho para escribir datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="e19b9-115">Grants the right to write data to the file.</span></span> <span data-ttu-id="e19b9-116">Para un directorio, este valor concede el derecho a crear un archivo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="e19b9-116">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="e19b9-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Archivo \_ de ANEXAr \_ archivo de datos (archivo) \_ agregar \_ subdirectorio (directorio)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="e19b9-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-118">Concede el derecho para anexar datos al archivo.</span><span class="sxs-lookup"><span data-stu-id="e19b9-118">Grants the right to append data to the file.</span></span> <span data-ttu-id="e19b9-119">Para un directorio, este valor concede el derecho a crear un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="e19b9-119">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="e19b9-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Archivo \_ de LEER \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="e19b9-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-121">Concede el derecho para leer atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="e19b9-121">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="e19b9-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Archivo \_ de ESCRIBIR \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="e19b9-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-123">Concede el derecho para escribir atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="e19b9-123">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span data-ttu-id="e19b9-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**Archivo \_ de EJECUTAR (archivo) recorrido de archivos ( \_ directorio)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="e19b9-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-125">Concede el derecho para ejecutar un archivo.</span><span class="sxs-lookup"><span data-stu-id="e19b9-125">Grants the right to execute a file.</span></span> <span data-ttu-id="e19b9-126">Para un directorio, se puede atravesar el directorio.</span><span class="sxs-lookup"><span data-stu-id="e19b9-126">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="e19b9-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="e19b9-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-128">Concede el derecho para eliminar un directorio y todos los archivos que contiene, aunque los archivos sean de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e19b9-128">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="e19b9-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Archivo \_ de \_Atributos de lectura** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="e19b9-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-130">Concede el derecho a leer los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="e19b9-130">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="e19b9-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Archivo \_ de \_Atributos de escritura** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="e19b9-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-132">Concede el derecho para cambiar los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="e19b9-132">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="e19b9-133"><span id="DELETE"></span><span id="delete"></span>**Eliminar** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="e19b9-133"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-134">Concede acceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="e19b9-134">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="e19b9-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leer \_ CONTROL** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="e19b9-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-136">Concede acceso de lectura al descriptor de seguridad y al propietario.</span><span class="sxs-lookup"><span data-stu-id="e19b9-136">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="e19b9-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Escribir \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="e19b9-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-138">Concede acceso de escritura a la lista de control de acceso discrecional (DACL).</span><span class="sxs-lookup"><span data-stu-id="e19b9-138">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="e19b9-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Escribir \_ PROPIETARIO** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="e19b9-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-140">Asigna el propietario de la escritura.</span><span class="sxs-lookup"><span data-stu-id="e19b9-140">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="e19b9-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="e19b9-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="e19b9-142">Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="e19b9-142">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e19b9-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e19b9-143">Return value</span></span>

<span data-ttu-id="e19b9-144">Devuelve **true** si el llamador tiene los permisos especificados y **false** si el llamador no tiene los permisos especificados.</span><span class="sxs-lookup"><span data-stu-id="e19b9-144">Returns **True** if the caller has the specified permissions, and **false** if the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e19b9-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e19b9-145">Requirements</span></span>



| <span data-ttu-id="e19b9-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e19b9-146">Requirement</span></span> | <span data-ttu-id="e19b9-147">Value</span><span class="sxs-lookup"><span data-stu-id="e19b9-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e19b9-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e19b9-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e19b9-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e19b9-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e19b9-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e19b9-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e19b9-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e19b9-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e19b9-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e19b9-152">Namespace</span></span><br/>                | <span data-ttu-id="e19b9-153">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e19b9-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e19b9-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e19b9-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="e19b9-155"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="e19b9-155"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="e19b9-156">MOF</span><span class="sxs-lookup"><span data-stu-id="e19b9-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e19b9-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e19b9-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e19b9-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e19b9-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e19b9-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e19b9-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e19b9-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="e19b9-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="e19b9-161">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e19b9-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e19b9-162">**Archivo de \_ paginación Win32**</span><span class="sxs-lookup"><span data-stu-id="e19b9-162">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

