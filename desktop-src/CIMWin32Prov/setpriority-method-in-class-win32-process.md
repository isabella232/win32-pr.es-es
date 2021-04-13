---
description: SetPriority&\# 32; El método de clase WMI intenta cambiar la prioridad de ejecución del proceso.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Método SetPriority de la clase Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf08057ec075448d9912e37c33b6087c381f97d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539261"
---
# <a name="setpriority-method-of-the-win32_process-class"></a>Método SetPriority de la \_ clase Process de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPriority** intenta cambiar la prioridad de ejecución del proceso.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Prioridad* \[ de de\]
</dt> <dd>

Nueva clase de prioridad para el proceso. Tenga en cuenta que estos valores son diferentes de los indicados explícitamente en la propiedad **Priority** del [**\_ proceso Win32**](win32-process.md).

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactivo** (64)


</dt> <dd>

Especificado para un proceso con subprocesos que se ejecutan solo cuando el sistema está inactivo. Los subprocesos del proceso son retenidos por los subprocesos de un proceso que se ejecutan en una clase de prioridad más alta, por ejemplo, un protector de pantalla. Los procesos secundarios heredan la clase de prioridad de inactividad.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Por debajo** de lo Normal (16384)


</dt> <dd>

Indica un proceso que tiene prioridad sobre **la \_ \_ clase de prioridad de inactividad**, pero por debajo de la **\_ \_ clase de prioridad normal**.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)


</dt> <dd>

Se especifica para un proceso sin necesidad de programación especial.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Por encima** de lo Normal (32768)


</dt> <dd>

Indica un proceso que tiene prioridad sobre **la \_ \_ clase de prioridad normal**, pero por debajo de la **\_ \_ clase de prioridad alta**.

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Prioridad alta** (128)


</dt> <dd>

Se especifica para un proceso que realiza tareas críticas en el tiempo que se deben ejecutar inmediatamente. Los subprocesos del proceso tienen prioridad sobre los subprocesos de aquellos procesos de clase de prioridad normal o inactiva. Un ejemplo es el Lista de tareas, que debe responder rápidamente cuando el usuario lo llama, independientemente de la carga del sistema operativo. Extreme las precauciones al usar la clase de prioridad alta, ya que una aplicación de clase de prioridad alta puede usar casi todo el tiempo de CPU disponible.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tiempo real** (256)


</dt> <dd>

Especificado para un proceso que tiene la prioridad más alta posible. Los subprocesos del proceso tienen preferencia sobre los subprocesos de todos los demás procesos, incluidos los procesos del sistema operativo que realizan tareas importantes. Por ejemplo, un proceso en tiempo real que se ejecuta durante más de un intervalo muy breve puede hacer que las cachés del disco no se vacíen o que el mouse no responda.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta** (0)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Privilegios insuficientes** (3)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**No se encontró la ruta de acceso** (9)
</dt> <dt>

**Parámetro no válido** (21)
</dt> <dt>

**Otro** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

Para establecer la prioridad en tiempo real, el autor de la  llamada debe tener el **\_ \_ \_ \_ privilegio de prioridad base** de SeIncreaseBasePriorityPrivilege (se Inc). Sin este privilegio, la prioridad más alta puede establecerse en una prioridad alta.

## <a name="examples"></a>Ejemplos

El ejemplo de [modificación de la prioridad de un proceso en ejecución](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) de VBScript cambia la prioridad de una instancia en ejecución de Notepad.exe de normal a por encima de lo normal.

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

[**\_Proceso Win32**](win32-process.md)
</dt> </dl>

 

