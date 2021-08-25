---
description: 'Método GetAccessMask de la clase Win32_Share: devuelve un mapa de bits uint32 con los derechos de acceso al recurso compartido que mantiene el usuario o grupo en cuyo nombre se devuelve la instancia.'
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Método GetAccessMask de la Win32_Share clase
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
ms.openlocfilehash: ebc2b2620b0bdc019e117f9a4b2c376be6320be968fdae42509dc3f62c3cc9a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077665"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a>Método GetAccessMask de la clase Win32 \_ Share

El **método GetAccessMask** devuelve un mapa de bits uint32 con los derechos de acceso al recurso compartido que mantiene el usuario o grupo en cuyo nombre se devuelve la instancia.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Derechos de acceso al recurso compartido que mantiene el usuario o grupo.

<dl> <dt>

**DIRECTORIO DE \_ LISTA DE \_ ARCHIVOS**
</dt> <dd>

1 (0x1)

Concede el derecho a leer datos del archivo. Para un directorio, este valor concede el derecho a enumerar el contenido del directorio.

</dd> <dt>

**FILE \_ ADD \_ FILE**
</dt> <dd>

2 (0x2)

Concede el derecho de escribir datos en el archivo. Para un directorio, este valor concede el derecho de crear un archivo en el directorio.

</dd> <dt>

**SUBDIRECTORIO \_ FILE ADD \_**
</dt> <dd>

4 (0x4)

Concede el derecho a anexar datos al archivo. Para un directorio, este valor concede el derecho a crear un subdirectorio.

</dd> <dt>

**EA \_ DE LECTURA DE \_ ARCHIVOS**
</dt> <dd>

8 (0x8)

Concede el derecho a leer atributos extendidos.

</dd> <dt>

**EA DE \_ ESCRITURA \_ DE ARCHIVOS**
</dt> <dd>

16 (0x10)

Concede el derecho a escribir atributos extendidos.

</dd> <dt>

**RECORRIDO DE \_ ARCHIVOS**
</dt> <dd>

32 (0x20)

Concede el derecho a ejecutar un archivo. Para un directorio, se puede recorrer el directorio.

</dd> <dt>

**FILE \_ DELETE \_ CHILD**
</dt> <dd>

64 (0x40)

Concede el derecho a eliminar un directorio y todos los archivos que contiene (sus elementos secundarios), incluso si los archivos son de solo lectura.

</dd> <dt>

**ATRIBUTOS DE \_ LECTURA \_ DE ARCHIVOS**
</dt> <dd>

128 (0x80)

Concede el derecho a leer atributos de archivo.

</dd> <dt>

**ATRIBUTOS DE \_ ESCRITURA \_ DE ARCHIVOS**
</dt> <dd>

256 (0x100)

Concede el derecho a cambiar los atributos de archivo.

</dd> <dt>

**DELETE**
</dt> <dd>

65536 (0x10000)

Concede acceso de eliminación.

</dd> <dt>

**CONTROL DE \_ LECTURA**
</dt> <dd>

131072 (0x20000)

Concede acceso de lectura al descriptor de seguridad y al propietario.

</dd> <dt>

**ESCRIBIR \_ DAC**
</dt> <dd>

262144 (0x40000)

Concede acceso de escritura a la lista de control de acceso discrecional (DACL).

</dd> <dt>

**PROPIETARIO \_ DE ESCRITURA**
</dt> <dd>

524288 (0x80000)

Asigna el propietario de escritura.

</dd> <dt>

**Sincronizar**
</dt> <dd>

1048576 (0x100000)

Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**El método GetAccessMask** es un método de objeto y se usa en una aparición de esta clase.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se crea una carpeta de recurso compartido y, a continuación, se obtiene el valor de la máscara de acceso en el descriptor de seguridad que protege la carpeta del recurso compartido.


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Recurso compartido de \_ Win32**](win32-share.md)
</dt> </dl>

 

