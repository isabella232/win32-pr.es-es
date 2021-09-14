---
description: Solicita permiso para suspender el equipo. Una aplicación que concede este permiso tiene que realizar los preparativos para la suspensión antes de volver.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: PBT_APMQUERYSUSPEND evento (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062845"
---
# <a name="pbt_apmquerysuspend-event"></a>Evento \_ APMQUERYSUSPEND de PBT

\[PBT APMQUERYSUSPEND está disponible para su uso en los sistemas \_ operativos especificados en la sección Requisitos. La compatibilidad con este evento se quitó en Windows Vista. Use [**SetThreadExecutionState en su**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) lugar.\]

Solicita permiso para suspender el equipo. Una aplicación que concede este permiso tiene que realizar los preparativos para la suspensión antes de volver.

Una ventana recibe este evento a través [**del mensaje \_ WM POWERBROADCAST.**](wm-powerbroadcast.md) Los *parámetros wParam* *y lParam* se establecen como se describe a continuación.


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

*Hwnd* 
</dt> <dd>

Identificador a ventana.

</dd> <dt>*uMsg*</dt> <dd> 

| Value                                                                                                                                                                                                                                                                   | Significado                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificador del mensaje.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Value                                                                                                                                                                                                                                        | Significado                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <dt>**PBT \_ APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt> </dl> | Identificador de evento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Marcas de acción. Si el bit 0 es 1, la aplicación puede solicitar al usuario instrucciones sobre cómo prepararse para la suspensión. De lo contrario, la aplicación debe prepararse sin interacción del usuario. Todos los demás valores de bits están reservados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para conceder la solicitud de suspensión. Para denegar la solicitud, devuelva **BROADCAST \_ QUERY \_ DENY**.

## <a name="remarks"></a>Observaciones

Una aplicación debe procesar este evento lo más rápido posible. La aplicación puede solicitar al usuario instrucciones sobre cómo prepararse para la suspensión solo si se establece el bit 0 en el parámetro *Flags.* Sin embargo, si este mensaje se emite porque el usuario está cerrando la caja del portátil, no será posible preguntar al usuario. Las aplicaciones deben respetar que el usuario espera un comportamiento determinado cuando cierra la caja del portátil o presiona el botón de encendido y permite que la transición se haga correctamente.

El sistema permite aproximadamente 20 segundos para que una aplicación quite el mensaje [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) que envía el evento PBT APMQUERYSUSPEND de la cola de mensajes de la \_ aplicación. Si una aplicación no quita el mensaje de su cola en menos de 20 segundos, el sistema asumirá que la aplicación está en un estado no dinámico y que la aplicación acepta la solicitud de suspensión. Las aplicaciones que no procesan sus colas de mensajes pueden tener sus operaciones interrumpidas. Después de quitar el mensaje de la cola de mensajes, una aplicación puede tardar tanto tiempo como sea necesario para realizar las operaciones necesarias antes de entrar en el estado de suspensión. Cualquier operación que pueda tardar más de 20 segundos debe realizarse en este momento, ya que el sistema solo permite 20 segundos para que las operaciones se completen durante el procesamiento de [ \_ PBT APMSUSPEND.](pbt-apmsuspend.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                                    |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                                           |
| Encabezado<br/>                   | <dl> <dt>WinUser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Eventos de reactivación del sistema](system-wake-up-events.md)
</dt> <dt>

[Eventos de administración de energía](power-management-events.md)
</dt> <dt>

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




