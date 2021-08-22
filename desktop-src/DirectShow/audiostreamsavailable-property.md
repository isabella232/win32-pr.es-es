---
description: La propiedad AudioStreamsAvailable recupera el número de secuencias de audio disponibles en el título actual.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Propiedad AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07025a3a3bf54ad98d32c54ee3c147bc36489822ef451965e1e0e0da8fe586c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586735"
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

## <a name="remarks"></a>Comentarios

Esta propiedad es de solo lectura sin ningún valor predeterminado. El uso principal de varias secuencias de audio es proporcionar grabaciones de películas en más de un idioma. Normalmente, no todos los títulos de un disco tienen todas las secuencias de audio habilitadas. Por ejemplo, la película de características podría tener escenarios en tres idiomas diferentes, pero es posible que los finalizadores solo tengan un idioma inglés. Para que un usuario pueda seleccionar una secuencia, la aplicación debe determinar qué secuencias están disponibles en el título actual. Tenga en cuenta que determinados flujos se identifican mediante un índice de cero a 7.

Los discos suelen presentar un menú en el que se muestran los elementos disponibles, lo que permite al usuario seleccionar la secuencia de audio que desea habilitar.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> </dl>

 

 



