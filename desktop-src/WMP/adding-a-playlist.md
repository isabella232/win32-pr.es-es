---
title: Agregar una lista de reproducción
description: Agregar una lista de reproducción
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- crear máscaras, listas de reproducción
- Máscaras de Windows Media Player, listas de reproducción
- máscaras, listas de reproducción
- listas de reproducción, máscaras
- listas de reproducción de metarchivos, máscaras
- Listas de reproducción de metarchivos de Windows Media, máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695404"
---
# <a name="adding-a-playlist"></a>Agregar una lista de reproducción

Puede usar listas de reproducción para elegir entre las recopilaciones de audio y vídeo.

Con la ilustración de la primera máscara, puede realizar algunos cambios en el archivo de definición de máscara.

El primer paso es usar el shell que usará para la mayoría de las máscaras:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



Ahora, agregue una segunda **vista** que contenga una lista de reproducción. Coloque el código siguiente después del </VIEW> del código de Shell.


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



Tendrá que dar un identificador a esta segunda vista para poder hacer referencia a ella más adelante. Agregue un PLAYELEMENT y un STOPELEMENT. Estos botones predefinidos facilitan la vida.


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



Por último, agregue un evento onClick a PLAYELEMENT para mostrar una lista de reproducción en la segunda vista:


```C++
            onClick = "JScript: theme.openView('playview');" />

```



Puede ver una máscara de lista de reproducción en funcionamiento similar en la sección de ejemplo del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de creación de máscaras**](skin-creation-guide.md)
</dt> </dl>

 

 




