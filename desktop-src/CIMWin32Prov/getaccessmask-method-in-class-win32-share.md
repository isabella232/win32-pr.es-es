---
description: Devuelve un mapa de bits UInt32 con los derechos de acceso al recurso compartido mantenido por el usuario o grupo en cuyo nombre se devuelve la instancia.
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Método GetAccessMask de la clase Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 745ce6d607adf84827c14a588640572b5d92be00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998236"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a>Método GetAccessMask de la \_ clase de recursos compartidos de Win32

El método **GetAccessMask** devuelve un mapa de bits UInt32 con los derechos de acceso al recurso compartido mantenido por el usuario o grupo en cuyo nombre se devuelve la instancia.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Derechos de acceso al recurso compartido mantenido por el usuario o grupo.

<dl> <dt>

**directorio de la lista de archivos \_ \_**
</dt> <dd>

1 (0x1)

Concede el derecho a leer los datos del archivo. Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.

</dd> <dt>

**ARCHIVO \_ agregar \_ archivo**
</dt> <dd>

2 (0X2)

Concede el derecho para escribir datos en el archivo. Para un directorio, este valor concede el derecho a crear un archivo en el directorio.

</dd> <dt>

**\_agregar \_ subdirectorio de archivo**
</dt> <dd>

4 (0x4)

Concede el derecho para anexar datos al archivo. Para un directorio, este valor concede el derecho a crear un subdirectorio.

</dd> <dt>

**ARCHIVO de \_ lectura \_ EA**
</dt> <dd>

8 (0x8)

Concede el derecho para leer atributos extendidos.

</dd> <dt>

**escritura de archivo \_ \_ EA**
</dt> <dd>

16 (0x10)

Concede el derecho para escribir atributos extendidos.

</dd> <dt>

**recorrido de archivos \_**
</dt> <dd>

32 (0x20)

Concede el derecho para ejecutar un archivo. Para un directorio, se puede atravesar el directorio.

</dd> <dt>

**ARCHIVO- \_ eliminar \_ secundario**
</dt> <dd>

64 (0x40)

Concede el derecho para eliminar un directorio y todos los archivos que contiene (sus elementos secundarios), incluso si los archivos son de solo lectura.

</dd> <dt>

**\_atributos de lectura de archivo \_**
</dt> <dd>

128 (0x80)

Concede el derecho a leer los atributos de archivo.

</dd> <dt>

**\_atributos de escritura de archivo \_**
</dt> <dd>

256 (0x100)

Concede el derecho para cambiar los atributos de archivo.

</dd> <dt>

**DELETE**
</dt> <dd>

65536 (0x10000)

Concede acceso de eliminación.

</dd> <dt>

**CONTROL de lectura \_**
</dt> <dd>

131072 (0x20000)

Concede acceso de lectura al descriptor de seguridad y al propietario.

</dd> <dt>

**ESCRIBIR \_ DAC**
</dt> <dd>

262144 (0x40000)

Concede acceso de escritura a la lista de control de acceso discrecional (DACL).

</dd> <dt>

**propietario de escritura \_**
</dt> <dd>

524288 (0x80000)

Asigna el propietario de la escritura.

</dd> <dt>

**SYNCHRONIZE**
</dt> <dd>

1048576 (0x100000)

Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método **GetAccessMask** es un método de objeto y se usa en una aparición de esta clase.

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se crea una carpeta de recurso compartido y, a continuación, se obtiene el valor de la máscara de acceso en el descriptor de seguridad que protege la carpeta de recursos compartidos.


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
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

[**\_Recurso compartido de Win32**](win32-share.md)
</dt> </dl>

 

