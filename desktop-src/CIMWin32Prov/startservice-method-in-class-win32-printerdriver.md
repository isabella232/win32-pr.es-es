---
description: El método StartService coloca el servicio en el estado iniciado.
ms.assetid: 0f221db1-29ad-4071-98d3-6d06e4f5e026
ms.tgt_platform: multiple
title: Método StartService de la Win32_PrinterDriver clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe5afb79f2c5d74f2e9a68093cb98ac0b8597d767a747c8bd66b766ba72dd00f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752385"
---
# <a name="startservice-method-of-the-win32_printerdriver-class"></a>Método StartService de la clase \_ PrinterDriver de Win32

El **método StartService** coloca el servicio en el estado iniciado.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para obtener valores diferentes de los enumerados en la lista siguiente, vea [**Constantes de error wmi**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Servicio iniciado correctamente.

</dd> <dt>

**1**
</dt> <dd>

Solicitud no admitida.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

