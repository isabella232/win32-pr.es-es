---
title: Adición de vídeo
description: Adición de vídeo
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- crear máscaras,vídeo
- Reproductor de Windows Media máscaras,vídeo
- máscaras, vídeo
- vídeo en máscaras, agregar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099778395146cb0bf0f27b483d55dd75c0fb8a0b28b879cc2d388f8e8cb7ba75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055413"
---
# <a name="adding-video"></a>Adición de vídeo

Puede agregar un vídeo al archivo simplemente con el elemento **VIDEO** y definir dónde desea colocar la ventana de vídeo.

Use el mismo código que hizo en la sección Elegir archivos; Todo lo que necesita hacer es agregar el elemento **VIDEO** con los atributos superior, izquierdo, ancho y alto.


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



Después, al reproducir un vídeo, se mostrará en la ventana. El arte del ejemplo de vídeo se modificó para crear una máscara ligeramente mayor. Dado que las capas se usaron en Photoshop, los botones se movieron fácilmente y se creó un nuevo conjunto muy rápidamente. Solo se cambió la imagen de fondo. Se usó un relleno en una capa en blanco y se agregó un efecto bisel y relieve.

Puede ver una máscara de vídeo de trabajo similar en la sección de ejemplo del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de creación de máscaras**](skin-creation-guide.md)
</dt> </dl>

 

 




