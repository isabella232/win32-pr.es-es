---
description: El método SelectDefaultSubpictureLanguage establece el idioma de subimagen predeterminado actual en el objeto MSWebDVD.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Método SelectDefaultSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805834"
---
# <a name="selectdefaultsubpicturelanguage-method"></a>Método SelectDefaultSubpictureLanguage

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SelectDefaultSubpictureLanguage` método establece el idioma de subimagen predeterminado actual en el objeto **MSWebDVD** .

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*
</dt> <dd>

Especifica el idioma como un entero.

</dd> <dt>

<span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*
</dt> <dd>

Especifica la extensión del lenguaje de subimagen como un entero.



| Value | Descripción                    |
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



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La extensión del lenguaje de subimagen proporciona más información acerca de la subimagen.

 

 



