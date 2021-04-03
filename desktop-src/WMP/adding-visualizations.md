---
title: Agregar visualizaciones
description: Agregar visualizaciones
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- crear máscaras, visualizaciones
- Máscaras de Windows Media Player, visualizaciones
- máscaras, visualizaciones
- visualizaciones, máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776321"
---
# <a name="adding-visualizations"></a>Agregar visualizaciones

Puede Agregar una ventana de visualización de la misma manera que agregó una ventana de vídeo. Se puede usar la misma máscara, pero se usa un elemento **Effects** .

En primer lugar, debe agregar el elemento **Effects** y asignarle un identificador y un tamaño:


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



A continuación, puede asignar los dos botones a una cadena de código de visualización anterior y siguiente:


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



Las capas y los mapas de bits eran los mismos que se usaron en el ejemplo de vídeo, con la excepción de que se ha copiado y volteado horizontalmente la flecha de reproducción.

Por último, se ha agregado un elemento **Player** simple con el atributo **URL** para elegir la canción que se va a reproducir.


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



Puede ver una máscara de visualización de trabajo similar en la sección de ejemplo del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de creación de máscaras**](skin-creation-guide.md)
</dt> </dl>

 

 




