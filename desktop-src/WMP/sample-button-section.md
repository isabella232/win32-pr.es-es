---
title: Sección de botón de ejemplo
description: Sección de botón de ejemplo
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Reproductor de Windows Media Máscaras móviles, sección Botón
- skins,Button section
- referencia de máscaras, sección Button
- botones en máscaras, sección Botón
- archivos de definición de máscara, sección Botón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c35a4efd0e52dd7f5fd0cf87fc269eb4a9f4c27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476172"
---
# <a name="sample-button-section"></a>Sección de botón de ejemplo

Las líneas siguientes muestran una sección típica de botones de un archivo de definición de máscara:


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
-   Orden aleatorio, repetición y movimiento por la lista de reproducción.
-   Silenciar el volumen.

Todos los botones excepto el botón de exclusión mutua son botones de región. El botón de exclusión mutua obtiene sus imágenes Pushed y Disabled del mapa de bits Super para mayor comodidad.

> [!Note]  
> Los tipos de botones están en desuso en máscaras Reproductor de Windows Media 10 Mobile o posterior. En lugar de un tipo de botón declarado en el archivo de máscara, escriba "NA" para cada tipo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




