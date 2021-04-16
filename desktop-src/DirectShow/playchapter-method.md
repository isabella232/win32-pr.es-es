---
description: El método PlayChapter inicia la reproducción del capítulo especificado en el título actual.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Método PlayChapter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686271"
---
# <a name="playchapter-method"></a>Método PlayChapter

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `PlayChapter` método inicia la reproducción del capítulo especificado en el título actual.

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Especifica el índice del capítulo en el título actual como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando se alcanza el final del capítulo especificado, este método continúa reproduciendo capítulos posteriores, si existen. Si solo quiere reproducir un capítulo especificado, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlayChapterInTitle**](playchapterintitle-method.md)
</dt> </dl>

 

 



