---
description: El método PlayChapterInTitle reproduce el capítulo especificado en el título especificado.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Método PlayChapterInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407684ecf8db6053a4d166a4ed069f9cabf0b36f983dd04bfdf9cf85e6c8dc2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830875"
---
# <a name="playchapterintitle-method"></a>Método PlayChapterInTitle

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `PlayChapterInTitle` método reproduce el capítulo especificado en el título especificado.

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica el título como un valor entero.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Especifica el capítulo como un valor entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método inicia la reproducción en el capítulo especificado y, a continuación, continúa reproduciendo indefinidamente. Si solo desea reproducir un capítulo determinado, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).

 

 



