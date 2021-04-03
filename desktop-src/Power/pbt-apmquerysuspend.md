---
description: Solicita permiso para suspender el equipo. Una aplicación que concede este permiso tiene que realizar los preparativos para la suspensión antes de volver.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: Evento PBT_APMQUERYSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909690"
---
# <a name="pbt_apmquerysuspend-event"></a>\_Evento PBT APMQUERYSUSPEND

\[PBT \_ APMQUERYSUSPEND está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. Se ha quitado la compatibilidad con este evento en Windows Vista. Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) en su lugar.\]

Solicita permiso para suspender el equipo. Una aplicación que concede este permiso tiene que realizar los preparativos para la suspensión antes de volver.

Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) . Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>*uMsg*</dt> <dd> 

| Value                                                                                                                                                                                                                                                                   | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificador de mensaje.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Value                                                                                                                                                                                                                                        | Significado                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <dt>**PBT \_ APMQUERYSUSPEND**</dt> <dt>0 (0X0)</dt> </dl> | Identificador del evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Marcas de acción. Si el bit 0 es 1, la aplicación puede preguntar al usuario para obtener instrucciones sobre cómo prepararse para la suspensión; de lo contrario, la aplicación debe prepararse sin la interacción del usuario. Todos los demás valores de bit están reservados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva **true** para permitir que la solicitud se suspenda. Para denegar la solicitud, devuelva la **consulta de difusión \_ \_**.

## <a name="remarks"></a>Observaciones

Una aplicación debe procesar este evento lo más rápido posible. La aplicación puede solicitar al usuario instrucciones sobre cómo prepararse para la suspensión solo si se establece el bit 0 en el parámetro *Flags* . Sin embargo, si se emite este mensaje porque el usuario está cerrando la tapa del portátil, no será posible preguntar al usuario. Las aplicaciones deben respetar que el usuario espera un determinado comportamiento al cerrar la tapa del portátil o presionar el botón de encendido y permitir que la transición se realice correctamente.

El sistema permite aproximadamente 20 segundos para que una aplicación Quite el mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) que está enviando el \_ evento PBT APMQUERYSUSPEND desde la cola de mensajes de la aplicación. Si una aplicación no quita el mensaje de su cola en menos de 20 segundos, el sistema asumirá que la aplicación está en un estado que no responde y que la aplicación acepta la solicitud de suspensión. Las aplicaciones que no procesan sus colas de mensajes pueden interrumpir sus operaciones. Después de quitar el mensaje de la cola de mensajes, una aplicación puede tardar tanto tiempo como sea necesario para realizar las operaciones necesarias antes de entrar en el estado de suspensión. En este momento, se deben realizar las operaciones que podrían tardar más de 20 segundos, ya que el sistema solo permite 20 segundos para que las operaciones se completen durante el procesamiento de [ \_ APMSUSPEND de PBT](pbt-apmsuspend.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                                    |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                                           |
| Encabezado<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de reactivación del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[**POWERBROADCAST de WM \_**](wm-powerbroadcast.md)
</dt> </dl>

 

 




