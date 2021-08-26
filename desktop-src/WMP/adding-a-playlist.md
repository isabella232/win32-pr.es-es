---
title: Agregar una lista de reproducción
description: Agregar una lista de reproducción
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- crear máscaras, listas de reproducción
- Reproductor de Windows Media máscaras,listas de reproducción
- máscaras, listas de reproducción
- listas de reproducción, máscaras
- listas de reproducción de metarchivo, máscaras
- Windows Listas de reproducción de metarchivo multimedia, máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23d9198f1f913b83cef40cea9f6ec47976f9f1e08a5e54257ab16df63e538b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031595"
---
# <a name="adding-a-playlist"></a>Agregar una lista de reproducción

Puede usar listas de reproducción para elegir entre colecciones de audio y vídeo.

Con las ilustraciones de la primera máscara, puede realizar algunos cambios en el archivo de definición de máscara.

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



Ahora agregue una segunda **vista**, que contiene una lista de reproducción. Coloque el código siguiente después del </VIEW> del código de shell.


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



Tendrá que proporcionar a esta segunda vista un identificador para que pueda hacer referencia a ella más adelante. Agregue un ELEMENTO PLAYELEMENT y un ELEMENTO STOPELEMENT. Estos botones predefinidos facilitan la vida.


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



Puede ver una máscara de lista de reproducción de trabajo similar en la sección de ejemplo del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de creación de máscaras**](skin-creation-guide.md)
</dt> </dl>

 

 




