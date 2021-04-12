---
description: El método Win32ShutdownTracker proporciona el mismo conjunto de opciones de cierre admitido por el método Win32Shutdown en el OperatingSystem de Win32 \_ , pero también permite especificar comentarios, un motivo para el apagado o un tiempo de espera.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Método Win32ShutdownTracker de la clase Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152853"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a>Método Win32ShutdownTracker de la \_ clase Win32 OperatingSystem

El método **Win32ShutdownTracker** proporciona el mismo conjunto de opciones de cierre admitido por el método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) en el [**\_ OperatingSystem de Win32**](win32-operatingsystem.md), pero también permite especificar comentarios, un motivo para el apagado o un tiempo de espera.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tiempo de espera* \[ de\]
</dt> <dd>

Tiempo, en segundos, antes de que tenga lugar el apagado. El valor predeterminado es 0 (cero).

</dd> <dt>

*Comentario* \[ de de\]
</dt> <dd>

Mensaje que se va a mostrar en el cuadro de diálogo de apagado que también se almacena como comentario en la entrada del registro de eventos.

</dd> <dt>

*ReasonCode* \[ de\]
</dt> <dd>

Motivo por el que se inicia el apagado.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Conjunto de mapas Dete de marcas para apagar el equipo. Para forzar un comando, agregue la marca Force (4) al valor del comando. Al usar forzar junto con el apagado o el reinicio de un equipo remoto, se cierra inmediatamente todo (incluido WMI, COM, etc.) o se reinicia el equipo remoto. Esto da como resultado un valor devuelto indeterminado.

<dt>

0 (0X0)
</dt> <dd>

Cerrar sesión

</dd> <dt>

4 (0x4)
</dt> <dd>

Cierre de sesión forzado (0 + 4)

</dd> <dt>

1 (0x1)
</dt> <dd>

Apagar

</dd> <dt>

5 (0X5)
</dt> <dd>

Cierre forzado (1 + 4)

</dd> <dt>

2 (0X2)
</dt> <dd>

Reboot

</dd> <dt>

6 (0x6)
</dt> <dd>

Reinicio forzado (2 + 4)

</dd> <dt>

8 (0x8)
</dt> <dd>

Apagar

</dd> <dt>

12 (0xC)
</dt> <dd>

Apagado forzado (8 + 4)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que la operación se ha realizado correctamente. Cualquier otro número indica que hubo un error. Para ver los códigos de error, consulte [**constantes error de WMI**](../wmisdk/wmi-error-constants.md) o [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](../debug/system-error-codes.md).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otro** (1 – 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El proceso de llamada debe tener el privilegio de **\_ \_ nombre de cierre de se** .

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se describe cómo llamar a **Win32ShutdownTracker**.


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
Next
```



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

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[**OperatingSystem de Win32 \_**](win32-operatingsystem.md)
</dt> <dt>

[**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
