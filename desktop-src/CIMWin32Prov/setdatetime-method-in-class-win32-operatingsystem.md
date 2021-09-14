---
description: SetDateTime&\# 8194; El método de clase WMI establece la hora actual del sistema en el equipo.
ms.assetid: b9b86a52-c3d7-489d-8632-b297970dbeac
ms.tgt_platform: multiple
title: Método SetDateTime de la Win32_OperatingSystem clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.SetDateTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60316904d58ffec38aa912a1454082e7edfae5a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174482"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a>Método SetDateTime de la clase OperatingSystem de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDateTime** establece la hora actual del sistema en el equipo.

En este tema se Managed Object Format sintaxis de MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetDateTime(
  [in] datetime LocalDatetime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LocalDatetime* \[ En\]
</dt> <dd>

Valor de la hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que se ha correcto. Cualquier otro número indica que hubo un error. Para obtener códigos de error, [**vea Constantes de error wmi**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otros** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El proceso de llamada debe tener el SE \_ SYSTEMTIME \_ NAME.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Sistema operativo \_ Win32**](win32-operatingsystem.md)
</dt> <dt>

[Tareas wmi: administración de escritorio](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

