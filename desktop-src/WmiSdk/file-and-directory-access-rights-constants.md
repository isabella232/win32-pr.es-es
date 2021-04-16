---
description: Las clases WMI que representan archivos o directorios, como \_ CodecFile de Win32 o \_ archivo de información CIM, contienen una propiedad AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Constantes de derechos de acceso a archivos y directorios (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708249"
---
# <a name="file-and-directory-access-rights-constants"></a>Constantes de derechos de acceso a archivos y directorios

Las clases WMI que representan archivos o directorios, como [**\_ CodecFile de Win32**](/windows/desktop/CIMWin32Prov/win32-codecfile) o [**\_ archivo**](/windows/desktop/CIMWin32Prov/cim-datafile)de información CIM, contienen una propiedad **AccessMask** . Esta propiedad contiene valores de bit que especifican los derechos de acceso que debe tener un usuario o grupo para las operaciones o el acceso específico en el archivo. Para obtener más información, consulte [derechos de acceso y seguridad de archivos](/windows/desktop/FileIO/file-security-and-access-rights) y cambiar la [seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).

Las clases de archivo o directorio que contienen una propiedad **AccessMask** incluyen:

-   [**\_Archivo de archivos CIM**](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [**\_Directorio CIM**](/windows/desktop/CIMWin32Prov/cim-directory)
-   [**\_LOGICALFILE CIM**](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [**Win32 \_ CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [**\_Directorio Win32**](/windows/desktop/CIMWin32Prov/win32-directory)
-   [**Win32 \_ NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))
-   [**\_Recurso compartido de Win32**](/windows/desktop/CIMWin32Prov/win32-share)
-   [**Win32 \_ ShortcutFile**](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

En la lista siguiente se enumeran los valores de los derechos de acceso a archivos y directorios en la propiedad **AccessMask** . Esta propiedad es un mapa de bits.

<dl> <dt>

<span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**\_datos de lectura de archivos \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede el derecho a leer los datos del archivo.


</dt> </dl> </dd> <dt>

<span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**directorio de la lista de archivos \_ \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede el derecho a leer los datos del archivo. Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**\_datos de escritura de archivo \_**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Concede el derecho para escribir datos en el archivo.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**ARCHIVO \_ agregar \_ archivo**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Concede el derecho para escribir datos en el archivo. Para un directorio, este valor concede el derecho a crear un archivo en el directorio.


</dt> </dl> </dd> <dt>

<span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**ARCHIVO \_ de \_ datos anexados**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede el derecho para anexar datos al archivo. Para un directorio, este valor concede el derecho a crear un subdirectorio.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**\_agregar \_ subdirectorio de archivo**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede el derecho para anexar datos al archivo. Para un directorio, este valor concede el derecho a crear un subdirectorio.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**ARCHIVO de \_ lectura \_ EA**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Concede el derecho para leer atributos extendidos.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**escritura de archivo \_ \_ EA**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Concede el derecho para escribir atributos extendidos.


</dt> </dl> </dd> <dt>

<span id="FILE_EXECUTE"></span><span id="file_execute"></span>**\_Ejecutar archivo**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede el derecho para ejecutar un archivo.


</dt> </dl> </dd> <dt>

<span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**recorrido de archivos \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede el derecho para ejecutar un archivo. Para un directorio, se puede atravesar el directorio.


</dt> </dl> </dd> <dt>

<span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**ARCHIVO- \_ eliminar \_ secundario**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Concede el derecho para eliminar un directorio y todos los archivos que contiene (sus elementos secundarios), incluso si los archivos son de solo lectura.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**\_atributos de lectura de archivo \_**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Concede el derecho a leer los atributos de archivo.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**\_atributos de escritura de archivo \_**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Concede el derecho para cambiar los atributos de archivo.


</dt> </dl> </dd> <dt>

<span id="DELETE"></span><span id="delete"></span>**ELIMÍNELOS**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Concede el derecho para eliminar el objeto.


</dt> </dl> </dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>**CONTROL de lectura \_**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Concede el derecho para leer la información del descriptor de seguridad del objeto, sin incluir la información en la SACL.


</dt> </dl> </dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**ESCRIBIR \_ DAC**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Concede el derecho a modificar la DACL en el descriptor de seguridad del objeto para el objeto.


</dt> </dl> </dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**propietario de escritura \_**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Concede el derecho a cambiar el propietario del descriptor de seguridad para el objeto.


</dt> </dl> </dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SINCRONIZÁNDOSE**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Concede el derecho a usar el objeto para la sincronización. Esto permite que un proceso espere hasta que el objeto esté en el estado señalado. Algunos tipos de objetos no admiten este derecho de acceso.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de seguridad de WMI](wmi-security-constants.md)
</dt> <dt>

[Mantenimiento de la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

