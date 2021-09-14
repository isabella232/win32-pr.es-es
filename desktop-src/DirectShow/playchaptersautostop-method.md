---
description: El método PlayChaptersAutoStop inicia la reproducción en el capítulo especificado del título especificado y en el número de capítulos especificado.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Método PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060987"
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

## <a name="remarks"></a>Observaciones

Cuando se reproduce el último capítulo, este método hace que se envíe una notificación de eventos [**\_ EC DVD CHAPTER \_ \_ AUTOSTOP**](ec-dvd-chapter-autostop.md) a la aplicación.

 

 



