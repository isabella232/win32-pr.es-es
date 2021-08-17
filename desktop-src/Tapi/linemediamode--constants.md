---
description: Las constantes LINEMEDIAMODE \_ describen los tipos de medios (o modos) de una sesión o llamada de comunicaciones.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: LINEMEDIAMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c11e40a81fffc967afd534ce6de591b524d835cbe97a919903bd97b1eeb4daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140018"
---
# <a name="linemediamode_-constants"></a>LineMEDIAMODE \_ (Constantes)

Las **constantes \_ LINEMEDIAMODE** describen los tipos de medios (o modos) de una sesión o llamada de comunicaciones.

<dl> <dt>

<span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**
</dt> <dd> <dl> <dt>



La energía de voz se detectó en la llamada y la voz se controla localmente mediante una aplicación automatizada, como con una aplicación de máquina de respuesta. Cuando un proveedor de servicios no puede distinguir entre la voz interactiva y la automatizada en una llamada entrante, la llamará como voz interactiva.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAMODEM**
</dt> <dd> <dl> <dt>



Una sesión de módem de datos en la llamada. Los protocolos de módem actuales requieren que la estación llamada inicie el protocolo de enlace. En el caso de una llamada de módem de datos entrante, la aplicación normalmente no puede realizar ninguna detección positiva. La forma en que el proveedor de servicios toma esta determinación es su elección. Por ejemplo, un período de silencio justo después de responder a una llamada entrante se puede usar como heurística para decidir que podría ser una llamada de módem de datos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**
</dt> <dd> <dl> <dt>



Una sesión adsi (interfaz de servicios de visualización análoga) en la llamada. ADSI mejora las llamadas de voz con información alfanumérica descargada en el teléfono y el uso de botones de software en el teléfono.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE \_ DIGITALDATA**
</dt> <dd> <dl> <dt>



Flujo de datos digital de formato no especificado.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE \_ G3FAX**
</dt> <dd> <dl> <dt>



Se envía o recibe un fax del grupo 3 a través de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE \_ G4FAX**
</dt> <dd> <dl> <dt>



Se envía o recibe un fax del grupo 4 a través de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE \_ INTERACTIVEVOICE**
</dt> <dd> <dl> <dt>



Se detectó energía de voz en la llamada y la llamada se controla como una llamada de voz interactiva con humanos en ambos extremos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ MIXED**
</dt> <dd> <dl> <dt>



Una sesión mixta en la llamada. Mixed es uno de los servicios telemáticos de ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**
</dt> <dd> <dl> <dt>



Una sesión de TDD (dispositivos de telefonía para el dispositivos de voz) en la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ TELETEX**
</dt> <dd> <dl> <dt>



Una sesión de Teletex en la llamada. Teletex es uno de los servicios telemáticos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE \_ TELEX**
</dt> <dd> <dl> <dt>



Una sesión de telex en la llamada. Telex es uno de los servicios telemáticos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**VÍDEO \_ LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



El tipo de medio de la llamada es vídeo. (TAPI versiones 2.1 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**
</dt> <dd> <dl> <dt>



Una sesión de vídeotex en la llamada. Videotex es uno de los servicios telemáticos.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE \_ VOICEVIEW**
</dt> <dd> <dl> <dt>



El tipo de medio de la llamada es VoiceView. (TAPI versiones 1.4 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Existe una secuencia multimedia, pero su modo no se conoce actualmente y puede conocerse más adelante. Esto correspondería a una llamada con un tipo de medio sin clasificar. En entornos típicos de telefonía análoga, el tipo de medio de una llamada entrante puede ser desconocido hasta que se haya respondido a la llamada y se haya filtrado el flujo multimedia para tomar una determinación.

Si se establece la marca de modo multimedia desconocido, también se pueden establecer otras marcas multimedia. Esto se usa para indicar que el medio es desconocido, pero que es probable que sea uno de los otros tipos de medios seleccionados.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Los 32 bits están reservados.

Tenga en cuenta que el modo de portador y el tipo de medio son nociones diferentes. El modo de portador de una llamada es una indicación de la calidad de la conexión telefónica proporcionada principalmente por la red. El tipo de medio de una llamada es una indicación del tipo de flujo de información que se intercambia a través de esa llamada. El fax o el módem de datos del grupo 3 son tipos de medios que usan una llamada con un modo de portador de voz de 3,1 kHz.

Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión negociada de la API en la línea y no usar este valor LINEMEDIAMODE si no se admite en la versión \_ negociada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




