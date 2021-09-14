---
description: La propiedad AudioStreamsAvailable recupera el número de secuencias de audio disponibles en el título actual.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Propiedad AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162186"
---
# <a name="audiostreamsavailable-property"></a>Propiedad AudioStreamsAvailable

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `AudioStreamsAvailable` propiedad recupera el número de secuencias de audio disponibles en el título actual.

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero de 1 a 8 que representa el número de secuencias de audio disponibles en el título actual.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura sin ningún valor predeterminado. El uso principal de varias secuencias de audio es proporcionar películas en más de un idioma. Normalmente, no todos los títulos de un disco tienen habilitadas todas las secuencias de audio. Por ejemplo, es posible que la película de características tenga escenarios en tres idiomas diferentes, pero es posible que los finalizadores solo tengan un idioma inglés. Para que un usuario pueda seleccionar una secuencia, la aplicación debe determinar qué secuencias están disponibles en el título actual. Tenga en cuenta que determinados flujos se identifican mediante un índice de cero a 7.

Por lo general, los discos presentan un menú que muestra los elementos disponibles, lo que permite al usuario seleccionar la secuencia de audio que se habilitará.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> </dl>

 

 



