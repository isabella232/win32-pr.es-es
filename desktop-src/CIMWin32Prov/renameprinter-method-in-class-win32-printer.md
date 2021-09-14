---
description: Cambia el nombre de una impresora.
ms.assetid: afbef871-5153-4b9e-9ad3-4d271a497c37
ms.tgt_platform: multiple
title: Método RenamePrinter de la Win32_Printer clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.RenamePrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6066dfd4280f7c43c9804933fb1ed5fb931bfa08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062649"
---
# <a name="renameprinter-method-of-the-win32_printer-class"></a>Método RenamePrinter de la clase Printer de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenamePrinter** cambia el nombre de una impresora.

En este tema se Managed Object Format sintaxis de MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 RenamePrinter(
  [in] string NewPrinterName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewPrinterName* \[ En\]
</dt> <dd>

Nuevo nombre de impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

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

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo de VBScript siguiente se cambia el nombre de una impresora y su nombre compartido de impresora.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where DeviceID = 'HP LaserJet 4Si M'") 
 
For Each objPrinter in colPrinters 
    objPrinter.RenamePrinter("ArtDepartmentPrinter") 
Next 
 
Set colPrinters = objWMIService.ExecQuery _ 
    ("Select * From Win32_Printer Where DeviceID = 'ArtDepartmentPrinter' ") 
 
For Each objPrinter in colPrinters 
    objPrinter.ShareName = "ArtDepartmentPrinter" 
    objPrinter.Put_ 
Next 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> <dt>

[**Impresora \_ Win32**](win32-printer.md)
</dt> </dl>

 

