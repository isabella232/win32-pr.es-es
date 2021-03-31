---
title: Botones (SDK de Windows Media Player)
description: Botones
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Máscaras de Windows Media Player Mobile, información general sobre el botón
- aspectos, información general sobre los botones
- referencia de las máscaras, botones
- botones en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f06eb2fe21ee18a24f92e92d4fa760e9c76887
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149832"
---
# <a name="buttons-windows-media-player-sdk"></a>Botones (SDK de Windows Media Player)

Querrá usar uno o varios botones en la máscara y cada botón debe definirse en el archivo de definición de máscara. Si no define un botón en esta sección, la máscara no podrá utilizarlo.

La sección de botones del archivo de definición de máscara comienza con esta línea:


```C++
[ Buttons ]

```



A continuación, debe agregar una o más líneas que contengan información sobre cada uno de los botones de la máscara. Una línea típica podría ser:


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



Tenga en cuenta que este código debe escribirse como una línea que empieza por "PlayPause" y termina por "push @ 160, 98".

Puede usar la siguiente plantilla para la sección de botón del archivo de definición de máscara:


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



De nuevo, tenga en cuenta que deben escribirse como líneas únicas, la primera empezando por "// <Function> " y terminando por " &lt; Inserte 2 Image src &gt; ". La segunda línea comienza con "//----------" y termina con "------------------."

La información del botón para cada línea de la sección Button debe aparecer en el orden siguiente. Solo se requieren las seis primeras partes de la línea. Las imágenes secundarias no se incluyen a menos que sean necesarias.

1.  [Función Button](button-function.md)
2.  [Tipo de botón](button-type.md)
3.  [Ubicación del botón](button-location.md)
4.  [Origen de la imagen insertada](pushed-image-source.md)
5.  [Origen de imagen para botón deshabilitado](image-source-for-disabled-button.md)
6.  [Golpear color RGB](hit-rgb-color.md)
7.  [Origen de imagen secundaria normal](normal-secondary-image-source.md)
8.  [Origen de imagen terciario normal](normal-tertiary-image-source.md)
9.  [Origen de la imagen secundaria insertada](pushed-secondary-image-source.md)
10. [Origen de la imagen terciaria insertada](pushed-tertiary-image-source.md)

Para obtener un ejemplo de código de botón, consulte la [sección del botón de ejemplo](sample-button-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




