---
description: La propiedad DefaultAudioLanguageExt recupera la extensión predeterminada del lenguaje de audio DVD.
ms.assetid: 628af2aa-e528-4689-953b-558e13e1d513
title: Propiedad DefaultAudioLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03423e6dda19563b55845662f7af5b21df00802726b279068a40c847aa6fc5e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953114"
---
# <a name="defaultaudiolanguageext-property"></a>Propiedad DefaultAudioLanguageExt

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DefaultAudioLanguageExt` propiedad recupera la extensión predeterminada del lenguaje de audio DVD.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultAudioLanguageExt
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que indica la extensión de lenguaje de audio predeterminada. Vea Comentarios para ver los valores posibles.

## <a name="remarks"></a>Comentarios

Esta propiedad es de solo lectura sin ningún valor predeterminado. En la tabla siguiente se muestran los valores posibles para las extensiones de lenguaje de audio de DVD.



| Value | Descripción       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Subtítulos          |
| 2     | VisualmenteAmpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

 

 



