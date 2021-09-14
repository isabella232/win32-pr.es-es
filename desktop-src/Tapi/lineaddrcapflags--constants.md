---
description: Las constantes de marca de bits LINEADDRCAPFLAGS se usan en el miembro dwAddrCapFlags de la estructura de datos LINEADDRESSCAPS para describir varias funcionalidades de \_ direcciones booleanas.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: LINEADDRCAPFLAGS_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250028"
---
# <a name="lineaddrcapflags_-constants"></a>Constantes LINEADDRCAPFLAGS \_

Las constantes de marca de bits **LINEADDRCAPFLAGS** se usan en el \_ **miembro dwAddrCapFlags** de la estructura de datos [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) para describir varias funcionalidades de direcciones booleanas.

<dl> <dt>

<span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS \_ ACCEPTTOALERT**
</dt> <dd> <dl> <dt>



**TRUE** si se debe aceptar una llamada de oferta mediante [**lineAccept para**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) empezar a alertar a los usuarios en ambos extremos de la llamada. de lo contrario, **FALSE**. Normalmente, esto solo se usa con ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS \_ ACDGROUP**
</dt> <dd> <dl> <dt>



La dirección admite grupos [de ACD en](about-call-center-controls.md#acd-group-object) conexión con las operaciones del centro de llamadas. Consulte [Acerca de los controles del centro de](./about-call-center-controls.md) llamadas para obtener información adicional sobre los grupos de ACD.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS \_ AUTORECONNECT**
</dt> <dd> <dl> <dt>



Especifica si la eliminación de una llamada de consulta se vuelve a conectar automáticamente a la llamada en espera de consulta. **TRUE si** la reconexión se realiza automáticamente; de lo contrario, **FALSE**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS \_ BLOCKIDDEFAULT**
</dt> <dd> <dl> <dt>



Especifica si la red envía o bloquea de forma predeterminada la información del identificador de autor de la llamada al realizar una llamada en esta dirección. Si **es TRUE,** la información del identificador está bloqueada de forma predeterminada; si **es FALSE**, la información del identificador se transmite de forma predeterminada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS \_ BLOCKIDOVERRIDE**
</dt> <dd> <dl> <dt>



Especifica si la configuración predeterminada para enviar o bloquear la información del identificador de autor de la llamada se puede invalidar por llamada. Si **es TRUE,** la invalidación es posible; si **es FALSE**, no es posible invalidar.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS \_ COMPLETIONID**
</dt> <dd> <dl> <dt>



Especifica si los identificadores de finalización devueltos por [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) son útiles y únicos. **TRUE** si es útil; de lo contrario, **FALSE**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS \_ CONFDROP**
</dt> <dd> <dl> <dt>



**TRUE** si [**lineDrop en**](/windows/desktop/api/Tapi/nf-tapi-linedrop) una llamada de conferencia primaria también tiene el efecto secundario de quitar (es decir, desconectar) a las demás partes implicadas en la llamada de conferencia; **FALSE** si la colocación de una llamada de conferencia todavía permite que las otras partes hablen entre sí.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS \_ CONFERENCEADD**
</dt> <dd> <dl> <dt>



Especifica si se puede realizar una llamada de duración precisa a la que se puede realizar la conferencia. A menudo, solo se pueden agregar llamadas en espera de consulta a como una llamada de conferencia.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS \_ CONFERENCEMAKE**
</dt> <dd> <dl> <dt>



Especifica si se puede establecer una llamada completamente nueva para usarla como una llamada de consulta (para agregar) en la conferencia.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS \_ DESTOFFHOOK**
</dt> <dd> <dl> <dt>



Especifica si el teléfono de la parte a la que se llamó se puede forzar automáticamente al realizar llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS \_ MARCADO**
</dt> <dd> <dl> <dt>



Especifica si se puede marcar una dirección de destino en esta dirección para realizar una llamada. **TRUE** si se debe marcar una dirección de destino; **FALSE** si la dirección de destino es fija (como con un "teléfono de acceso rápido").


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS \_ FWDBUSYNAADDR**
</dt> <dd> <dl> <dt>



Especifica si el reenvío de llamadas para ocupado y sin respuesta puede usar direcciones de reenvío diferentes. Esta marca solo es significativa si el reenvío para ocupado y para ninguna respuesta se puede controlar por separado. Esta marca es **TRUE si** el reenvío para ocupado y para ninguna respuesta puede usar direcciones de destino diferentes; de lo contrario, es **FALSE.**


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS \_ FWDCONSULT**
</dt> <dd> <dl> <dt>



Especifica si el reenvío de llamadas implica el establecimiento de una llamada de consulta.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS \_ FWDINTEXTADDR**
</dt> <dd> <dl> <dt>



Especifica si las llamadas internas y externas se pueden reenviar a direcciones de reenvío diferentes. Esta marca solo es significativa si el reenvío de llamadas internas y externas se puede controlar por separado. Esta marca es **TRUE si** las llamadas internas y externas se pueden reenviar a diferentes direcciones de destino; de lo contrario, es **FALSE.**


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS \_ FWDNUMRINGS**
</dt> <dd> <dl> <dt>



Especifica si se puede especificar el número de anillos para una sin respuesta al reenviar llamadas sin respuesta. Si **es TRUE,** el intervalo válido se proporciona en los miembros **dwMinFwdNumRings** y **dwMaxFwdNumRings** de la [**estructura LINEADDRESSCAPS.**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS \_ FWDSTATUSVALID**
</dt> <dd> <dl> <dt>



Especifica si el estado de reenvío en la estructura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) de esta dirección es válido o, como máximo, es una "mejor estimación", dada la ausencia de confirmación precisa por parte del conmutador o la red.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS \_ HOLDMAKESNEW**
</dt> <dd> <dl> <dt>



Cuando se coloca una llamada en esta dirección en espera (mediante [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) o una acción externa), se crea automáticamente una nueva llamada (lo más probable en LINECALLSTATE \_ DIALTONE).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS \_ NOEXTERNALCALLS**
</dt> <dd> <dl> <dt>



La dirección está asociada a una línea interna en un VALOR DE SERVICIO restringido de tal manera que no se puede usar para realizar llamadas a una dirección fuera del conmutador (por ejemplo, es un timbre). La aplicación puede usar esta indicación para ayudar al usuario a seleccionar la apariencia de llamada correcta que se usará para realizar una llamada. Cuando este bit está desactivado, no indica necesariamente que la dirección se puede usar para realizar llamadas externas, ya que es posible que el proveedor de servicios no sea consciente del tipo de línea.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS \_ NOINTERNALCALLS**
</dt> <dd> <dl> <dt>



La dirección está asociada a una línea co directa (tronco) y no se puede usar para realizar llamadas internas en un OBJETO SWITCH. La aplicación puede usar esta indicación para ayudar al usuario a seleccionar la apariencia de llamada correcta que se usará para realizar una llamada. Cuando este bit está desactivado, no indica necesariamente que la dirección se puede usar para realizar llamadas internas, ya que es posible que el proveedor de servicios no sea consciente del tipo de línea.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS \_ NOPSTNADDRESSTRANSLATION**
</dt> <dd> <dl> <dt>



Esta dirección no admite la traducción de direcciones de red telefónica conmutadas públicamente. Esta marca solo se expone a las aplicaciones que negocian una versión TAPI de 3.0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



Especifica si el teléfono de la parte de origen se puede quitar automáticamente al realizar llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS \_ PARTIALDIAL**
</dt> <dd> <dl> <dt>



Especifica si está disponible el marcado parcial.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS \_ PICKUPCALLWAIT**
</dt> <dd> <dl> <dt>



**TRUE** si [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) se puede usar para seleccionar una llamada detectada por el usuario como una llamada en espera de llamada; de lo contrario, **FALSE**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS \_ PICKUPGROUPID**
</dt> <dd> <dl> <dt>



Especifica si se requiere un identificador de grupo para la recogida de llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS \_ PREDICTIVEDIALER**
</dt> <dd> <dl> <dt>



Esta dirección tiene funcionalidades mejoradas de supervisión del progreso de la llamada que se pueden aplicar a las llamadas salientes para determinar los estados de llamada, como *ringback*, *busy*, *specialinfo* y *connected,* o el tipo de medio del dispositivo que responde a la llamada. También puede tener la capacidad de transferir automáticamente las llamadas salientes a otra dirección cuando una llamada alcanza cualquiera de los estados predefinidos.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**COLA LINEADDRCAPFLAGS \_**
</dt> <dd> <dl> <dt>



Esta dirección no está asociada a una estación o dispositivo físico determinados, pero es un lugar de retención donde las llamadas esperan a un procesamiento adicional. Las llamadas colocadas en la cola pueden recibir un tratamiento determinado. También se pueden transferir automáticamente cuando un recurso determinado está disponible (por ejemplo, si la cola es una cola de ACD y las llamadas esperan a un agente disponible).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS \_ ROUTEPOINT**
</dt> <dd> <dl> <dt>



Esta dirección no está asociada a una estación o dispositivo físico determinados, pero es un lugar de retención donde las llamadas esperan el enrutamiento por parte de la aplicación (la aplicación examina la dirección llamada y puede redirigir la llamada a otra dirección). La llamada también se puede transferir automáticamente si expira un tiempo de espera de enrutamiento (el conmutador suele suponer un enrutamiento predeterminado).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS \_ SECURE**
</dt> <dd> <dl> <dt>



Especifica si las llamadas en esta dirección se pueden proteger en el momento de la configuración de llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS \_ SETCALLINGID**
</dt> <dd> <dl> <dt>



La aplicación puede optar por establecer el miembro **CallingPartyID** en [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) al llamar a [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) y otras funciones que aceptan una **estructura LINECALLPARAMS.** Si el contenido del identificador es aceptable y hay una ruta de acceso disponible, el proveedor de servicios pasará el identificador a la parte llamada para indicar la identidad de la parte que realiza la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS \_ SETUPCONFNULL**
</dt> <dd> <dl> <dt>



Especifica si la configuración de una llamada de conferencia comienza con una llamada inicial **(FALSE)** o sin ninguna llamada inicial **(TRUE).**


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS \_ TRANSFERADD**
</dt> <dd> <dl> <dt>



Especifica si se puede transferir una llamada a duración. A menudo, solo se pueden transferir las llamadas en espera de consulta.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS \_ TRANSFERMAKE**
</dt> <dd> <dl> <dt>



Especifica si se puede establecer una llamada completamente nueva para usarla como una llamada de consulta en la transferencia.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

