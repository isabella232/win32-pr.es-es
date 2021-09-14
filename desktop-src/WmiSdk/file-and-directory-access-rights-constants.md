---
description: Las clases WMI que representan archivos o directorios, como Win32 CodecFile o \_ CIM \_ DataFile, contienen una propiedad AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Constantes de derechos de acceso a archivos y directorios (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965295"
---
# <a name="file-and-directory-access-rights-constants"></a>Constantes de derechos de acceso a archivos y directorios

Las clases WMI que representan archivos o directorios, como [**Win32 \_ CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) o [**CIM \_ DataFile,**](/windows/desktop/CIMWin32Prov/cim-datafile)contienen una **propiedad AccessMask.** Esta propiedad contiene valores de bits que especifican los derechos de acceso que un usuario o grupo debe tener para el acceso o las operaciones específicas en el archivo. Para obtener más información, vea [Derechos de acceso y seguridad de archivos](/windows/desktop/FileIO/file-security-and-access-rights) y Cambio de la seguridad de acceso en objetos [protegibles.](changing-access-security-on-securable-objects.md)

Las clases de archivo o directorio que contienen una **propiedad AccessMask** incluyen:

-   [**Archivo de datos CIM \_**](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [**Directorio \_ CIM**](/windows/desktop/CIMWin32Prov/cim-directory)
-   [**CIM \_ LogicalFile**](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [**CódecFile de \_ Win32**](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [**Directorio \_ win32**](/windows/desktop/CIMWin32Prov/win32-directory)
-   [**Win32 \_ NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))
-   [**Recurso compartido de \_ Win32**](/windows/desktop/CIMWin32Prov/win32-share)
-   [**Win32 \_ ShortcutFile**](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

En la lista siguiente se enumeran los valores de los derechos de acceso a archivos y directorios en la **propiedad AccessMask.** Esta propiedad es un mapa de bits.

<dl> <dt>

<span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**DATOS DE \_ LECTURA DE \_ ARCHIVOS**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede el derecho de leer datos del archivo.


</dt> </dl> </dd> <dt>

<span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**DIRECTORIO DE \_ LISTA DE \_ ARCHIVOS**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede el derecho de leer datos del archivo. Para un directorio, este valor concede el derecho de enumerar el contenido del directorio.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**DATOS DE \_ ESCRITURA \_ DE ARCHIVOS**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Concede el derecho de escribir datos en el archivo.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**FILE \_ ADD \_ FILE**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Concede el derecho de escribir datos en el archivo. Para un directorio, este valor concede el derecho de crear un archivo en el directorio.


</dt> </dl> </dd> <dt>

<span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**DATOS \_ ANEXADOS DE \_ ARCHIVO**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede el derecho a anexar datos al archivo. Para un directorio, este valor concede el derecho a crear un subdirectorio.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**SUBDIRECTORIO \_ FILE ADD \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede el derecho a anexar datos al archivo. Para un directorio, este valor concede el derecho a crear un subdirectorio.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE \_ READ \_ EA**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Concede el derecho de leer atributos extendidos.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE \_ WRITE \_ EA**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Concede el derecho a escribir atributos extendidos.


</dt> </dl> </dd> <dt>

<span id="FILE_EXECUTE"></span><span id="file_execute"></span>**FILE \_ EXECUTE**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede el derecho a ejecutar un archivo.


</dt> </dl> </dd> <dt>

<span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**RECORRIDO DE \_ ARCHIVOS**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede el derecho a ejecutar un archivo. Para un directorio, se puede recorrer el directorio.


</dt> </dl> </dd> <dt>

<span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**ELIMINACIÓN \_ DE \_ ARCHIVOS SECUNDARIO**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Concede el derecho a eliminar un directorio y todos los archivos que contiene (sus elementos secundarios), incluso si los archivos son de solo lectura.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**ATRIBUTOS DE \_ LECTURA \_ DE ARCHIVO**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Concede el derecho a leer atributos de archivo.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**ATRIBUTOS DE \_ ESCRITURA \_ DE ARCHIVOS**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Concede el derecho a cambiar los atributos de archivo.


</dt> </dl> </dd> <dt>

<span id="DELETE"></span><span id="delete"></span>**ELIMINAR**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Concede el derecho para eliminar el objeto.


</dt> </dl> </dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>**CONTROL DE \_ LECTURA**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Concede el derecho a leer la información en el descriptor de seguridad del objeto, sin incluir la información en la SACL.


</dt> </dl> </dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**ESCRIBIR \_ DAC**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Concede el derecho a modificar la DACL en el descriptor de seguridad del objeto para el objeto.


</dt> </dl> </dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**PROPIETARIO DE \_ ESCRITURA**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Concede el derecho a cambiar el propietario en el descriptor de seguridad del objeto.


</dt> </dl> </dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SINCRONIZAR**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Concede el derecho a usar el objeto para la sincronización. Esto permite que un proceso espere hasta que el objeto esté en estado señalado. Algunos tipos de objeto no admiten este derecho de acceso.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de seguridad wmi](wmi-security-constants.md)
</dt> <dt>

[Mantener la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

