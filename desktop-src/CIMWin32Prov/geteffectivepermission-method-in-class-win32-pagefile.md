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
# <a name="geteffectivepermission-method-of-the-win32_pagefile-class"></a>Método GetEffectivePermission de la clase de archivo de \_ paginación Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) determina si el usuario tiene todos los permisos necesarios especificados en el parámetro de *permisos* identificado para el objeto de archivo de [**\_ paginación Win32**](win32-pagefile.md) , el directorio y el recurso compartido en el que se encuentra el archivo de paginación, si el archivo o el directorio están en un recurso compartido.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Permisos* \[ de de\]
</dt> <dd>

Mapa de bits de los permisos que puede consultar el autor de la llamada.

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Archivo \_ de LEER \_ datos (archivo) directorio de lista de archivos ( \_ \_ directorio)** (1 (0x1))


</dt> <dd>

Concede el derecho a leer los datos del archivo. Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Archivo \_ de ESCRIBIR archivo de \_ datos (archivo) \_ agregar \_ archivo (directorio)** (2 (0X2))


</dt> <dd>

Concede el derecho para escribir datos en el archivo. Para un directorio, este valor concede el derecho a crear un archivo en el directorio.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Archivo \_ de ANEXAr \_ archivo de datos (archivo) \_ agregar \_ subdirectorio (directorio)** (4 (0x4))


</dt> <dd>

Concede el derecho para anexar datos al archivo. Para un directorio, este valor concede el derecho a crear un subdirectorio.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Archivo \_ de LEER \_ EA** (8 (0x8))


</dt> <dd>

Concede el derecho para leer atributos extendidos.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Archivo \_ de ESCRIBIR \_ EA** (16 (0x10))


</dt> <dd>

Concede el derecho para escribir atributos extendidos.

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**Archivo \_ de EJECUTAR (archivo) recorrido de archivos ( \_ directorio)** (32 (0x20))


</dt> <dd>

Concede el derecho para ejecutar un archivo. Para un directorio, se puede atravesar el directorio.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64 (0x40))


</dt> <dd>

Concede el derecho para eliminar un directorio y todos los archivos que contiene, aunque los archivos sean de solo lectura.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Archivo \_ de \_Atributos de lectura** (128 (0x80))


</dt> <dd>

Concede el derecho a leer los atributos de archivo.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Archivo \_ de \_Atributos de escritura** (256 (0x100))


</dt> <dd>

Concede el derecho para cambiar los atributos de archivo.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**Eliminar** (65536 (0x10000))


</dt> <dd>

Concede acceso de eliminación.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Leer \_ CONTROL** (131072 (0x20000))


</dt> <dd>

Concede acceso de lectura al descriptor de seguridad y al propietario.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Escribir \_ DAC** (262144 (0x40000))


</dt> <dd>

Concede acceso de escritura a la lista de control de acceso discrecional (DACL).

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**Escribir \_ PROPIETARIO** (524288 (0x80000))


</dt> <dd>

Asigna el propietario de la escritura.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))


</dt> <dd>

Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el llamador tiene los permisos especificados y **false** si el llamador no tiene los permisos especificados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| Encabezado<br/>                   | <dl> <dt>Aclui. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Archivo de \_ paginación Win32**](win32-pagefile.md)
</dt> </dl>

 

