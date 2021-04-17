---
description: Las \_ constantes de marcador de bits LINEADDRCAPFLAGS se usan en el miembro dwAddrCapFlags de la estructura de datos LINEADDRESSCAPS para describir diversas funcionalidades de dirección booleana.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: Constantes de LINEADDRCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690224"
---
# <a name="lineaddrcapflags_-constants"></a>Constantes de LINEADDRCAPFLAGS \_

Las  \_ constantes de marcador de bits LINEADDRCAPFLAGS se usan en el miembro **dwAddrCapFlags** de la estructura de datos [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) para describir diversas funcionalidades de dirección booleana.

<dl> <dt>

<span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS \_ ACCEPTTOALERT**
</dt> <dd> <dl> <dt>



**True** si se debe aceptar una llamada de oferta mediante [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) para iniciar la alerta de los usuarios en ambos extremos de la llamada. en caso contrario, **false**. Normalmente, solo se usa con ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS \_ ACDGROUP**
</dt> <dd> <dl> <dt>



La dirección admite [grupos ACD](about-call-center-controls.md#acd-group-object) en relación con las operaciones del centro de llamadas. Consulte [acerca de los controles del centro de llamadas](./about-call-center-controls.md) para obtener información adicional sobre los grupos ACD.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS \_ reconexión automática**
</dt> <dd> <dl> <dt>



Especifica si la eliminación de una llamada de consulta se vuelve a conectar automáticamente a la llamada en la espera de la consulta. **True** si la reconexión se produce automáticamente; en caso contrario, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS \_ BLOCKIDDEFAULT**
</dt> <dd> <dl> <dt>



Especifica si la red envía o bloquea de forma predeterminada información de identificador de autor de la llamada al efectuar una llamada a esta dirección. Si es **true**, la información del identificador está bloqueada de forma predeterminada; Si es **false**, la información del identificador se transmite de forma predeterminada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS \_ BLOCKIDOVERRIDE**
</dt> <dd> <dl> <dt>



Especifica si se puede invalidar la configuración predeterminada para enviar o bloquear la información de identificador de llamada por llamada. Si es **true**, se puede reemplazar. Si es **false**, no se puede reemplazar.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS \_ COMPLETIONID**
</dt> <dd> <dl> <dt>



Especifica si los identificadores de finalización devueltos por [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) son útiles y únicos. **True si es** útil; en caso contrario, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS \_ CONFDROP**
</dt> <dd> <dl> <dt>



**True** si [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) en una llamada de conferencia Parent también tiene el efecto secundario de quitar (es decir, desconectar) las demás partes implicadas en la llamada de conferencia; **False** si la eliminación de una llamada de Conferencia sigue permitiendo a las demás partes comunicarse entre ellas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS \_ CONFERENCEHELD**
</dt> <dd> <dl> <dt>



Especifica si se puede realizar la Conferencia de una llamada de retención. A menudo, solo las llamadas en la espera de la consulta se pueden agregar a como una llamada de conferencia.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS \_ CONFERENCEMAKE**
</dt> <dd> <dl> <dt>



Especifica si se puede establecer una llamada completamente nueva para su uso como una llamada de consulta (para agregar) en la Conferencia.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS \_ DESTOFFHOOK**
</dt> <dd> <dl> <dt>



Especifica si el teléfono de la entidad a la que se llama puede forzarse automáticamente OffHook al realizar llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**\_marcado LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Especifica si se puede marcar una dirección de destino en esta dirección para realizar una llamada. **True** si se debe marcar una dirección de destino; **False** si la dirección de destino es fija (como con un "teléfono activo").


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS \_ FWDBUSYNAADDR**
</dt> <dd> <dl> <dt>



Especifica si el reenvío de llamadas para ocupado y para ninguna respuesta puede usar diferentes direcciones de reenvío. Esta marca solo es significativa si el reenvío está ocupado y no se puede controlar por separado. Esta marca es **true** si el reenvío está ocupado y para ninguna respuesta puede usar direcciones de destino diferentes. de lo contrario, es **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS \_ FWDCONSULT**
</dt> <dd> <dl> <dt>



Especifica si el reenvío de llamadas implica el establecimiento de una llamada de consulta.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS \_ FWDINTEXTADDR**
</dt> <dd> <dl> <dt>



Especifica si las llamadas internas y externas se pueden reenviar a diferentes direcciones de reenvío. Este marcador solo es significativo si el reenvío de llamadas internas y externas se puede controlar por separado. Esta marca es **true** si las llamadas internas y externas se pueden reenviar a direcciones de destino diferentes; de lo contrario, es **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS \_ FWDNUMRINGS**
</dt> <dd> <dl> <dt>



Especifica si el número de anillos de una respuesta no se puede especificar cuando el reenvío de llamadas no responde. Si es **true**, el intervalo válido se proporciona en los miembros **dwMinFwdNumRings** y **dwMaxFwdNumRings** de la estructura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS \_ FWDSTATUSVALID**
</dt> <dd> <dl> <dt>



Especifica si el estado de reenvío de la estructura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) para esta dirección es válido o es como máximo una "estimación óptima", dada la ausencia de confirmación precisa del conmutador o la red.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS \_ HOLDMAKESNEW**
</dt> <dd> <dl> <dt>



Cuando una llamada en esta dirección se coloca en espera (mediante [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) o una acción externa), se crea automáticamente una nueva llamada (lo que es más probable en LINECALLSTATE \_ ditono).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS \_ NOEXTERNALCALLS**
</dt> <dd> <dl> <dt>



La dirección está asociada a una línea interna en una PBX que está restringida de forma que no se puede usar para realizar llamadas a una dirección fuera del conmutador (por ejemplo, es una Intercom). La aplicación puede usar esta indicación para ayudar al usuario a seleccionar la apariencia de llamada correcta que se va a usar para realizar una llamada. Cuando este bit está desactivado, no indica necesariamente que la dirección se puede usar para realizar llamadas externas, ya que el proveedor de servicios no puede ser Cognizant del tipo de línea.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS \_ NOINTERNALCALLS**
</dt> <dd> <dl> <dt>



La dirección está asociada a una línea directa (tronco) y no se puede usar para realizar llamadas internas en una PBX. La aplicación puede usar esta indicación para ayudar al usuario a seleccionar la apariencia de llamada correcta que se va a usar para realizar una llamada. Cuando este bit está desactivado, no indica necesariamente que la dirección se puede usar para realizar llamadas internas, ya que el proveedor de servicios no puede ser Cognizant del tipo de línea.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS \_ NOPSTNADDRESSTRANSLATION**
</dt> <dd> <dl> <dt>



Esta dirección no admite la traducción de direcciones de red telefónicas conmutadas públicamente. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



Especifica si el teléfono de la entidad de origen puede tomarse automáticamente OffHook al realizar llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS \_ PARTIALDIAL**
</dt> <dd> <dl> <dt>



Especifica si el marcado parcial está disponible.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS \_ PICKUPCALLWAIT**
</dt> <dd> <dl> <dt>



**True** si [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) se puede usar para recoger una llamada detectada por el usuario como una llamada de llamada en espera; en caso contrario, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS \_ PICKUPGROUPID**
</dt> <dd> <dl> <dt>



Especifica si se requiere un identificador de grupo para la recogida de llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS \_ PREDICTIVEDIALER**
</dt> <dd> <dl> <dt>



Esta dirección tiene funciones mejoradas de supervisión del progreso de las llamadas que se pueden aplicar a las llamadas salientes para determinar los Estados de la llamada, como *timbre*, *ocupado*, *specialinfo* y *conectado*, o el tipo de medio del dispositivo que responde a la llamada. También puede tener la capacidad de transferir automáticamente llamadas salientes a otra dirección cuando una llamada alcanza cualquiera de un conjunto predefinido de Estados.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**\_cola LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Esta dirección no está asociada a una estación o un dispositivo físico determinados, pero es un lugar en el que las llamadas esperan para un procesamiento posterior. Las llamadas que se colocan en la cola pueden recibir un tratamiento determinado. También se pueden transferir automáticamente cuando un recurso determinado está disponible (por ejemplo, si la cola es una cola de ACD y las llamadas están esperando a un agente disponible).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS \_ ROUTEPOINT**
</dt> <dd> <dl> <dt>



Esta dirección no está asociada a una estación o un dispositivo físico determinados, pero es un lugar en el que las llamadas esperan a que la aplicación realice el enrutamiento (la aplicación examina la dirección a la que se llama y puede redirigir la llamada a otra dirección). La llamada también se puede transferir automáticamente si expira el tiempo de espera de enrutamiento (el conmutador normalmente presupone un enrutamiento predeterminado).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS \_ seguro**
</dt> <dd> <dl> <dt>



Especifica si las llamadas en esta dirección se pueden proteger en el momento de la configuración de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS \_ SETCALLINGID**
</dt> <dd> <dl> <dt>



La aplicación puede optar por establecer el miembro **CallingPartyID** en [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) al llamar a [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) y a otras funciones que aceptan una estructura **LINECALLPARAMS** . El proveedor de servicios, si el contenido del identificador es aceptable y está disponible una ruta de acceso, pasar el identificador a la parte llamada para indicar la identidad de la entidad de llamada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS \_ SETUPCONFNULL**
</dt> <dd> <dl> <dt>



Especifica si la configuración de una llamada de conferencia comienza con una llamada inicial (**false**) o sin una llamada inicial (**true**).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS \_ TRANSFERHELD**
</dt> <dd> <dl> <dt>



Especifica si se puede transferir una llamada de retención. A menudo, solo se pueden transferir llamadas en la espera de la consulta.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS \_ TRANSFERMAKE**
</dt> <dd> <dl> <dt>



Especifica si se puede establecer una llamada completamente nueva para su uso como una llamada de consulta en la transferencia.


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

 

