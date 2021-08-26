---
title: Botones (Reproductor de Windows Media SDK)
description: Botones
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Reproductor de Windows Media Máscaras móviles, información general sobre botones
- máscaras, información general sobre botones
- referencia de máscaras, botones
- botones en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128c723c5b8bbac31c82a32060704bc892dfb7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885537"
---
# <a name="buttons-windows-media-player-sdk"></a>Botones (Reproductor de Windows Media SDK)

Querrá usar uno o varios botones en la máscara y cada botón debe definirse en el archivo de definición de máscara. Si no define un botón en esta sección, la máscara no podrá usarlo.

La sección de botones del archivo de definición de máscara comienza con esta línea:


```C++
[ Buttons ]

```



A continuación, debe agregar una o varias líneas que contengan información sobre cada uno de los botones de la máscara. Una línea típica podría ser:


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



Tenga en cuenta que este código debe escribirse como una línea que comience por "PlayPause" y termine con "Pushed @ 160,98".

Puede usar la siguiente plantilla para la sección Botón del archivo de definición de máscara:


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



De nuevo, tenga en cuenta que deben escribirse como líneas únicas, la primera empieza por "// Function" y termina con &lt; &gt; &lt; "Push 2 Image &gt; Src". La segunda línea comienza por "// ----------" y termina con "------------------."

La información de los botones de cada línea de la sección Botón debe aparecer en el orden siguiente. Solo se requieren las seis primeras partes de la línea. Las imágenes secundarias no se incluyen a menos que sean necesarias.

1.  [Button (Función)](button-function.md)
2.  [Tipo de botón](button-type.md)
3.  [Ubicación del botón](button-location.md)
4.  [Origen de la imagen inserda](pushed-image-source.md)
5.  [Origen de la imagen para el botón Deshabilitado](image-source-for-disabled-button.md)
6.  [Color RGB de la pulsación](hit-rgb-color.md)
7.  [Origen de la imagen secundaria normal](normal-secondary-image-source.md)
8.  [Origen de la imagen terciaria normal](normal-tertiary-image-source.md)
9.  [Origen de la imagen secundaria inserda](pushed-secondary-image-source.md)
10. [Origen de imagen terciaria inserda](pushed-tertiary-image-source.md)

Para obtener un ejemplo de código de botón, vea [Sample Button Section](sample-button-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




