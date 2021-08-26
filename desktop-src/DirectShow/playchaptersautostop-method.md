---
description: El método PlayChaptersAutoStop inicia la reproducción en el capítulo especificado del título especificado y en el número de capítulos especificado.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Método PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58c518496f81f4ca4e662bf8dbc821f2378cd38d27c7546356144910c0c5ba72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830745"
---
# <a name="playchaptersautostop-method"></a>Método PlayChaptersAutoStop

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método inicia la reproducción en el capítulo especificado del título especificado y en el `PlayChaptersAutoStop` número de capítulos especificado.

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica el título como un valor entero.

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

Especifica el capítulo inicial como un valor entero.

</dd> <dt>

<span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*
</dt> <dd>

Especifica el número de capítulos que se reproducirán como un valor entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cuando se reproduce el último capítulo, este método hace que se envíe una notificación de eventos [**\_ EC DVD CHAPTER \_ \_ AUTOSTOP**](ec-dvd-chapter-autostop.md) a la aplicación.

 

 



