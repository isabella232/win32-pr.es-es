---
title: EQUALIZERSETTINGS.speakerSize
description: El atributo speakerSize especifica o recupera el número de índice del tamaño actual del hablante.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS.speakerSize Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d289a89a22e8c10cf669e9b55fc304826acb3ce0f72468f725e7d5fae0dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748653"
---
# <a name="equalizersettingsspeakersize"></a>EQUALIZERSETTINGS.speakerSize

El **atributo speakerSize** especifica o recupera el número de índice del tamaño actual del hablante.

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de **lectura** y escritura (long) que contiene uno de los valores siguientes.



| Value | Descripción                              |
|-------|------------------------------------------|
| 0     | Los hablantes actuales son auriculares.     |
| 1     | Los hablantes actuales tienen un tamaño normal. |
| 2     | Los altavoces actuales son grandes.          |



 

## <a name="remarks"></a>Comentarios

El nombre descriptivo del tamaño del altavoz se puede recuperar mediante el **atributo currentSpeakerName.**

Este atributo se omite si **enhancedAudio** está establecido en false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.currentSpeakerName**](equalizersettings-currentspeakername.md)
</dt> <dt>

[**EQUALIZERSETTINGS.enhancedAudio**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





