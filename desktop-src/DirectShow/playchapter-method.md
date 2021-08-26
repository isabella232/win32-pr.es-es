---
description: El método PlayChapter inicia la reproducción desde el capítulo especificado dentro del título actual.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Método PlayChapter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832b1da6940b26a3cc3a4ab5bdba8653806966f8a399b74eb5adf50600e22293
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102347"
---
# <a name="playchapter-method"></a>Método PlayChapter

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `PlayChapter` método inicia la reproducción desde el capítulo especificado dentro del título actual.

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Especifica el índice de capítulo del título actual como entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cuando se alcanza el final del capítulo especificado, este método continúa reproduciendo capítulos posteriores, si existe alguno. Si solo desea reproducir un capítulo especificado, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlayChapterInTitle**](playchapterintitle-method.md)
</dt> </dl>

 

 



