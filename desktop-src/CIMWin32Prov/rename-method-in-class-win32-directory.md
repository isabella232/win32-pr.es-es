---
description: Cambia el nombre del archivo de entrada de directorio especificado en la ruta de acceso del objeto.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Cambiar el nombre del método de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 874151e1ff8c9feca375df3eb441665863d1070d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659326"
---
# <a name="rename-method-of-the-win32_directory-class"></a>Cambiar el nombre del método de la \_ clase de directorio Win32

El método **Rename** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cambia el nombre del archivo de entrada de directorio especificado en la ruta de acceso del objeto. No se admite el cambio de nombre si el destino está en otra unidad o si se requiere sobrescribir un archivo lógico existente.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, vea [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileName* 
</dt> <dd>

Nuevo nombre completo del archivo (o directorio). Ejemplo: c: \\ temp \\newfile.txt.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se cambió el nombre del archivo correctamente y cualquier otro número para indicar un error.

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

Para cambiar el nombre de una carpeta, primero Enlace a la carpeta en cuestión y, a continuación, llame al método Rename. Como único parámetro del método, pase el nuevo nombre de la carpeta como un nombre de ruta de acceso completo. Por ejemplo, si la carpeta de la copia de \\ seguridad de registros c: scripts \\ se va a cambiar de nombre \\ c: \\ scripts \\ , debe pasar c: \\ scripts \\ Archive como el nombre completo de la carpeta. Al pasar solo el nombre de la carpeta-Archive, se produce un error de ruta de acceso no válido.

La clase de directorio Win32 no \_ proporciona un método de un solo paso para mover carpetas. En su lugar, mover una carpeta normalmente implica dos pasos:

<dl> 1. Copiar la carpeta en su nueva ubicación  
2. Eliminar la carpeta original  
</dl>

La única excepción a este proceso de dos pasos consiste en mover una carpeta a una nueva ubicación en la misma unidad. Por ejemplo, supongamos que desea trasladar C: \\ temp a c: \\ scripts \\ archivo de archivos temporales \\ . Siempre que la ubicación actual y la nueva ubicación estén en la misma unidad, puede mover la carpeta simplemente llamando al método Rename y pasando la nueva ubicación como parámetro de método. Este enfoque permite desplazar la carpeta en un solo paso. Sin embargo, se produce un error en el script si la unidad actual y la nueva unidad son diferentes. Se produce un error al intentar cambiar el nombre de C: \\ temp a D: \\ Temp con un error "la unidad no es el mismo".

## <a name="examples"></a>Ejemplos

En el código siguiente, en el ejemplo de [migración de una carpeta mediante WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript en la galería de TechNet, se usa el método Rename para trasladar la carpeta c: \\ scripts a c: \\ documentos de Admins \\ \\ archivo \\ VBScript.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
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
</dt> </dl>

 

