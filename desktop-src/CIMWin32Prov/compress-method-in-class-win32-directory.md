---
description: Comprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Método Compress de la Win32_Directory clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968863"
---
# <a name="compress-method-of-the-win32_directory-class"></a>Método Compress de la clase Directory de \_ Win32

El **método comprimir** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) comprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto.

En este tema se Managed Object Format sintaxis de MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Compress();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el archivo se comprimió correctamente y cualquier otro número para indicar un error.

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

Error no especificado.

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

La plataforma no está Windows.

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

Se ha infringido el uso compartido.

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

La compresión proporciona una manera de liberar espacio de almacenamiento adicional en una unidad de disco sin adquirir hardware nuevo y sin quitar archivos o carpetas. Según el tamaño del disco duro y el tipo de archivos almacenados en ese disco, es posible que pueda recuperar cientos de megabytes de espacio en disco y, por tanto, impedir la necesidad de adquirir una nueva unidad de disco duro y desconectar el equipo hasta que se instale la nueva unidad.

El método Compress comprime todos los archivos y subcarpetas dentro de una carpeta especificada. Además, la clase también incluye un método Uncompress que quita la compresión de todos los archivos y subcarpetas de una carpeta. También se proporcionan métodos similares con la clase \_ de archivo de datos CIM. Esto le permite comprimir o descomprimir de forma selectiva archivos específicos dentro de una carpeta.

Dado que la compresión presenta una ligera reducción del rendimiento, no se recomienda para los archivos o carpetas a los que se accede de forma rutinaria; Por ejemplo, es probable que no quiera comprimir archivos de base de datos, archivos de registro o carpetas de perfil de usuario. Los mejores candidatos para la compresión son archivos y carpetas a los que no se accede con mucha frecuencia. Por ejemplo, podría escribir un script para devolver una colección de carpetas en una unidad a la que no se ha accedido durante un mes o más y, a continuación, comprimir cada una de esas carpetas.

La cantidad de espacio en disco liberada mediante la compresión de carpetas varía en función del tipo de archivos almacenados en esa carpeta. Por ejemplo, .jpg archivos ya están comprimidos y la compresión adicional tiene poco efecto en el tamaño del archivo. Sin embargo, con otros tipos de archivo, el ahorro puede ser considerable. Por ejemplo, se creó una nueva carpeta en un equipo de prueba basado en Windows 2000 y se copiaron en esa carpeta 33 documentos Microsoft Word, que suman un total de 15 megabytes (MB) de espacio en disco. Cuando se comprimían los documentos, la carpeta solo tenía 7 MB de espacio en disco.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de VBScript comprime la carpeta C: \\ Scripts.


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Directorio \_ win32**](win32-directory.md)
</dt> <dt>

[**Descomprimir**](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

