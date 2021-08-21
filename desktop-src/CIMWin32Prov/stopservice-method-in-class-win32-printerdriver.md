---
description: Coloca el servicio representado por el objeto PrinterDriver de Win32 \_ en estado detenido.
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: Método StopService de la Win32_PrinterDriver (Sdoias.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0ec49d6f5b9c7efcb860ba99eaf7984fa89cfb0bc12cbdfcfe8bde0db95eff1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020403"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a>Método StopService de la clase \_ PrinterDriver de Win32

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca el servicio representado por el objeto [**\_ PrinterDriver de Win32**](win32-printerdriver.md) en estado detenido.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para obtener valores diferentes de los enumerados en la lista siguiente, vea [**Constantes de error wmi**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Servicio detenido correctamente.

</dd> <dt>

**1**
</dt> <dd>

Solicitud no admitida.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                        |
| Header<br/>                   | <dl> <dt>Sdoias.h</dt> </dl>           |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

