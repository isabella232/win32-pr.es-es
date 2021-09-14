---
title: Adición de visualizaciones
description: Adición de visualizaciones
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- crear máscaras, visualizaciones
- Reproductor de Windows Media máscaras, visualizaciones
- máscaras, visualizaciones
- visualizaciones, máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890180"
---
# <a name="adding-visualizations"></a>Adición de visualizaciones

Puede agregar una ventana de visualización de la misma manera que agregó una ventana de vídeo. Se puede usar la misma máscara, pero se **usa un elemento EFFECTS.**

En primer lugar, debe agregar **el elemento EFFECTS** y darle un identificador y un tamaño:


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



A continuación, puede asignar a los dos botones una cadena de código de visualización anterior y siguiente:


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



Las capas y los mapas de bits eran los mismos que se usaban en el ejemplo de vídeo, salvo que la flecha de reproducción se copiaba y volteó horizontalmente.

Por último, se ha agregado un elemento **PLAYER** sencillo con el atributo **URL** para elegir una canción para reproducir.


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

 

 




