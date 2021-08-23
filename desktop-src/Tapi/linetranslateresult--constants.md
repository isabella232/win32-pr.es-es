---
description: Las constantes de marca de bits LINETRANSLATERESULT \_ describen varios resultados de una traducción de direcciones.
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: LINETRANSLATERESULT_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba28c04bc52d3857d76bffefed5fe07803954e72f4a5e7e05ffa22d4ee6c646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518785"
---
# <a name="linetranslateresult_-constants"></a>Constantes LINETRANSLATERESULT \_

Las constantes de marca de bits **LINETRANSLATERESULT \_** describen varios resultados de una traducción de direcciones.

<dl> <dt>

<span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT \_ CANONICAL**
</dt> <dd> <dl> <dt>



Indica que la cadena de entrada tenía un formato canónico válido.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT \_ DIALBILLING**
</dt> <dd> <dl> <dt>



Indica que la dirección devuelta contiene un valor "$".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>



Indica que la dirección devuelta contiene una "W".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



Indica que la dirección devuelta contiene un "?".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Indica que la dirección devuelta contiene una "@".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT \_ INTERNATIONAL**
</dt> <dd> <dl> <dt>



Indica que la llamada se está tratando como una llamada internacional (el código de país o región especificado en la dirección de destino es diferente del código de país o región especificado para **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT \_ INTOLLLIST**
</dt> <dd> <dl> <dt>



Indica que la llamada local se marca como de larga distancia porque el país o región tiene llamadas de peaje y el prefijo aparece en **TollPrefixList** de **CurrentLocation**.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT \_ LOCAL**
</dt> <dd> <dl> <dt>



Indica que la llamada se está tratando como una llamada local (el código de país o región y el código de área especificados en la dirección de destino son los mismos que los especificados para **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT \_ LONGDISTANCE**
</dt> <dd> <dl> <dt>



Indica que la llamada se está tratando como una llamada de larga distancia (el código de país o región especificado en la dirección de destino es el mismo, pero el código de área es diferente de los especificados para **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT \_ NOTINTOLLLIST**
</dt> <dd> <dl> <dt>



Indica que el país o región admite llamadas de peaje, pero el prefijo no aparece en **TollPrefixList,** por lo que la llamada se marca como una llamada local. Tenga en cuenta que si INTOLLIST y NOTINTOLLIST están desactivados, el país o región actual no admite prefijos de peaje y los elementos de la interfaz de usuario relacionados con los prefijos de peaje no deben presentarse al usuario; Si este tipo de bit está activado, el país o región admite listas de peaje y se deben habilitar los elementos de la interfaz de usuario relacionados.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT \_ NOTRANSLATION**
</dt> <dd> <dl> <dt>



Indica que la traducción de direcciones no está disponible. Este elemento solo se expone a las aplicaciones que negocian una versión tapi de la versión 3.0 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT \_ VOICEDETECT**
</dt> <dd> <dl> <dt>



Indica que la dirección que se puede marcar devuelta contiene un ":". Este elemento solo se expone a las aplicaciones que negocian una versión TAPI de 2.0 o posterior.

> [!Note]  
> El carácter ":" (dos puntos) se agregará a la lista de caracteres que se pueden incrustar en una cadena que se puede marcar y pasar a las direcciones de destino. Si se intenta pasar desde una aplicación a un dispositivo de línea que admita una versión de API anterior a la 2.0, lo más probable es que se deba a LINEERR INVALADDRESS o, posiblemente, que el carácter se ignore por \_ completo. El significado de este carácter es "Pausar hasta que se detecte un aviso de voz y, a continuación, continuar marcando". está diseñado para su uso al marcar automáticamente en sistemas que dan avisos de voz, como procesadores de tarjetas de llamadas de larga distancia.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




