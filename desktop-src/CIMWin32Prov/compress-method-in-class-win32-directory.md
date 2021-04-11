---
description: Comprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Método compress de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea694c09e11e5801016a4ea85b9774448c542991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152868"
---
# <a name="compress-method-of-the-win32_directory-class"></a>Método compress de la \_ clase de directorio Win32

El método **compress** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) comprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Compress();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el archivo se ha comprimido correctamente y cualquier otro número para indicar un error.

<dl> <dt>

**0**
</dt> <dd>

La solicitud fue correcta.

</dd> <dt>

**2**
</dt> <dd>

Se denegó el acceso.

</dd> <dt>

**8**
</dt> <dd>

Se produjo un error no especificado.

</dd> <dt>

**9**
</dt> <dd>

El nombre especificado no era válido.

</dd> <dt>

**10**
</dt> <dd>

El objeto especificado ya existe.

</dd> <dt>

**11**
</dt> <dd>

El sistema de archivos no es NTFS.

</dd> <dt>

**12**
</dt> <dd>

La plataforma no es Windows.

</dd> <dt>

**13**
</dt> <dd>

La unidad no es la misma.

</dd> <dt>

**14**
</dt> <dd>

El directorio no está vacío.

</dd> <dt>

**15**
</dt> <dd>

Se ha producido una infracción de uso compartido.

</dd> <dt>

**16**
</dt> <dd>

El archivo de inicio especificado no era válido.

</dd> <dt>

**17**
</dt> <dd>

No se mantiene un privilegio necesario para la operación.

</dd> <dt>

**21**
</dt> <dd>

Un parámetro especificado no es válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La compresión proporciona una forma de liberar espacio de almacenamiento adicional en una unidad de disco sin necesidad de adquirir hardware nuevo y sin quitar archivos o carpetas. En función del tamaño del disco duro y del tipo de archivos almacenados en ese disco, es posible que pueda recuperar cientos de megabytes de espacio en disco y, por lo tanto, no tenga que adquirir una nueva unidad de disco duro y dejar el equipo sin conexión hasta que se instale la nueva unidad.

El método compress comprime todos los archivos y subcarpetas de una carpeta especificada. Además, la clase también incluye un método UNCOMPRESS que quita la compresión de todos los archivos y subcarpetas de una carpeta. También se proporcionan métodos similares con la \_ clase de archivo de archivos CIM. Esto le permite comprimir o descomprimir archivos específicos de una carpeta de forma selectiva.

Dado que la compresión es una ligera disminución del rendimiento, no se recomienda para los archivos o carpetas a los que se tiene acceso de forma rutinaria. por ejemplo, es probable que no desee comprimir archivos de base de datos, archivos de registro o carpetas de perfiles de usuario. Los mejores candidatos para la compresión son los archivos y las carpetas a los que no se tiene acceso con mucha frecuencia. Por ejemplo, puede escribir un script para devolver una colección de carpetas de una unidad a la que no se ha accedido durante un mes o más y, a continuación, comprimir cada una de esas carpetas.

La cantidad de espacio en disco liberado por las carpetas de compresión varía en función del tipo de archivos almacenados en esa carpeta. Por ejemplo, los archivos. jpg ya están comprimidos y la compresión adicional tiene poco efecto en el tamaño del archivo. Con otros tipos de archivo, sin embargo, el ahorro puede ser considerable. Por ejemplo, se ha creado una nueva carpeta en un equipo de prueba basado en Windows 2000 y 33 documentos de Microsoft Word, con un total de 15 megabytes (MB) de espacio en disco, que se han copiado en esa carpeta. Cuando se comprimen los documentos, la carpeta solo tenía 7 MB de espacio en disco.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de VBScript comprime la carpeta C: \\ scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Directorio Win32**](win32-directory.md)
</dt> <dt>

[**Descomprimir**](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

