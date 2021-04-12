---
description: Crea un nuevo controlador de impresora.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Método AddPrinterDriver de la clase Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423235"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a>Método AddPrinterDriver de la \_ clase PrinterDriver de Win32

El método de la clase **AddPrinterDriver** crea un nuevo controlador de impresora.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DriverInfo* \[ de\]
</dt> <dd>

Instancia de la clase [**Win32 \_ PrinterDriver**](win32-printerdriver.md) que representa el controlador de impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para valores distintos de los que aparecen en la lista siguiente, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Correcto.

</dd> <dt>

**5**
</dt> <dd>

Acceso denegado.

</dd> <dt>

**87**
</dt> <dd>

El parámetro no es correcto. Puede producirse cuando el objeto no se rellena correctamente o cuando no se puede encontrar el controlador en el sistema. Como alternativa, el atributo name puede ser diferente del modelo especificado en el archivo. inf. O bien, es posible que falte una barra diagonal inversa (" \\ ") en un atributo PathFile.

</dd> <dt>

**1797**
</dt> <dd>

Se desconoce el controlador de impresora.

</dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> Al usar el método **AddPrinterDriver** , debe usar **SeLoadDriverPrivilege** para cargar o descargar un controlador de dispositivo.

 

## <a name="examples"></a>Ejemplos

El ejemplo de código[instalar un controlador de impresora no encontrado en el archivo. cab VBScript de los controladores](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) instala una impresora hipotética con un controlador de impresión no encontrado en Drivers.cab.

En el siguiente ejemplo de VBScript se instala el controlador de impresora para una impresora Apple LaserWriter 8500.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ printer. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

