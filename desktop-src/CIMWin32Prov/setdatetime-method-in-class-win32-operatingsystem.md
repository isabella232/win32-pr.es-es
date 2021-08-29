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
ms.openlocfilehash: bbab7d9e599fb33fe999ac56eaba5f180895f7658d718cd524bc9685109ae2af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760145"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a>Método SetDateTime de la clase \_ OperatingSystem win32

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDateTime** establece la hora actual del sistema en el equipo.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

Devuelve cero (0) para indicar que se ha correcto. Cualquier otro número indica que hubo un error. Para obtener códigos de error, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otros** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentarios

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

 

