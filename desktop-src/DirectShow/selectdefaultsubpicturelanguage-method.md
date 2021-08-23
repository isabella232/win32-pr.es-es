---
description: El método SelectDefaultSubpictureLanguage establece el lenguaje de subimagen predeterminado actual en el objeto MSWebDVD.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: SelectDefaultSubpictureLanguage (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aaa6b927d33626299258ac54136e1a67b0dedb40427a35d9c79465be3e9a15d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072589"
---
# <a name="selectdefaultsubpicturelanguage-method"></a>SelectDefaultSubpictureLanguage (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SelectDefaultSubpictureLanguage` método establece el lenguaje de subimagen predeterminado actual en el objeto **MSWebDVD.**

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

Especifica la extensión de lenguaje de subimagen como un entero.



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



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La extensión de lenguaje de subpicture proporciona más información sobre la subpicture.

 

 



