---
description: SetDateTime&\# 8194; El método de clase WMI establece la hora actual del sistema en el equipo.
ms.assetid: b9b86a52-c3d7-489d-8632-b297970dbeac
ms.tgt_platform: multiple
title: Método SetDateTime de la clase Win32_OperatingSystem
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659392"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a>Método SetDateTime de la \_ clase Win32 OperatingSystem

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDateTime** establece la hora actual del sistema en el equipo.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetDateTime(
  [in] datetime LocalDatetime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LocalDatetime* \[ de\]
</dt> <dd>

Valor de la hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que la operación se ha realizado correctamente. Cualquier otro número indica que hubo un error. Para ver los códigos de error, consulte [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otro** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El proceso de llamada debe tener el \_ privilegio de nombre SYSTEMTIME de se \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**OperatingSystem de Win32 \_**](win32-operatingsystem.md)
</dt> <dt>

[Tareas WMI: administración de escritorio](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

