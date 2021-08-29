---
description: La propiedad DefaultSubpictureLanguageExt recupera la extensión de lenguaje de subpicture de DVD predeterminada.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Propiedad DefaultSubpictureLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55dbf4bac4a5fb66e369c67e986c064112826c2184dcd5df1d858235632cba98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102995"
---
# <a name="defaultsubpicturelanguageext-property"></a>Propiedad DefaultSubpictureLanguageExt

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DefaultSubpictureLanguageExt` propiedad recupera la extensión de lenguaje de subpicture de DVD predeterminada.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor Entero que indica la extensión predeterminada del lenguaje de subimagen de DVD.

## <a name="remarks"></a>Comentarios

Esta propiedad es de solo lectura sin ningún valor predeterminado. En la siguiente tabla se muestran los valores posibles.



| Valor | Descripción                    |
|-------|--------------------------------|
| 0     | Extensión no especificada        |
| 1     | Títulos normales                |
| 2     | Títulos grandes                   |
| 3     | Títulos de los niños            |
| 5     | Subtítulos normales         |
| 6     | Subtítulos grandes            |
| 7     | Subtítulos de los niños     |
| 9     | Forzado                         |
| 13    | Comentarios del director normal     |
| 14    | Comentarios de big director        |
| 15    | Comentarios del director de los hijos |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**SeleccioneDefaultSubpictureLanguage**](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



