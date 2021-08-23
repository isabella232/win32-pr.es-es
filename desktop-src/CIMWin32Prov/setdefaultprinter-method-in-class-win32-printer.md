---
description: El método de clase WMI SetDefaultPrinter establece la impresora del sistema predeterminada para el usuario que llama al método .
ms.assetid: 7e896961-363d-4b8b-9d22-bbfc9681e97b
ms.tgt_platform: multiple
title: Método SetDefaultPrinter de la Win32_Printer predeterminada
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetDefaultPrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d896fe76946881ebbc52591da1bfce1fbc0fb99ce4adfb02418aa35b912f0e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440185"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a>Método SetDefaultPrinter de la clase Printer de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultPrinter** establece la impresora del sistema predeterminada para el usuario que llama al método .

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si se realiza correctamente y otro valor si se produce un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

## <a name="examples"></a>Ejemplos

El ejemplo Instalar un puerto de impresora [TCP/IP](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) e impresora VBScript instala un puerto de impresora TCP/IP, instala una impresora y, a continuación, establece la impresora como predeterminada.

El siguiente ejemplo de código VBScript establece la impresora predeterminada en un equipo.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'ScriptedPrinter'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.SetDefaultPrinter() 
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> <dt>

[Tareas wmi: impresoras e impresión](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[**Impresora \_ Win32**](win32-printer.md)
</dt> </dl>

 

