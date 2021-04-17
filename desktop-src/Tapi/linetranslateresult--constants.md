---
description: Las \_ constantes de marcador de bits LINETRANSLATERESULT describen varios resultados de una traducción de direcciones.
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: Constantes de LINETRANSLATERESULT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad10c3da2b4250ded5706e4aaa10b9b61f8739b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681214"
---
# <a name="linetranslateresult_-constants"></a>Constantes de LINETRANSLATERESULT \_

Las constantes de marcador de bits **LINETRANSLATERESULT \_** describen varios resultados de una traducción de direcciones.

<dl> <dt>

<span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**\_canónico LINETRANSLATERESULT**
</dt> <dd> <dl> <dt>



Indica que la cadena de entrada tiene un formato canónico válido.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT \_ DIALBILLING**
</dt> <dd> <dl> <dt>



Indica que la dirección devuelta contiene un "$".


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



Indica que la dirección devuelta contiene un "@".


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT \_ International**
</dt> <dd> <dl> <dt>



Indica que la llamada se está tratando como una llamada internacional (el código de país o región especificado en la dirección de destino es diferente del código de país o región especificado para el **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT \_ INTOLLLIST**
</dt> <dd> <dl> <dt>



Indica que la llamada local se está marcando como larga distancia porque el país o la región tiene llamada de peaje y el prefijo aparece en el **TollPrefixList** de **CurrentLocation**.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT \_ local**
</dt> <dd> <dl> <dt>



Indica que la llamada se está tratando como una llamada local (el código de país o región y el código de área especificados en la dirección de destino son los mismos que los especificados para el **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT \_ LONGDISTANCE**
</dt> <dd> <dl> <dt>



Indica que la llamada se está tratando como una llamada de larga distancia (el código de país o región especificado en la dirección de destino es el mismo, pero el código de área es diferente de los especificados para el **CurrentLocation**).


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT \_ NOTINTOLLLIST**
</dt> <dd> <dl> <dt>



Indica que el país o la región admite llamadas de peaje, pero el prefijo no aparece en **TollPrefixList**, por lo que la llamada se marca como una llamada local. Tenga en cuenta que, si tanto como inNOTINTOLLIST están desactivados, el país o la región actual no admiten prefijos de peaje y los elementos de la interfaz de usuario relacionados con prefijos de peaje no se deben presentar al usuario; Si este bit está activado, el país o la región admiten listas de peajes, y los elementos de la interfaz de usuario relacionados deben estar habilitados.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT \_ NOtranslation**
</dt> <dd> <dl> <dt>



Indica que la traducción de direcciones no está disponible. Este elemento solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT \_ VOICEDETECT**
</dt> <dd> <dl> <dt>



Indica que la dirección de marcado devuelta contiene un ":". Este elemento solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.

> [!Note]  
> El carácter ":" (dos puntos) se agregará a la lista de caracteres que se puede incrustar en una cadena de marcado y pasarse a las direcciones de destino. Si intenta pasarlo desde una aplicación a un dispositivo de línea que admita una versión de API anterior a 2,0, lo más probable es que LINEERR \_ INVALADDRESS, o que en el carácter se omita por completo. El significado de este carácter es "PAUSE hasta que se detecte un mensaje de voz y continúe marcando"; está pensada para su uso cuando se marca automáticamente en sistemas que proporcionan mensajes de voz, como procesadores de tarjetas de llamada a larga distancia.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




