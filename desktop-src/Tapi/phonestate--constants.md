---
description: Las constantes de marca de bits PHONESTATE \_ describen varios elementos de estado para un dispositivo de teléfono.
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: PHONESTATE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168874"
---
# <a name="phonestate_-constants"></a>Constantes \_ PHONESTATE

Las constantes de marca de bits **PHONESTATE \_** describen varios elementos de estado para un dispositivo de teléfono.

<dl> <dt>

<span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) han cambiado. La aplicación debe usar [**phoneGetDevCaps para**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) leer la estructura actualizada. Si un proveedor de servicios envía un mensaje [**PHONE \_ STATE**](phone-state.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1.4 o posterior de TAPI; las aplicaciones que negocian una versión de API anterior recibirán mensajes PHONE STATE que especifican \_ PHONESTATE REINIT, lo que les obliga a cerrar y reinicializar su conexión a TAPI para obtener la información \_ actualizada.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE \_ CONECTADO**
</dt> <dd> <dl> <dt>



La conexión entre el dispositivo telefónico y TAPI se acaba de realizar. Esto sucede cuando se invoca TAPI por primera vez o cuando el cable que conecta el teléfono al equipo está conectado con TAPI activo.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



La información específica del dispositivo del teléfono ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE \_ DESCONECTADO**
</dt> <dd> <dl> <dt>



La conexión entre el dispositivo telefónico y TAPI se ha roto. Esto sucede cuando el cable que conecta el teléfono establecido al equipo se desconecta mientras TAPI está activo.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE \_ DISPLAY**
</dt> <dd> <dl> <dt>



La presentación del teléfono ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE \_ HANDSETGAIN**
</dt> <dd> <dl> <dt>



Ha cambiado la configuración de la ganancia del micrófono del terminal.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE \_ HANDSETHOOKSWITCH**
</dt> <dd> <dl> <dt>



El estado del conmutador de enlace del terminal ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE \_ HANDSETVOLUME**
</dt> <dd> <dl> <dt>



La configuración del volumen del altavoz del conjunto de manos ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE \_ HEADSETHOOKSWITCH**
</dt> <dd> <dl> <dt>



El estado del conmutador de enlace del casco ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE \_ HEADSETGAIN**
</dt> <dd> <dl> <dt>



La configuración de la ganancia del micrófono del casco ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE \_ HEADSETVOLUME**
</dt> <dd> <dl> <dt>



La configuración del volumen del altavoz del casco ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**PHONESTATE \_ LAMP**
</dt> <dd> <dl> <dt>



Ha cambiado una bombilla del teléfono.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**MONITORES PHONESTATE \_**
</dt> <dd> <dl> <dt>



Número de monitores para el dispositivo de teléfono.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE \_ OTHER**
</dt> <dd> <dl> <dt>



Teléfono los elementos de estado distintos de los enumerados a continuación han cambiado. La aplicación debe comprobar el estado actual del teléfono para determinar qué elementos han cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**PHONESTATE \_ OWNER**
</dt> <dd> <dl> <dt>



Número de propietarios del dispositivo telefónico.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**REINICIALIZACIÓN DE PHONESTATE \_**
</dt> <dd> <dl> <dt>



Los elementos han cambiado en la configuración de los dispositivos de teléfono. Para tener en cuenta estos cambios (en cuanto a la apariencia de los nuevos dispositivos de teléfono), la aplicación debe reinicializar su uso de TAPI.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE \_ QUITADO**
</dt> <dd> <dl> <dt>



Indica que el proveedor de servicios quita el dispositivo del sistema (lo más probable es que lo haga a través de una acción del usuario, a través de un panel de control o una utilidad similar). Normalmente, [**\_ un mensaje PHONE STATE**](phone-state.md) con este valor estará inmediatamente seguido de un mensaje PHONE [**\_ CLOSE**](phone-close.md) en el dispositivo. Los intentos posteriores de acceder al dispositivo antes de reinicializar TAPI darán lugar a que PHONEERR \_ NODEVICE se devuelva a la aplicación. Si un proveedor de servicios envía un mensaje PHONE STATE que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1.4 o posterior de TAPI; las aplicaciones que negocian una versión de API anterior no recibirán ninguna \_ notificación.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE \_ RESUME**
</dt> <dd> <dl> <dt>



El uso del dispositivo telefónico de la aplicación se reanuda después de haberse suspendido durante algún tiempo.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE \_ RINGMODE**
</dt> <dd> <dl> <dt>



El modo de anillo del teléfono ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE \_ RINGVOLUME**
</dt> <dd> <dl> <dt>



El volumen de anillo del teléfono ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE \_ SPEAKERHOOKSWITCH**
</dt> <dd> <dl> <dt>



El estado del conmutador de enlace del altavoz ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE \_ SPEAKERGAIN**
</dt> <dd> <dl> <dt>



El estado de la configuración de la ganancia del micrófono del altavoz ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE \_ SPEAKERVOLUME**
</dt> <dd> <dl> <dt>



La configuración del volumen del altavoz del altavoz ha cambiado.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE \_ SUSPEND**
</dt> <dd> <dl> <dt>



El uso del teléfono de la aplicación se suspende temporalmente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PHONE \_ CLOSE**](phone-close.md)
</dt> <dt>

[**ESTADO DEL \_ TELÉFONO**](phone-state.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




