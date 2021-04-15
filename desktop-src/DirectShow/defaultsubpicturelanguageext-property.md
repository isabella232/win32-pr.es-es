---
description: La propiedad DefaultSubpictureLanguageExt recupera la extensión de idioma de subimagen de DVD predeterminada.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Propiedad DefaultSubpictureLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536712"
---
# <a name="defaultsubpicturelanguageext-property"></a>Propiedad DefaultSubpictureLanguageExt

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DefaultSubpictureLanguageExt` propiedad recupera la extensión de idioma de subimagen de DVD predeterminada.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que indica la extensión de idioma de subimagen de DVD predeterminada.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado. En la siguiente tabla se muestran los valores posibles.



| Valor | Descripción                    |
|-------|--------------------------------|
| 0     | No se ha especificado la extensión        |
| 1     | Leyendas normales                |
| 2     | Leyendas grandes                   |
| 3     | Títulos de los elementos secundarios            |
| 5     | Subtítulos normales cerrados         |
| 6     | Subtítulos Big Closed            |
| 7     | Subtítulos (CC) de los niños     |
| 9     | Forzado                         |
| 13    | Comentarios del Director normal     |
| 14    | Comentarios del Big Director        |
| 15    | Comentarios de Director's de los niños |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**SelectDefaultSubpictureLanguage**](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



