---
description: El método de clase RESUME WMI continúa con un trabajo de impresión en pausa.
ms.assetid: acfbca2b-19af-4339-bbca-834db50c3d8d
ms.tgt_platform: multiple
title: Método Resume de la clase Win32_PrintJob reanudación
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8ca1602eb29e1e18d83d2e8b79760d13f63e101
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892537"
---
# <a name="resume-method-of-the-win32_printjob-class"></a>Método Resume de la clase PrintJob de Win32 \_

El **método de** clase RESUME [WMI](/windows/desktop/WmiSdk/retrieving-a-class) continúa con un trabajo de impresión en pausa.

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Resume();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.

<dl> <dt>

**0**
</dt> <dd>

Correcto

</dd> <dt>

**5**
</dt> <dd>

Acceso denegado

</dd> </dl>

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código VBScript reanuda todos los trabajos de impresión en un equipo.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Resume 
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

[**PrintJob de Win32 \_**](win32-printjob.md)
</dt> </dl>

 

