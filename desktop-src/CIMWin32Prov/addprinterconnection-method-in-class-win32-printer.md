---
description: Proporciona una conexión a una impresora existente en la red y la agrega a la lista de impresoras disponibles.
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: Método AddPrinterConnection de la clase Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2ad9e225a60e33fdf51d5f677dd4342acd148b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907052"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a>Método AddPrinterConnection de la \_ clase Printer de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AddPrinterConnection** proporciona una conexión a una impresora existente en la red y la agrega a la lista de impresoras disponibles.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ de de\]
</dt> <dd>

Nombre descriptivo de la impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Correcto

</dd> <dt>

**5**
</dt> <dd>

Acceso denegado

</dd> <dt>

**1801**
</dt> <dd>

Nombre de impresora no válido

</dd> <dt>

**1930**
</dt> <dd>

Controlador de impresora incompatible

</dd> </dl>

## <a name="examples"></a>Ejemplos

El ejemplo de PowerShell [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) instala todos los controladores de impresora desde un servidor de impresión especificado.

En el ejemplo de PowerShell de [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) se enumeran las impresoras compartidas de un equipo remoto y se ofrece la posibilidad de agregar una conexión de impresora desde el equipo remoto al equipo.

El siguiente ejemplo de código de VBScript agrega una impresora local.


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
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

[Tareas de WMI: impresoras e impresión](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[**\_Impresora Win32**](win32-printer.md)
</dt> </dl>

 

