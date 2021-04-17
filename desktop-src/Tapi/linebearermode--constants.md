---
description: Las \_ constantes de marcador de bits LINEBEARERMODE describen diferentes modos de portador de una llamada.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: Constantes de LINEBEARERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690968"
---
# <a name="linebearermode_-constants"></a>Constantes de LINEBEARERMODE \_

Las constantes de marcador de bits **LINEBEARERMODE \_** describen diferentes modos de portador de una llamada. Cuando una aplicación realiza una llamada, puede solicitar un modo de portador específico. Estos modos se usan para seleccionar una calidad de servicio determinada para la conexión solicitada desde la red telefónica subyacente. Los modos de portador disponibles en una línea determinada son la capacidad del dispositivo de la línea.

<dl> <dt>

<span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**
</dt> <dd> <dl> <dt>



La transferencia alternativa de voz o datos sin restricciones en la misma llamada (ISDN).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**datos de LINEBEARERMODE \_**
</dt> <dd> <dl> <dt>



La transferencia de datos sin restricciones en la llamada. La velocidad de datos se especifica por separado.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ multiuso**
</dt> <dd> <dl> <dt>



Modo multiuso definido por ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**
</dt> <dd> <dl> <dt>



Esto corresponde a una conexión de señalización no asociada a la llamada desde la aplicación al proveedor o el conmutador de servicio (tratado como una secuencia de medios por TAPI).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**acceso \_ directo de LINEBEARERMODE**
</dt> <dd> <dl> <dt>



Cuando una llamada está activa en LINEBEARERMODE \_ PASSTHROUGH, el proveedor de servicios proporciona acceso directo al hardware asociado para que la aplicación lo controle. Este modo lo usan principalmente las aplicaciones que quieren un control directo temporal sobre los módems asincrónicos, a los que se accede a través de las [funciones de comunicaciones](/windows/desktop/DevIO/communications-functions)con el fin de configurar o usar características especiales que no admite el proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**
</dt> <dd> <dl> <dt>



Servicio de portador para datos digitales en los que solo los siete bits de orden inferior de cada octeto pueden contener datos de usuario (por ejemplo, para el servicio 56Kbit/s conmutado).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE \_ Speech**
</dt> <dd> <dl> <dt>



Esto corresponde a la transmisión de voz G. 711 en la llamada. La red puede usar técnicas de procesamiento como la transmisión analógica, la cancelación de eco y la compresión/descompresión. No se garantiza la integridad de bits. La voz no está diseñada para admitir los tipos de medios de fax y módem.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ Voice**
</dt> <dd> <dl> <dt>



Se trata de un servicio de portador de nivel sonoro analógico de 3,1 kHz. No se garantiza la integridad de bits. La voz puede admitir tipos de medios de fax y módem.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Tenga en cuenta que el modo de portador y el tipo de medio son nociones diferentes. El modo de portador de una llamada es una indicación de la calidad de la conexión telefónica tal como la proporciona principalmente la red. El tipo de medio de una llamada es una indicación del tipo de flujo de información que se intercambia en esa llamada. El módem de fax o de datos del grupo 3 son tipos de medios que usan una llamada con un modo de portador de voz 3,1 kHz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

