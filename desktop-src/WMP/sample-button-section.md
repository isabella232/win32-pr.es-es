---
title: Sección de botón de ejemplo
description: Sección de botón de ejemplo
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Aspectos de Windows Media Player Mobile, sección de botones
- aspectos, sección de botones
- referencia de las máscaras, sección de botones
- botones en máscaras, sección de botones
- archivos de definición de máscara, sección de botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c35a4efd0e52dd7f5fd0cf87fc269eb4a9f4c27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075965"
---
# <a name="sample-button-section"></a>Sección de botón de ejemplo

Las siguientes líneas muestran una sección típica de los botones de un archivo de definición de máscara:


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98
    Info       PushHit    97,49,43,43    Pushed @ 57,0     Disabled @ 57,0      0,  0,  0
    Stop       PushHit    97,173,43,43   Pushed @ 57,124   Disabled @ 57,124  255,255,  0
    Prev       PushHit    40,83,43,43    Pushed @ 0,34     Disabled @ 0,34      0,  0,255
    Next       PushHit    153,83,43,43   Pushed @ 113,34   Disabled @ 113,34  255,  0,  0
    Shuffle    ToggleHit  40,136,43,43   Pushed @ 0,87     Disabled @ 0,87      0,255,  0
    Repeat     ToggleHit  153,136,43,43  Pushed @ 113,87   Disabled @ 113,87  255,  0,255
    Mute       Toggle     5,220,24,23    Super @ 247,29    Super @ 4,28         0,  0,  0

```



Este código define ocho botones que se usan para proporcionar todas las funciones siguientes en una máscara:

-   Reproducir, pausar y detener elementos multimedia.
-   Orden aleatorio, repetir y desplazarse por la lista de reproducción.
-   Silenciar el volumen.

Todos los botones, excepto el botón silenciar, son botones de región. El botón silenciar obtiene las imágenes insertadas y deshabilitadas del súper mapa de bits para mayor comodidad.

> [!Note]  
> Los tipos de botones están en desuso en las máscaras de Windows Media Player 10 Mobile o posterior. En lugar de un tipo de botón declarado en el archivo de máscara, escriba "NA" para cada tipo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




