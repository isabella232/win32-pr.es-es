---
description: Las \_ constantes LINEMEDIAMODE describen los tipos de medios (o modos) de una sesión de comunicaciones o una llamada a.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: Constantes de LINEMEDIAMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680770"
---
# <a name="linemediamode_-constants"></a>Constantes de LINEMEDIAMODE \_

Las **constantes \_ LINEMEDIAMODE** describen los tipos de medios (o modos) de una sesión de comunicaciones o una llamada a.

<dl> <dt>

<span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**
</dt> <dd> <dl> <dt>



Se ha detectado energía de voz en la llamada, y la voz se controla localmente mediante una aplicación automatizada como, por ejemplo, con una aplicación de equipo de respuesta. Cuando un proveedor de servicios no puede distinguir entre voz interactiva y automatizada en una llamada entrante, notificará la llamada como voz interactiva.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE de \_ módem**
</dt> <dd> <dl> <dt>



Una sesión de módem de datos en la llamada. Los protocolos de módem actuales requieren que la estación llamada inicie el protocolo de enlace. En el caso de una llamada de módem de datos de entrada, la aplicación normalmente no puede hacer ninguna detección positiva. La forma en que el proveedor de servicios toma esta decisión es su elección. Por ejemplo, se puede usar un período de silencio justo después de responder a una llamada entrante como heurística para decidir que esto podría ser una llamada de módem de datos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**
</dt> <dd> <dl> <dt>



Una sesión ADSI (interfaz de servicios de pantalla analógica) en la llamada. ADSI mejora las llamadas de voz con información alfanumérica descargada en el teléfono y el uso de botones flexibles en el teléfono.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE \_ DIGITALDATA**
</dt> <dd> <dl> <dt>



Flujo de datos digitales del formato no especificado.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE \_ G3FAX**
</dt> <dd> <dl> <dt>



Se está enviando o recibiendo un fax de grupo 3 a través de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE \_ G4FAX**
</dt> <dd> <dl> <dt>



Se está enviando o recibiendo un fax de grupo 4 a través de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE \_ INTERACTIVEVOICE**
</dt> <dd> <dl> <dt>



Se ha detectado energía de voz en la llamada y la llamada se trata como una llamada de voz interactiva con seres humanos en ambos extremos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ Mixed**
</dt> <dd> <dl> <dt>



Una sesión mixta en la llamada. Mixed es uno de los servicios telemáticos de ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**
</dt> <dd> <dl> <dt>



Una sesión de TDD (dispositivos de telefonía para sordos) en la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ teletexto**
</dt> <dd> <dl> <dt>



Una sesión de teletexto en la llamada. Teletexto es uno de los servicios telemáticos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**\_télex LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



Una sesión de télex en la llamada. Télex es uno de los servicios telemáticos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**vídeo de LINEMEDIAMODE \_**
</dt> <dd> <dl> <dt>



El tipo de medio de la llamada es vídeo. (Versiones de TAPI 2,1 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**
</dt> <dd> <dl> <dt>



Una sesión de Videotex en la llamada. Videotex es uno de los servicios telemáticos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**VOICEVIEW de LINEMEDIAMODE \_**
</dt> <dd> <dl> <dt>



El tipo de medio de la llamada es VoiceView. (Versiones de TAPI 1,4 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ desconocido**
</dt> <dd> <dl> <dt>



Existe un flujo multimedia pero su modo no se conoce actualmente y se puede conocer más adelante. Esto corresponde a una llamada con un tipo de medio sin clasificar. En los entornos de telefonía analógica típicos, el tipo de medio de una llamada entrante puede ser desconocido hasta que se haya respondido a la llamada y se haya filtrado el flujo multimedia para realizar una determinación.

Si se establece la marca de modo de medio desconocido, también se pueden establecer otras marcas multimedia. Se usa para indicar que el medio es desconocido pero que es probable que sea uno de los otros tipos de medios seleccionados.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Todos los 32 bits están reservados.

Tenga en cuenta que el modo de portador y el tipo de medio son nociones diferentes. El modo de portador de una llamada es una indicación de la calidad de la conexión telefónica tal como la proporciona principalmente la red. El tipo de medio de una llamada es una indicación del tipo de flujo de información que se intercambia en esa llamada. El módem de fax o de datos del grupo 3 son tipos de medios que usan una llamada con un modo de portador de voz 3,1 kHz.

Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en la línea y no usar este \_ valor de LINEMEDIAMODE si no se admite en la versión negociada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




