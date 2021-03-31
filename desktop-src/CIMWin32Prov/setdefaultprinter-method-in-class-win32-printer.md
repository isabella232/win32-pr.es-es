---
description: El método de clase WMI SetDefaultPrinter establece la impresora predeterminada del sistema para el usuario que llama al método.
ms.assetid: 7e896961-363d-4b8b-9d22-bbfc9681e97b
ms.tgt_platform: multiple
title: Método SetDefaultPrinter de la clase Win32_Printer
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
ms.openlocfilehash: a18c6d7771eb0e95d86142f41262d721509eb6f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907535"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a>Método SetDefaultPrinter de la \_ clase Printer de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultPrinter** establece la impresora predeterminada del sistema para el usuario que llama al método.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si es correcto y otro valor si se produce un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

## <a name="examples"></a>Ejemplos

El ejemplo [instalar un puerto de impresora TCP/IP y una impresora](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) de VBScript instala un puerto de impresora TCP/IP, instala una impresora y, a continuación, establece la impresora como predeterminada.

En el siguiente ejemplo de código de VBScript se establece la impresora predeterminada en un equipo.


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

 

