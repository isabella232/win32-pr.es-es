---
title: EQUALIZERSETTINGS. Speaker
description: El atributo Speakers especifica o recupera el número de índice del tamaño actual del altavoz.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS. pone en altavoz Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699594"
---
# <a name="equalizersettingsspeakersize"></a>EQUALIZERSETTINGS. Speaker

El atributo **Speakers** especifica o recupera el número de índice del tamaño actual del altavoz.

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura y escritura (Long) que contiene uno de los valores siguientes.



| Value | Descripción                              |
|-------|------------------------------------------|
| 0     | Los altavoces actuales son auriculares.     |
| 1     | Los altavoces actuales tienen un tamaño normal. |
| 2     | Los altavoces actuales son grandes.          |



 

## <a name="remarks"></a>Observaciones

El nombre descriptivo del tamaño del altavoz se puede recuperar mediante el atributo **currentSpeakerName** .

Este atributo se omite si **enhancedAudio** está establecido en false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.currentSpeakerName**](equalizersettings-currentspeakername.md)
</dt> <dt>

[**EQUALIZERSETTINGS.enhancedAudio**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





