---
description: El método Win32ShutdownTracker proporciona el mismo conjunto de opciones de apagado compatibles con el método Win32Shutdown en Win32 OperatingSystem, pero también permite especificar comentarios, un motivo de apagado o un tiempo de \_ espera.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Método Win32ShutdownTracker de la Win32_OperatingSystem clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968776"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a>Método Win32ShutdownTracker de la clase OperatingSystem win32 \_

El método **Win32ShutdownTracker** proporciona el mismo conjunto de opciones de apagado compatibles con el método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) en [**Win32 \_ OperatingSystem,**](win32-operatingsystem.md)pero también permite especificar comentarios, un motivo de apagado o un tiempo de espera.

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

*Tiempo de espera* \[ En\]
</dt> <dd>

Tiempo, en segundos, antes de que se lleve a cabo el apagado. El valor predeterminado es 0 (cero).

</dd> <dt>

*Comentario* \[ En\]
</dt> <dd>

Mensaje que se va a mostrar en el cuadro de diálogo de apagado que también se almacena como comentario en la entrada del registro de eventos.

</dd> <dt>

*ReasonCode* \[ En\]
</dt> <dd>

Motivo para iniciar el apagado.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Conjunto de marcas de mapa de bits para apagar el equipo. Para forzar un comando, agregue la marca Force (4) al valor del comando. El uso de Forzar junto con Apagar o Reiniciar en un equipo remoto apaga inmediatamente todo (incluido WMI, COM, entre otros) o reinicia el equipo remoto. Esto da como resultado un valor devuelto indeterminado.

<dt>

0 (0x0)
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

5 (0x5)
</dt> <dd>

Apagado forzado (1 + 4)

</dd> <dt>

2 (0x2)
</dt> <dd>

Reiniciar

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

Devuelve cero (0) para indicar que se ha correcto. Cualquier otro número indica que hubo un error. Para obtener códigos de error, [**vea Wmi Error Constants**](../wmisdk/wmi-error-constants.md) o [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](../debug/system-error-codes.md).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otros** (1-4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El proceso de llamada debe tener el **SE \_ SHUTDOWN \_ NAME.**

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código VBScript se describe cómo llamar a **Win32ShutdownTracker**.


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[**Sistema operativo \_ Win32**](win32-operatingsystem.md)
</dt> <dt>

[**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
