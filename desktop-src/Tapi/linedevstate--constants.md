---
description: Las \_ constantes de marcador de bits LINEDEVSTATE describen diversos eventos de estado de línea.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: Constantes de LINEDEVSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49717c1adb0f62a48a041f5920c0b82c7b817277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691068"
---
# <a name="linedevstate_-constants"></a>Constantes de LINEDEVSTATE \_

Las constantes de marcador de bits **LINEDEVSTATE \_** describen diversos eventos de estado de línea.

<dl> <dt>

<span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**\_batería LINEDEVSTATE**
</dt> <dd> <dl> <dt>



El nivel de batería ha cambiado significativamente (teléfono móvil).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para la dirección han cambiado. La aplicación debe usar [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) para leer la estructura actualizada. Si un proveedor de servicios envía un mensaje [**line \_ LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de TAPI recibirán los mensajes de **línea \_ LINEDEVSTATE** que especifican LINEDEVSTATE \_ reinit, lo que les obliga a apagar y reinicializar su conexión con TAPI para obtener la información actualizada.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ cerrar**
</dt> <dd> <dl> <dt>



Otra aplicación ha cerrado la línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**
</dt> <dd> <dl> <dt>



Indica que se han realizado cambios de configuración en uno o varios de los dispositivos multimedia asociados al dispositivo de línea. La aplicación, si lo desea, puede usar [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) para leer la información actualizada. Si un proveedor de servicios envía un mensaje [**line \_ LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de la API no recibirán ninguna notificación.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**
</dt> <dd> <dl> <dt>



Indica que la finalización de la llamada identificada por el identificador de finalización incluida en el parámetro *dwParam2* del mensaje de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) se canceló externamente y ya no se considera válida (si ese valor se pasara en una llamada subsiguiente a [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), la función produciría un error con LINEERR \_ INVALCOMPLETIONID). Si un proveedor de servicios envía un mensaje [**line \_ LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de la API no recibirán ninguna notificación.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ conectado**
</dt> <dd> <dl> <dt>



La línea se desconectó previamente y ahora está conectada a TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



La información específica del dispositivo de la línea ha cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ DESconectado**
</dt> <dd> <dl> <dt>



Esta línea estaba conectada previamente y ahora está desconectada de TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**SERVICIO de LINEDEVSTATE \_**
</dt> <dd> <dl> <dt>



La línea está conectada a TAPI. Esto sucede cuando TAPI se activa por primera vez o cuando el cable de línea está físicamente conectado y en servicio en el conmutador mientras TAPI está activo.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**\_bloqueo LINEDEVSTATE**
</dt> <dd> <dl> <dt>



El estado de bloqueo del dispositivo de línea ha cambiado. (Para obtener más información, consulte LINEDEVSTATUSFLAGS \_ BLOQUEADO en [**\_ constantes LINEDEVSTATUSFLAGS**](linedevstatusflags--constants.md)).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**mantenimiento de LINEDEVSTATE \_**
</dt> <dd> <dl> <dt>



El mantenimiento se realiza en la línea en el conmutador. No se puede usar TAPI para operar en el dispositivo de línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**
</dt> <dd> <dl> <dt>



El indicador de espera del mensaje está desactivado.


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



Ha cambiado el número de finalizaciones de llamadas pendientes en el dispositivo de línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ abrir**
</dt> <dd> <dl> <dt>



Otra aplicación ha abierto la línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ otro**
</dt> <dd> <dl> <dt>



Los elementos de estado de dispositivo distintos de los que se enumeran a continuación han cambiado. La aplicación debe comprobar el estado actual del dispositivo para determinar qué elementos han cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**
</dt> <dd> <dl> <dt>



La línea está fuera de servicio en el conmutador o está físicamente desconectada. No se puede usar TAPI para operar en el dispositivo de línea.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**reinicialización de LINEDEVSTATE \_**
</dt> <dd> <dl> <dt>



Los elementos han cambiado en la configuración de los dispositivos de línea. Para tener en cuenta estos cambios (como en el aspecto de los dispositivos de nueva línea), la aplicación debe reinicializar el uso de TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ quitado**
</dt> <dd> <dl> <dt>



Indica que el proveedor de servicios está quitando el dispositivo del sistema (lo que es más probable a través de la acción del usuario, a través de un panel de control o una utilidad similar). Un mensaje de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) con este valor normalmente irá seguido inmediatamente de un mensaje de [**\_ cierre de línea**](line-close.md) en el dispositivo. Los intentos posteriores de obtener acceso al dispositivo antes de que se reinicialice TAPI darán lugar a que se \_ devuelva LINEERR Device a la aplicación. Si un proveedor de servicios envía un mensaje [**line \_ LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de la API no recibirán ninguna notificación.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**\_timbre LINEDEVSTATE**
</dt> <dd> <dl> <dt>



El modificador indica a la línea que avise al usuario.

**TAPI:** Los proveedores de servicios notifican a las aplicaciones en cada ciclo de timbre enviando repetidamente mensajes de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) que contienen esta constante. Por ejemplo, en el Estados Unidos, los proveedores de servicios envían un mensaje con esta constante cada seis segundos.

**TSPI:** En un dispositivo de POTS, el proveedor de servicios puede enviar el mensaje cada vez que la oficina central envía la tensión de timbre. En dispositivos digitales como ISDN, es posible que el proveedor de servicios tenga que sintetizar la repetición del mensaje si el modificador solo genera una solicitud de anillo. Cada repetición del mensaje debería mostrar el aumento del número de timbres, de modo que las funciones de guardado de peaje funcionen correctamente.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ ROAMMODE**
</dt> <dd> <dl> <dt>



El modo de itinerancia del dispositivo de línea ha cambiado.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**\_señal LINEDEVSTATE**
</dt> <dd> <dl> <dt>



El nivel de señal ha cambiado significativamente (teléfono móvil).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**\_terminales LINEDEVSTATE**
</dt> <dd> <dl> <dt>



La configuración de terminal ha cambiado. Esto puede ocurrir, por ejemplo, si varios dispositivos de línea comparten terminales entre ellos (por ejemplo, dos líneas que comparten un terminal telefónico).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**
</dt> <dd> <dl> <dt>



Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) han cambiado. La aplicación debe usar [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) para leer la estructura actualizada. Si un proveedor de servicios envía un mensaje [**line \_ LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de TAPI recibirán los mensajes de **línea \_ LINEDEVSTATE** que especifican LINEDEVSTATE \_ reinit, lo que les obliga a apagar y reinicializar su conexión con TAPI para obtener la información actualizada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**cierre de línea \_**](line-close.md)
</dt> <dt>

[**LÍNEA \_ LINEDEVSTATE**](line-linedevstate.md)
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

 

 




