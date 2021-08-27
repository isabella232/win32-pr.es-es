---
description: Cambia el nombre del archivo de entrada de directorio especificado en la ruta de acceso del objeto.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Método Rename de la Win32_Directory clase
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
ms.openlocfilehash: 86b6bd35b14ee2a342dee27615c1ff21d9274a5f3020c4f804df5065f430813f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077445"
---
# <a name="rename-method-of-the-win32_directory-class"></a>Método Rename de la clase Directory de \_ Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Rename** cambia el nombre del archivo de entrada de directorio especificado en la ruta de acceso del objeto. No se admite un cambio de nombre si el destino está en otra unidad o si se requiere sobrescribir un archivo lógico existente.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

Nombre nuevo completo del archivo (o directorio). Ejemplo: c: \\ temp \\newfile.txt.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el nombre del archivo se ha cambiado correctamente y cualquier otro número para indicar un error.

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

Ha habido una infracción de uso compartido.

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

## <a name="remarks"></a>Comentarios

Para cambiar el nombre de una carpeta, primero enlace a la carpeta en cuestión y, a continuación, llame al método Rename. Como único parámetro para el método , pase el nuevo nombre de la carpeta como un nombre de ruta de acceso completo. Por ejemplo, si se va a cambiar el nombre de la carpeta de la copia de seguridad de registros de C: Scripts a C: Archivo de scripts, debe pasar C: Archivo de scripts como nombre \\ \\ completo de la \\ \\ \\ \\ \\ carpeta. Al pasar solo el nombre de la carpeta - Archivo - , se produce un error de ruta de acceso no válida.

La clase Directory de Win32 \_ no proporciona un método de un paso para mover carpetas. En su lugar, mover una carpeta suele implicar dos pasos:

<dl> 1. Copia de la carpeta en su nueva ubicación  
2. Eliminación de la carpeta original  
</dl>

La única excepción a este proceso de dos pasos implica mover una carpeta a una nueva ubicación en la misma unidad. Por ejemplo, supongamos que desea mover C: \\ Temp a C: \\ Scripts Temporary \\ Files \\ Archive. Siempre que la ubicación actual y la nueva ubicación estén en la misma unidad, puede mover la carpeta simplemente llamando al método Rename y pasando la nueva ubicación como parámetro de método. Este enfoque le permite mover la carpeta de forma eficaz en un solo paso. Sin embargo, se produce un error en el script si la unidad actual y la nueva unidad son diferentes. Un intento de cambiar el nombre de C: Temp a D: Temp produce un \\ error \\ "Drive not the same" (Unidad no es la misma).

## <a name="examples"></a>Ejemplos

En el código siguiente, del ejemplo Mover una carpeta mediante [VBScript wmi](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) de la Galería de TechNet, se usa el método Rename para mover la carpeta C: Scripts a C: Archivos de documentos de administrador \\ \\ \\ \\ \\ VBScript.


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



| Requisito | Valor |
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

[**Directorio \_ Win32**](win32-directory.md)
</dt> </dl>

 

