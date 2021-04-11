---
description: El método PlayChaptersAutoStop inicia la reproducción en el capítulo especificado en el título especificado y el número de capítulos especificados.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Método PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274692"
---
# <a name="playchaptersautostop-method"></a>Método PlayChaptersAutoStop

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `PlayChaptersAutoStop` método inicia la reproducción en el capítulo especificado en el título especificado y para el número de capítulos especificado.

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica el título como valor entero.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Especifica el capítulo Inicio como valor entero.

</dd> <dt>

<span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*
</dt> <dd>

Especifica el número de capítulos que se reproducirán como valor entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En el momento en que se ha reproducido el último capítulo, este método hace que se envíe a la aplicación una notificación de evento de [**\_ \_ \_ reparo de capítulos del DVD**](ec-dvd-chapter-autostop.md) de la CE.

 

 



