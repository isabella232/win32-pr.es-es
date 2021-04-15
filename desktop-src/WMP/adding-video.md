---
title: Agregar vídeo
description: Agregar vídeo
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- crear máscaras, vídeo
- Máscaras de Windows Media Player, vídeo
- máscaras, vídeo
- vídeo en máscaras, agregar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc952f2fa80536bc6b2bb9ef3b43c6730616af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695312"
---
# <a name="adding-video"></a>Agregar vídeo

Puede Agregar un vídeo al archivo simplemente mediante el elemento de **vídeo** y definiendo dónde desea colocar la ventana de vídeo.

Use el mismo código que en la sección elegir archivos; lo único que debe hacer es agregar el elemento de **vídeo** con los atributos superior, izquierdo, ancho y alto.


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



Cuando reproduzca un vídeo, se mostrará en la ventana. La imagen del ejemplo de vídeo se ha modificado para crear una máscara ligeramente más grande. Dado que las capas se usaron en Photoshop, los botones se movieron fácilmente y se creó un nuevo conjunto con mucha rapidez. Solo se ha cambiado la imagen de fondo. Se usó un relleno en una capa en blanco y se agregó un efecto de bisel y de relieve.

Puede ver una máscara de vídeo similar en la sección de ejemplo del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de creación de máscaras**](skin-creation-guide.md)
</dt> </dl>

 

 




