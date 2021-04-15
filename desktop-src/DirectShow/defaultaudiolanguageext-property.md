---
description: La propiedad DefaultAudioLanguageExt recupera la extensión de idioma de audio de DVD predeterminada.
ms.assetid: 628af2aa-e528-4689-953b-558e13e1d513
title: Propiedad DefaultAudioLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5ce89099cd8e31cde9beb8bb3c8a9f1e16b3b0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536874"
---
# <a name="defaultaudiolanguageext-property"></a>Propiedad DefaultAudioLanguageExt

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DefaultAudioLanguageExt` propiedad recupera la extensión de idioma de audio de DVD predeterminada.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultAudioLanguageExt
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que indica la extensión del idioma de audio predeterminado. Vea la sección Comentarios para ver los posibles valores.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado. En la tabla siguiente se muestran los valores posibles para las extensiones de lenguaje de audio de DVD.



| Value | Descripción       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Subtítulos          |
| 2     | VisuallyImpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

 

 



