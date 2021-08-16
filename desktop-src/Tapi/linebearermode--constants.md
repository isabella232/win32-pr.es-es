---
description: Las constantes de marca de bits LINEBEARERMODE describen diferentes modos \_ de portador de una llamada.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: LINEBEARERMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bb03664b6e904cbce7e376eb111675430ea86b8e6880211d76d5b364467097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761786"
---
# <a name="linebearermode_-constants"></a>LineBEARERMODE \_ (Constantes)

Las constantes de marca de bits **LINEBEARERMODE \_** describen diferentes modos de portador de una llamada. Cuando una aplicación realiza una llamada, puede solicitar un modo de portador específico. Estos modos se usan para seleccionar una determinada calidad de servicio para la conexión solicitada desde la red telefónica subyacente. Los modos de portador disponibles en una línea determinada son una funcionalidad del dispositivo de la línea.

<dl> <dt>

<span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**
</dt> <dd> <dl> <dt>



La transferencia alternativa de voz o datos sin restricciones en la misma llamada (ISDN).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**LINEBEARERMODE \_ DATA**
</dt> <dd> <dl> <dt>



Transferencia de datos sin restricciones en la llamada. La velocidad de datos se especifica por separado.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ MULTIUSE**
</dt> <dd> <dl> <dt>



Modo multiuso definido por ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**
</dt> <dd> <dl> <dt>



Esto corresponde a una conexión de señalización no asociada a la llamada desde la aplicación al proveedor de servicios o al conmutador (tratado como un flujo multimedia por TAPI).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE \_ PASSTHROUGH**
</dt> <dd> <dl> <dt>



Cuando una llamada está activa en LINEBEARERMODE PASSTHROUGH, el proveedor de servicios proporciona acceso directo al hardware conectado para que la aplicación \_ lo controle. Este modo lo usan principalmente las aplicaciones que dese el control directo temporal sobre los módems asincrónicos, a los que se accede a través de las funciones de comunicaciones [,](/windows/desktop/DevIO/communications-functions)con el fin de configurar o usar características especiales que el proveedor de servicios no admite de otro modo.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**
</dt> <dd> <dl> <dt>



Servicio de portador para datos digitales en el que solo los siete bits de orden inferior de cada octeto pueden contener datos de usuario (por ejemplo, para el servicio conmutado de 56 kbits/s).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE \_ SPEECH**
</dt> <dd> <dl> <dt>



Esto corresponde a la transmisión de voz G.711 en la llamada. La red puede usar técnicas de procesamiento como la transmisión análoga, la cancelación de eco y la compresión y descompresión. La integridad de bits no está garantizada. La voz no está pensada para admitir los tipos de medios de fax y módem.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ VOICE**
</dt> <dd> <dl> <dt>



Se trata de un servicio de portador de nivel de voz análogo normal de 3,1 kHz. La integridad de bits no está garantizada. La voz puede admitir tipos de medios de fax y módem.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Tenga en cuenta que el modo de portador y el tipo de medio son nociones diferentes. El modo de portador de una llamada es una indicación de la calidad de la conexión telefónica proporcionada principalmente por la red. El tipo de medio de una llamada es una indicación del tipo de flujo de información que se intercambia sobre esa llamada. El fax o el módem de datos del grupo 3 son tipos de medios que usan una llamada con un modo de portador de voz de 3,1 kHz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

