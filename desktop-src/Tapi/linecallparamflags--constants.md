---
description: Las \_ constantes LINECALLPARAMFLAGS describen varias marcas de estado sobre una llamada.
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: Constantes de LINECALLPARAMFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678990"
---
# <a name="linecallparamflags_-constants"></a>Constantes de LINECALLPARAMFLAGS \_

Las **constantes \_ LINECALLPARAMFLAGS** describen varias marcas de estado sobre una llamada.

<dl> <dt>

<span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS \_ BLOCKID**
</dt> <dd> <dl> <dt>



La identidad del originador debe ocultarse (identificador del llamador de bloque).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS \_ DESTOFFHOOK**
</dt> <dd> <dl> <dt>



El teléfono de la entidad a la que se llama debe tomarse automáticamente OffHook.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS \_ inactivo**
</dt> <dd> <dl> <dt>



La llamada se debe originar en el aspecto de una llamada inactiva y no unirse a una llamada en curso. Cuando se usa la función [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , si \_ no se establece el valor inactivo de LINECALLPARAMFLAGS y hay una llamada existente en la línea, la función se interrumpe en la llamada existente si es necesario para realizar la nueva llamada. Si no hay ninguna llamada existente, la función realiza la nueva llamada según lo especificado.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



Este bit solo se usa junto con [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) y [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference). La dirección que se va a incluir en la Conferencia con la llamada actual se especifica en el miembro **targetAddress** de [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams). La llamada de consulta no dibuja físicamente el tono de marcado desde el conmutador, pero progresará a través de varios Estados del establecimiento de llamadas (por ejemplo, marcado y continuación). Cuando la llamada de consulta alcanza el estado conectado, la Conferencia se establece automáticamente. la llamada original, que permaneció en estado conectado, entra en el estado de conferencia; la llamada de consulta entra en el estado de conferencia; el hConfCall entra en el estado conectado. Si se produce un error en la llamada de consulta (entra en el estado disconnected seguido de idle), el hConfCall también entra en el estado inactivo y la llamada original (que puede haber sido una conferencia existente, en el caso de **linePrepareAddToConference**) permanece en estado conectado. La entidad original (o entidades) nunca percibe que la llamada ha desaparecido. Esta característica se usa a menudo para agregar un supervisor a una llamada del agente ACD cuando sea necesario para supervisar las interacciones con un llamador Irate.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



Este bit solo se usa junto con [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). Combina el funcionamiento de **lineSetupTransfer** seguido de la llamada de [**consulta en un**](/windows/desktop/api/Tapi/nf-tapi-linedial) solo paso. La dirección que se va a marcar se especifica en el miembro **targetAddress** de [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams). La llamada original se coloca en el estado *onholdpendingtransfer* , al igual que si se llamara a **lineSetupTransfer** normalmente, y la llamada de consulta se establece normalmente. La aplicación debe seguir llamando a [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) para que afecte a la transferencia. Esta característica se usa a menudo al invocar una transferencia desde un servidor a través de un vínculo de control de llamadas de terceros, ya que estos vínculos no admiten con frecuencia el proceso normal de dos pasos.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



El teléfono del autor debe tomarse automáticamente OffHook.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS \_ PREDICTIVEDIAL**
</dt> <dd> <dl> <dt>



Este bit solo se usa cuando se realiza una llamada en una dirección con funcionalidad de marcado de predicción (LINEADDRCAPFLAGS \_ PREDICTIVEDIALER está activada en el miembro **DwAddrCapFlags** de [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)). El bit debe estar activado para habilitar el progreso de llamada mejorado y/o las capacidades de supervisión de dispositivos multimedia del dispositivo. Si este bit no está activado, la llamada se realizará sin el progreso de llamada mejorado o la supervisión de tipo de medio, y no se iniciará ninguna transferencia automática en función del estado de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS \_ seguro**
</dt> <dd> <dl> <dt>



La llamada debe estar configurada como segura.


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

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**Fino**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




