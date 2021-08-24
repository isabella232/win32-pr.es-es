---
description: Crea un nuevo controlador de impresora.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Método AddPrinterDriver de la Win32_PrinterDriver clase
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
ms.openlocfilehash: 14681c381f8c8b9abbc5b28ec763b959854e2303b9a0b87af762238f4e5a8d27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752805"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a>Método AddPrinterDriver de la clase \_ PrinterDriver de Win32

El **método de clase AddPrinterDriver** crea un nuevo controlador de impresora.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DriverInfo* \[ En\]
</dt> <dd>

Instancia de la [**clase \_ PrinterDriver win32**](win32-printerdriver.md) que representa el controlador de impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para obtener valores diferentes de los enumerados en la lista siguiente, vea [**Constantes de error wmi**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Correcto.

</dd> <dt>

**5**
</dt> <dd>

Acceso denegado:

</dd> <dt>

**87**
</dt> <dd>

El parámetro no es correcto. Puede producirse cuando el objeto no se rellena correctamente o cuando no se encuentra el controlador en el sistema. Como alternativa, el atributo name puede ser diferente del modelo especificado en el archivo .inf. O bien, puede que falte una barra diagonal inversa (" \\ ") en un atributo PathFile.

</dd> <dt>

**1797**
</dt> <dd>

Se desconoce el controlador de impresora.

</dd> </dl>

## <a name="remarks"></a>Comentarios

> [!Note]  
> Al usar el **método AddPrinterDriver,** debe usar **SeLoadDriverPrivilege** para cargar o descargar un controlador de dispositivo.

 

## <a name="examples"></a>Ejemplos

El[ejemplo de código](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) Instalar un controlador de impresora no encontrado en el cab de controladores VBScript instala una impresora hipotética con un controlador de impresión que no se encuentra en Drivers.cab.

En el ejemplo de VBScript siguiente se instala el controlador de impresora para una impresora AppleWriter 8500.


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

