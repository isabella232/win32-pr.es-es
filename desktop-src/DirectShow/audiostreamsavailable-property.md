---
description: La propiedad AudioStreamsAvailable recupera el número de secuencias de audio disponibles en el título actual.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Propiedad AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906548"
---
# <a name="audiostreamsavailable-property"></a>Propiedad AudioStreamsAvailable

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `AudioStreamsAvailable` propiedad recupera el número de secuencias de audio disponibles en el título actual.

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero comprendido entre 1 y 8 que representa el número de secuencias de audio disponibles en el título actual.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado. El uso principal de varias secuencias de audio es proporcionar bandas sonoras de películas en más de un idioma. Normalmente, no todos los títulos de un disco tienen habilitadas todas las secuencias de audio. Por ejemplo, la película de características podría tener bandas sonoras en tres idiomas diferentes, pero los finalizadores podrían tener solo una banda de reproducción en inglés. Para que un usuario pueda seleccionar un flujo, la aplicación debe determinar qué secuencias están disponibles en el título actual. Tenga en cuenta que los flujos concretos se identifican mediante un índice de cero a 7.

Normalmente, los discos presentan un menú que muestra las bandas sonoras disponibles, lo que permite al usuario seleccionar la secuencia de audio que se va a habilitar.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> </dl>

 

 



