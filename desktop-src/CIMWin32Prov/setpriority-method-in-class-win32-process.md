---
description: SetPriority&\# 32; El método de clase WMI intenta cambiar la prioridad de ejecución del proceso.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Método SetPriority de la Win32_Process clase
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
ms.openlocfilehash: decd5892d480e4f236ae9d7acdc1a25c018557166535c963eb35dc3f6f62ffa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675574"
---
# <a name="setpriority-method-of-the-win32_process-class"></a>Método SetPriority de la clase Win32 \_ Process

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPriority** intenta cambiar la prioridad de ejecución del proceso.

En este tema se Managed Object Format sintaxis de MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Prioridad* \[ En\]
</dt> <dd>

Nueva clase de prioridad para el proceso. Tenga en cuenta que estos valores son diferentes de los indicados explícitamente en la **propiedad Priority** de [**Win32 \_ Process**](win32-process.md).

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactivo** (64)


</dt> <dd>

Se especifica para un proceso con subprocesos que se ejecutan solo cuando el sistema está inactivo. Los subprocesos de un proceso que se ejecutan en una clase de prioridad superior adelantan los subprocesos del proceso, por ejemplo, un protector de pantalla. Los procesos secundarios heredan la clase idle-priority.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Por debajo de Normal** (16384)


</dt> <dd>

Indica un proceso que tiene prioridad por encima de **IDLE \_ PRIORITY \_ CLASS**, pero por debajo **de NORMAL PRIORITY \_ \_ CLASS**.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)


</dt> <dd>

Se especifica para un proceso sin necesidad de programación especial.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Por encima de normal** (32768)


</dt> <dd>

Indica un proceso que tiene prioridad por encima de **NORMAL \_ PRIORITY \_ CLASS**, pero por debajo **de HIGH PRIORITY \_ \_ CLASS**.

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Prioridad alta** (128)


</dt> <dd>

Se especifica para un proceso que realiza tareas de tiempo crítico que se deben ejecutar inmediatamente. Los subprocesos del proceso tienen prioridad sobre los subprocesos de aquellos procesos de clase de prioridad normal o inactiva. Un ejemplo es el Lista de tareas, que debe responder rápidamente cuando lo llama el usuario, independientemente de la carga en el sistema operativo. Debe tener mucho cuidado al usar la clase de prioridad alta, ya que una aplicación de clase de prioridad alta puede usar casi todo el tiempo de CPU disponible.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tiempo real** (256)


</dt> <dd>

Se especifica para un proceso que tiene la prioridad más alta posible. Los subprocesos del proceso adelantan los subprocesos de todos los demás procesos, incluidos los procesos del sistema operativo que realizan tareas importantes. Por ejemplo, un proceso en tiempo real que se ejecuta durante más de un intervalo muy breve puede hacer que las cachés de disco no se vacíen o que un mouse deje de responder.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta** (0)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Privilegios insuficientes** (3)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**Ruta de acceso no encontrada** (9)
</dt> <dt>

**Parámetro no válido** (21)
</dt> <dt>

**Otros** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

Para establecer la prioridad en Tiempo real, el autor de la llamada debe tener **SeIncreaseBasePriorityPrivilege** (**SE INC BASE PRIORITY \_ \_ \_ \_ PRIVILEGE**). Sin este privilegio, la prioridad más alta que se puede establecer en es Alta prioridad.

## <a name="examples"></a>Ejemplos

El [ejemplo modify the priority of a running process](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript cambia la prioridad de una instancia en ejecución de Notepad.exe normal a por encima de normal.

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

[**Proceso \_ win32**](win32-process.md)
</dt> </dl>

 

