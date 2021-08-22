---
description: El método de clase WMI Delete eliminará el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: 5663b8a8-3089-475b-8a36-454a7315bfca
ms.tgt_platform: multiple
title: Método Delete de la Win32_Directory clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2966751c822213025d7107e4eff055900e6c8102711b66329e6f3c4fcbe1ed02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676701"
---
# <a name="delete-method-of-the-win32_directory-class"></a>Método Delete de la clase De directorio \_ win32

El **método de** clase WMI [Delete](/windows/desktop/WmiSdk/retrieving-a-class) eliminará el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.

En este tema se Managed Object Format sintaxis de MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el archivo se eliminó correctamente y cualquier otro número para indicar un error.

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

Las carpetas no son necesariamente adiciones permanentes a un sistema de archivos. En algún momento, es posible que sea necesario eliminar las carpetas, quizás porque ya no son necesarias, porque el rol del equipo ha cambiado o porque las carpetas se crearon por error.

Eliminar le permite eliminar carpetas: simplemente se enlaza a la carpeta en cuestión y, a continuación, se llama al método Delete. Después de llamar al método Delete, la carpeta se quita permanentemente del sistema de archivos; no se envía al papelera de reciclaje. Además, no se emite ningún aviso de confirmación ("¿está seguro de que desea eliminar esta carpeta?"). En su lugar, la carpeta se quita inmediatamente.

No se pueden eliminar carpetas de solo lectura mediante FileSystemObject; sin embargo, esto se puede hacer mediante WMI. Si el script usa WMI y no desea quitar una carpeta de solo lectura, debe usar la propiedad Legible para comprobar el estado de la carpeta antes de eliminarla.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código VBScript elimina la carpeta C: \\ Scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Delete
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Directorio \_ win32**](win32-directory.md)
</dt> </dl>

 

