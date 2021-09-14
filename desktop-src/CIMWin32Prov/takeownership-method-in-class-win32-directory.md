---
description: 'Método TakeOwnerShip de la clase Win32_Directory : el método de clase WMI TakeOwnerShip obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.'
ms.assetid: 1112823b-0bb6-4dc0-a5c4-8d3839a47a3a
ms.tgt_platform: multiple
title: Método TakeOwnerShip de la Win32_Directory clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 178f1bf523d939883a7fc18b5bdbd7142cc4f824
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062269"
---
# <a name="takeownership-method-of-the-win32_directory-class"></a>Método TakeOwnerShip de la clase Directory de \_ Win32

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto. Si el archivo lógico es realmente un directorio, **TakeOwnerShip** actúa de forma recursiva, tomando posesión de todos los archivos y subdirectorios que contiene el directorio.

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.

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

## <a name="examples"></a>Ejemplos

El siguiente Visual Basic script llama al [**método TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) para tomar posesión de la carpeta \\ temporal C:.


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
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

[**Directorio \_ Win32**](win32-directory.md)
</dt> </dl>

 

