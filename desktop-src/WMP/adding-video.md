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
ms.openlocfilehash: 0cc952f2fa80536bc6b2bb9ef3b43c6730616af3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890204"
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

 

 




