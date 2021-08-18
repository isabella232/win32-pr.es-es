---
description: Las constantes de marca de bits LINEDEVSTATE \_ describen varios eventos de estado de línea.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: LINEDEVSTATE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb11959614999ff50e421e0b77c63d1215a831040774e3123b43aa3534a3f853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140068"
---
# <a name="linedevstate_-constants"></a>Constantes \_ LINEDEVSTATE

Las constantes de marca de bits **LINEDEVSTATE \_** describen varios eventos de estado de línea.

<dl> <dt>

<span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**LINEDEVSTATE \_ BATTERY**
</dt> <dd> <dl> <dt>



El nivel de batería ha cambiado significativamente (móvil).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) de la dirección han cambiado. La aplicación debe usar [**lineGetDevCaps para**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) leer la estructura actualizada. Si un proveedor de servicios envía un mensaje [**\_ LINE LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado TAPI versión 1.4 o posterior; las aplicaciones que negocian una versión anterior de TAPI recibirán mensajes **LINE \_ LINEDEVSTATE** que especifican LINEDEVSTATE REINIT, lo que les obliga a apagar y reinicializar su conexión con TAPI para obtener la información \_ actualizada.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ CLOSE**
</dt> <dd> <dl> <dt>



Otra aplicación ha cerrado la línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**
</dt> <dd> <dl> <dt>



Indica que se han realizado cambios de configuración en uno o varios de los dispositivos multimedia asociados al dispositivo de línea. La aplicación, si lo desea, puede usar [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) para leer la información actualizada. Si un proveedor de servicios envía un mensaje [**\_ LINE LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado TAPI versión 1.4 o posterior; las aplicaciones que negocian una versión de API anterior no recibirán ninguna notificación.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**
</dt> <dd> <dl> <dt>



Indica que la finalización de la llamada identificada por el identificador de finalización contenido en el parámetro *dwParam2* del mensaje [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) se ha cancelado externamente y ya no se considera válida (si ese valor se pasara en una llamada posterior a [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), la función produciría un error con \_ LINEERR INVALCOMPLETIONID). Si un proveedor de servicios envía un mensaje [**\_ LINE LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado TAPI versión 1.4 o posterior; las aplicaciones que negocian una versión de API anterior no recibirán ninguna notificación.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ CONECTADO**
</dt> <dd> <dl> <dt>



La línea se desconectó anteriormente y ahora está conectada a TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



La información específica del dispositivo de la línea ha cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ DESCONECTADO**
</dt> <dd> <dl> <dt>



Esta línea estaba conectada anteriormente y ahora está desconectada de TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE \_ INSERVICE**
</dt> <dd> <dl> <dt>



La línea está conectada a TAPI. Esto sucede cuando TAPI se activa por primera vez o cuando el cable de línea está conectado físicamente y en servicio en el conmutador mientras TAPI está activo.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**LINEDEVSTATE \_ LOCK**
</dt> <dd> <dl> <dt>



El estado bloqueado del dispositivo de línea ha cambiado. (Para obtener más información, vea LINEDEVSTATUSFLAGS \_ LOCKED en [**constantes LINEDEVSTATUSFLAGS \_**](linedevstatusflags--constants.md)).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**MANTENIMIENTO DE \_ LINEDEVSTATE**
</dt> <dd> <dl> <dt>



El mantenimiento se realiza en la línea en el conmutador. TAPI no se puede usar para operar en el dispositivo de línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**
</dt> <dd> <dl> <dt>



El indicador de espera de mensajes está desactivado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE \_ MSGWAITON**
</dt> <dd> <dl> <dt>



El indicador de espera de mensajes está activado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



El número de llamadas en el dispositivo de línea ha cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE \_ NUMCOMPLETIONS**
</dt> <dd> <dl> <dt>



El número de finalizaciones de llamadas pendientes en el dispositivo de línea ha cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ OPEN**
</dt> <dd> <dl> <dt>



Otra aplicación ha abierto la línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ OTHER**
</dt> <dd> <dl> <dt>



Los elementos de estado del dispositivo distintos de los que se enumeran a continuación han cambiado. La aplicación debe comprobar el estado actual del dispositivo para determinar qué elementos han cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**
</dt> <dd> <dl> <dt>



La línea está fuera de servicio en el conmutador o físicamente desconectada. TAPI no se puede usar para operar en el dispositivo de línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE \_ REINIT**
</dt> <dd> <dl> <dt>



Los elementos han cambiado en la configuración de los dispositivos de línea. Para tener en cuenta estos cambios (en cuanto a la apariencia de los nuevos dispositivos de línea), la aplicación debe reinicializar su uso de TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ QUITADO**
</dt> <dd> <dl> <dt>



Indica que el proveedor de servicios quita el dispositivo del sistema (lo más probable es que lo haga a través de una acción del usuario, a través de un panel de control o una utilidad similar). Normalmente, [**\_ un mensaje LINE LINEDEVSTATE**](line-linedevstate.md) con este valor estará seguido inmediatamente de un [**mensaje LINE \_ CLOSE**](line-close.md) en el dispositivo. Los intentos posteriores de acceder al dispositivo antes de reinicializar TAPI darán lugar a que LINEERR \_ NODEVICE se devuelva a la aplicación. Si un proveedor de servicios envía un mensaje [**\_ LINE LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado TAPI versión 1.4 o posterior; las aplicaciones que negocian una versión de API anterior no recibirán ninguna notificación.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**ANILLO \_ LINEDEVSTATE**
</dt> <dd> <dl> <dt>



El modificador indica a la línea que alerte al usuario.

**TAPI:** Los proveedores de servicios notifican a las aplicaciones en cada ciclo de anillo mediante el envío repetido de [**mensajes \_ LINE LINEDEVSTATE**](line-linedevstate.md) que contienen esta constante. Por ejemplo, en la Estados Unidos, los proveedores de servicios envían un mensaje con esta constante cada seis segundos.

**TSPI:** En un dispositivo POTS, el proveedor de servicios puede enviar el mensaje cada vez que la oficina central envía el voltaje del anillo. En dispositivos digitales como ISDN, el proveedor de servicios puede necesitar sintetizar la repetición del mensaje si el conmutador genera solo una solicitud de anillo. Cada repetición del mensaje debe mostrar el aumento del número de anillos para que las funciones de ahorro de peaje funcionen correctamente.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ ROAMMODE**
</dt> <dd> <dl> <dt>



El modo de roam del dispositivo de línea ha cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**LINEDEVSTATE \_ SIGNAL**
</dt> <dd> <dl> <dt>



El nivel de señal ha cambiado significativamente (móvil).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**TERMINALES LINEDEVSTATE \_**
</dt> <dd> <dl> <dt>



La configuración del terminal ha cambiado. Esto puede ocurrir, por ejemplo, si varios dispositivos de línea comparten terminales entre ellos (por ejemplo, dos líneas que comparten un terminal de teléfono).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**
</dt> <dd> <dl> <dt>



Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) han cambiado. La aplicación debe usar [**lineGetTranslateCaps para**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) leer la estructura actualizada. Si un proveedor de servicios envía un mensaje [**\_ LINE LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado TAPI versión 1.4 o posterior; las aplicaciones que negocian una versión anterior de TAPI recibirán mensajes **LINE \_ LINEDEVSTATE** que especifican LINEDEVSTATE REINIT, lo que les obliga a apagar y reinicializar su conexión con TAPI para obtener la información \_ actualizada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




