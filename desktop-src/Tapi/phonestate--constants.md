---
description: Las \_ constantes de marcador de bits PHONESTATE describen varios elementos de estado para un dispositivo telefónico.
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: Constantes de PHONESTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679230"
---
# <a name="phonestate_-constants"></a>Constantes de PHONESTATE \_

Las constantes de marcador de bits **PHONESTATE \_** describen varios elementos de estado para un dispositivo telefónico.

<dl> <dt>

<span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) han cambiado. La aplicación debe usar [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) para leer la estructura actualizada. Si un proveedor de servicios envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de API recibirán mensajes de estado de teléfono que \_ especifican PHONESTATE \_ reinit, lo que les obliga a apagar y reinicializar la conexión a TAPI para obtener la información actualizada


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE \_ conectado**
</dt> <dd> <dl> <dt>



Se acaba de realizar la conexión entre el dispositivo telefónico y TAPI. Esto sucede cuando se invoca primero TAPI o cuando el cable que conecta el teléfono al equipo está conectado con TAPI activo.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



La información específica del dispositivo del teléfono ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE \_ DESconectado**
</dt> <dd> <dl> <dt>



La conexión entre el dispositivo telefónico y TAPI se acaba de interrumpir. Esto sucede cuando el cable que conecta el teléfono al equipo está desconectado mientras TAPI está activo.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE \_ Mostrar**
</dt> <dd> <dl> <dt>



La presentación del teléfono ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE \_ HANDSETGAIN**
</dt> <dd> <dl> <dt>



La configuración de ganancia de micrófono del auricular ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE \_ HANDSETHOOKSWITCH**
</dt> <dd> <dl> <dt>



El estado de conmutador de auricular ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE \_ HANDSETVOLUME**
</dt> <dd> <dl> <dt>



La configuración del volumen de altavoz del auricular ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE \_ HEADSETHOOKSWITCH**
</dt> <dd> <dl> <dt>



El estado de conmutador del casco ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE \_ HEADSETGAIN**
</dt> <dd> <dl> <dt>



La configuración de ganancia de micrófono del casco ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE \_ HEADSETVOLUME**
</dt> <dd> <dl> <dt>



La configuración del volumen de altavoz del casco ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**\_lámpara PHONESTATE**
</dt> <dd> <dl> <dt>



Ha cambiado una lámpara del teléfono.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**\_monitores PHONESTATE**
</dt> <dd> <dl> <dt>



El número de monitores para el dispositivo telefónico.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE \_ otro**
</dt> <dd> <dl> <dt>



Los elementos de estado de teléfono distintos de los que se enumeran a continuación han cambiado. La aplicación debe comprobar el estado del teléfono actual para determinar qué elementos han cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**propietario de PHONESTATE \_**
</dt> <dd> <dl> <dt>



El número de propietarios del dispositivo telefónico.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**reinicialización de PHONESTATE \_**
</dt> <dd> <dl> <dt>



Los elementos han cambiado en la configuración de los dispositivos telefónicos. Para tener en cuenta estos cambios (como en el aspecto de los nuevos dispositivos telefónicos), la aplicación debe reinicializar el uso de TAPI.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE \_ quitado**
</dt> <dd> <dl> <dt>



Indica que el proveedor de servicios está quitando el dispositivo del sistema (lo que es más probable a través de la acción del usuario, a través de un panel de control o una utilidad similar). Un mensaje de [**\_ Estado de teléfono**](phone-state.md) con este valor normalmente irá seguido inmediatamente de un mensaje de [**\_ cierre de teléfono**](phone-close.md) en el dispositivo. Los intentos posteriores de obtener acceso al dispositivo antes de que se reinicialice TAPI darán lugar a que se \_ devuelva PHONEERR Device a la aplicación. Si un proveedor de servicios envía un \_ mensaje de estado de teléfono que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de la API no recibirán ninguna notificación.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**\_reanudación de PHONESTATE**
</dt> <dd> <dl> <dt>



El uso de la aplicación del dispositivo telefónico se reanuda después de haberse suspendido durante algún tiempo.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE \_ RINGMODE**
</dt> <dd> <dl> <dt>



El modo de anillo del teléfono ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE \_ RINGVOLUME**
</dt> <dd> <dl> <dt>



El volumen de timbre del teléfono ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE \_ SPEAKERHOOKSWITCH**
</dt> <dd> <dl> <dt>



El estado de conmutador del altavoz ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE \_ SPEAKERGAIN**
</dt> <dd> <dl> <dt>



Ha cambiado el estado de la opción de ganancia de micrófono del altavoz.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE \_ SPEAKERVOLUME**
</dt> <dd> <dl> <dt>



La configuración del volumen de altavoz del altavoz ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**suspensión de PHONESTATE \_**
</dt> <dd> <dl> <dt>



El uso de la aplicación del teléfono se suspende temporalmente.


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

[**\_cerrar teléfono**](phone-close.md)
</dt> <dt>

[**Estado del teléfono \_**](phone-state.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




