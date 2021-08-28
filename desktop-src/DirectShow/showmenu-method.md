---
description: El método ShowMenu muestra el menú especificado en la pantalla.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: ShowMenu (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb9135e2999675dc46774f15ee79afd835085b40fe210d0ca1cfd173f8a99fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050515"
---
# <a name="showmenu-method"></a>ShowMenu (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `ShowMenu` método muestra el menú especificado en la pantalla.

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*
</dt> <dd>

Especifica el identificador de menú como entero.



| Value | Descripción |
|-------|-------------|
| 2     | Title (Top) |
| 3     | Root        |
| 4     | Subimagen  |
| 5     | Audio       |
| 6     | Ángulo       |
| 7     | Capítulo     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Los nombres de menú de DVD pueden resultar un poco confusos. El menú de título es otro nombre para el menú administrador de vídeo, el menú principal de todo el disco; por lo general, enumera todos los conjuntos de títulos de vídeo disponibles en el disco. El menú raíz es el menú de un conjunto de títulos de vídeo, que puede contener un título o un grupo de títulos. Todos los títulos de un conjunto de títulos comparten los mismos menús Subpicture, Audio y Angle.

 

 



