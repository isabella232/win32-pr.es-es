---
description: Determina si el usuario tiene todos los permisos necesarios especificados en el parámetro Permissions para el objeto de archivo, el directorio y el recurso compartido donde se encuentra el archivo de acceso directo, si el archivo o directorio está en un recurso compartido.
ms.assetid: 36f823c1-fa19-40a1-b750-41e1f73bdf01
ms.tgt_platform: multiple
title: Método GetEffectivePermission de la Win32_ShortcutFile (Aclui.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52b57318ac05212304024ead82026d6daf0d8ea4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974505"
---
# <a name="geteffectivepermission-method-of-the-win32_shortcutfile-class"></a>Método GetEffectivePermission de la clase ShortcutFile de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetEffectivePermission** determina si el usuario tiene todos los permisos necesarios especificados en el parámetro *Permissions* para el objeto de archivo, el directorio y el recurso compartido donde se encuentra el archivo de acceso directo, si el archivo o directorio está en un recurso compartido.

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Permisos* \[ En\]
</dt> <dd>

Mapa de bits de permisos.

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE \_ READ \_ DATA (archivo) FILE \_ LIST DIRECTORY \_ (directorio)** (1 (0x1))


</dt> <dd>

Concede el derecho a leer datos del archivo. Para un directorio, este valor concede el derecho a enumerar el contenido del directorio.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE \_ WRITE \_ DATA (file) FILE \_ ADD FILE \_ (directory)** (2 (0x2))


</dt> <dd>

Concede el derecho de escribir datos en el archivo. Para un directorio, este valor concede el derecho a crear un archivo en el directorio .

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE \_ APPEND \_ DATA (file) FILE \_ ADD \_ SUBDIRECTORY (directory)** (4 (0x4))


</dt> <dd>

Concede el derecho a anexar datos al archivo. Para un directorio, este valor concede el derecho a crear un subdirectorio.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE \_ READ \_ EA** (8 (0x8))


</dt> <dd>

Concede el derecho a leer atributos extendidos.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE \_ WRITE \_ EA** (16 (0x10))


</dt> <dd>

Concede el derecho a escribir atributos extendidos.

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**FILE \_ EXECUTE (archivo) FILE \_ TRAVERSE (directorio)** (32 (0x20))


</dt> <dd>

Concede el derecho a ejecutar un archivo. Para un directorio, se puede recorrer el directorio.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE \_ DELETE \_ CHILD (directorio)** (64 (0x40))


</dt> <dd>

Concede el derecho a eliminar un directorio y todos los archivos que contiene, incluso si los archivos son de solo lectura.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE \_ ATRIBUTOS \_ DE** LECTURA (128 (0x80))


</dt> <dd>

Concede el derecho a leer atributos de archivo.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE \_ ATRIBUTOS \_ DE** ESCRITURA (256 (0x100))


</dt> <dd>

Concede el derecho a cambiar los atributos de archivo.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))


</dt> <dd>

Concede acceso de eliminación.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**READ \_ CONTROL** (131072 (0x20000))


</dt> <dd>

Concede acceso de lectura al descriptor de seguridad y al propietario.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**ESCRITURA \_ DAC** (262144 (0x40000))


</dt> <dd>

Concede acceso de escritura a la lista de control de acceso discrecional (DACL).

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**ESCRITURA \_ OWNER** (524288 (0x80000))


</dt> <dd>

Asigna el propietario de escritura.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))


</dt> <dd>

Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **True** si el usuario tiene los permisos especificados y **false** si el usuario no tiene los permisos especificados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| Encabezado<br/>                   | <dl> <dt>Aclui.h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ ShortcutFile**](win32-shortcutfile.md)
</dt> </dl>

 

