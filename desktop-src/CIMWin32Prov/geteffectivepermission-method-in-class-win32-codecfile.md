---
description: Usa los valores establecidos en el parámetro Permissions para determinar si el usuario tiene los permisos especificados establecidos en la propiedad AccessMask del \_ objeto CodecFile de Win32 que representa el archivo de códec.
ms.assetid: 068dfcaf-037b-4516-b85a-8ba6558ba561
ms.tgt_platform: multiple
title: Método GetEffectivePermission de la clase Win32_CodecFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc2f24071d5ab864e06686f094707d9111ea07ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907140"
---
# <a name="geteffectivepermission-method-of-the-win32_codecfile-class"></a><span data-ttu-id="2f092-103">Método GetEffectivePermission de la \_ clase CodecFile de Win32</span><span class="sxs-lookup"><span data-stu-id="2f092-103">GetEffectivePermission method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="2f092-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) usa los valores establecidos en el parámetro *Permissions* para determinar si el usuario tiene los permisos especificados establecidos en la propiedad **AccessMask** del objeto [**\_ CodecFile de Win32**](win32-codecfile.md) que representa el archivo de códec.</span><span class="sxs-lookup"><span data-stu-id="2f092-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses the values set in the *Permissions* parameter to determine whether the user has the specified permissions set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object that represents the codec file.</span></span> <span data-ttu-id="2f092-105">Los permisos se aplican al archivo, el directorio en el que reside el archivo y el recurso compartido, si el directorio o el archivo están en un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="2f092-105">The permissions apply to the file, the directory in which the file resides, and the share, if either the directory or the file are in a share.</span></span>

<span data-ttu-id="2f092-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="2f092-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2f092-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2f092-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f092-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f092-108">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="2f092-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f092-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f092-110">*Permisos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2f092-110">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f092-111">Mapa de bits de los permisos que se establecen en la propiedad **AccessMask** del objeto [**\_ CodecFile de Win32**](win32-codecfile.md) .</span><span class="sxs-lookup"><span data-stu-id="2f092-111">Bitmap of permissions that are set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="2f092-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Archivo \_ de LEER \_ datos (archivo) directorio de lista de archivos ( \_ \_ directorio)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="2f092-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-113">Concede el derecho a leer los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="2f092-113">Grants the right to read data from the file.</span></span> <span data-ttu-id="2f092-114">Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.</span><span class="sxs-lookup"><span data-stu-id="2f092-114">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="2f092-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Archivo \_ de ESCRIBIR archivo de \_ datos (archivo) \_ agregar \_ archivo (directorio)** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="2f092-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-116">Concede el derecho para escribir datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="2f092-116">Grants the right to write data to the file.</span></span> <span data-ttu-id="2f092-117">Para un directorio, este valor concede el derecho a crear un archivo en el directorio.</span><span class="sxs-lookup"><span data-stu-id="2f092-117">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="2f092-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Archivo \_ de ANEXAr \_ archivo de datos (archivo) \_ agregar \_ subdirectorio (directorio)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="2f092-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-119">Concede el derecho para anexar datos al archivo.</span><span class="sxs-lookup"><span data-stu-id="2f092-119">Grants the right to append data to the file.</span></span> <span data-ttu-id="2f092-120">Para un directorio, este valor concede el derecho a crear un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="2f092-120">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="2f092-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Archivo \_ de LEER \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="2f092-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-122">Concede el derecho para leer atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="2f092-122">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="2f092-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Archivo \_ de ESCRIBIR \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="2f092-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-124">Concede el derecho para escribir atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="2f092-124">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="2f092-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**Archivo \_ de EJECUTAR (archivo) recorrido de archivos ( \_ directorio)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="2f092-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-126">Concede el derecho para ejecutar un archivo.</span><span class="sxs-lookup"><span data-stu-id="2f092-126">Grants the right to execute a file.</span></span> <span data-ttu-id="2f092-127">Para un directorio, se puede atravesar el directorio.</span><span class="sxs-lookup"><span data-stu-id="2f092-127">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="2f092-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="2f092-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-129">Concede el derecho para eliminar un directorio y todos los archivos que contiene, aunque los archivos sean de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2f092-129">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="2f092-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Archivo \_ de \_Atributos de lectura** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="2f092-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-131">Concede el derecho a leer los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2f092-131">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="2f092-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Archivo \_ de \_Atributos de escritura** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="2f092-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-133">Concede el derecho para cambiar los atributos de archivo.</span><span class="sxs-lookup"><span data-stu-id="2f092-133">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="2f092-134"><span id="DELETE"></span><span id="delete"></span>**Eliminar** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="2f092-134"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-135">Concede acceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="2f092-135">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="2f092-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leer \_ CONTROL** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="2f092-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-137">Concede acceso de lectura al descriptor de seguridad y al propietario.</span><span class="sxs-lookup"><span data-stu-id="2f092-137">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="2f092-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Escribir \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="2f092-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-139">Concede acceso de escritura a la lista de control de acceso discrecional (ACL).</span><span class="sxs-lookup"><span data-stu-id="2f092-139">Grants write access to the discretionary access control list (ACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="2f092-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Escribir \_ PROPIETARIO** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="2f092-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-141">Asigna el propietario de la escritura.</span><span class="sxs-lookup"><span data-stu-id="2f092-141">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="2f092-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="2f092-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="2f092-143">Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="2f092-143">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f092-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f092-144">Return value</span></span>

<span data-ttu-id="2f092-145">Devuelve **verdadero** cuando el autor de la llamada tiene los permisos especificados y **false** cuando el autor de la llamada no tiene los permisos especificados.</span><span class="sxs-lookup"><span data-stu-id="2f092-145">Returns **True** when the caller has the specified permissions, and **false** when the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f092-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f092-146">Requirements</span></span>



| <span data-ttu-id="2f092-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f092-147">Requirement</span></span> | <span data-ttu-id="2f092-148">Value</span><span class="sxs-lookup"><span data-stu-id="2f092-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f092-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f092-149">Minimum supported client</span></span><br/> | <span data-ttu-id="2f092-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f092-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f092-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f092-151">Minimum supported server</span></span><br/> | <span data-ttu-id="2f092-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f092-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f092-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2f092-153">Namespace</span></span><br/>                | <span data-ttu-id="2f092-154">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2f092-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2f092-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f092-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f092-156"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f092-156"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="2f092-157">MOF</span><span class="sxs-lookup"><span data-stu-id="2f092-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f092-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f092-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f092-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f092-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f092-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f092-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f092-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f092-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f092-162">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f092-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2f092-163">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="2f092-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

