---
description: Obtiene la propiedad del archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto. Este método es una versión extendida del método TakeOwnerShip.
ms.assetid: 73726207-e885-4957-bff8-6903c4b99278
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e391e942e581d0f80d46b0f59b9b273d7bff499
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659360"
---
# <a name="takeownershipex-method-of-the-win32_directory-class"></a>Método TakeOwnerShipEx de la \_ clase de directorio Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** obtiene la propiedad del archivo de entrada de directorio lógico especificado en la ruta de acceso del objeto. Este método es una versión extendida del método [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) . Si el archivo lógico es realmente un directorio, este método actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StopFileName* \[ enuncia\]
</dt> <dd>

Nombre del archivo o directorio en el que se produjo un error en el método **TakeOwnerShipEx** . Este parámetro es **null** si el método se ejecuta correctamente.

</dd> <dt>

*StartFileName* \[ en, opcional\]
</dt> <dd>

Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **TakeOwnerShipEx**. El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior. Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) .

Si se utiliza *StartFileName* , *Recursive* también debe establecerse en true.

</dd> <dt>

*Recursivo* \[ en, opcional\]
</dt> <dd>

Si es **true**, el cambio de propiedad se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .

> [!Note]  
> En el caso de las instancias de archivo, se omite el parámetro de entrada *recursivo* .

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.

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

## <a name="examples"></a>Ejemplos

El siguiente código de script de Visual Basic llama al método [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) para tomar posesión de la \\ carpeta C: Temp.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx").inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod("Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
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

 

