---
title: Arte del álbum
description: Arte del álbum
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Reproductor de Windows Media Máscaras móviles, arte de álbum
- skins,album art
- referencia de máscaras, arte de álbum
- archivos de arte para máscaras, arte de álbum
- arte de álbum en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8183c7de25c891c59ef68f5938de532a66700400d916c3fc7610a761b2024d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865125"
---
# <a name="album-art"></a>Arte del álbum

Al crear una máscara para Reproductor de Windows Media 10 Mobile o posterior, es posible que quiera mostrar el arte del álbum relacionado con el elemento multimedia que se está reproduciendo actualmente. Al diseñar la máscara, querrá reservar espacio en la imagen de fondo para contener el arte del álbum.

La sección Album Art del archivo de definición de máscara debe comenzar con la siguiente línea:


```C++
[ Album Art ]

```



A continuación, debe agregar información que especifique la ubicación y el tamaño de la imagen del álbum en la máscara. Debe escribir cuatro enteros positivos, separados por comas que definan la izquierda, la parte superior, el ancho y el alto del arte del álbum, en píxeles, con respecto a la imagen de fondo. En el ejemplo siguiente se muestra cómo especificar dimensiones:


```C++
//  <Location>
//  ----------
   5,37,230,155

```



Si planea incluir una sección de vídeo en la máscara, puede usar el mismo tamaño y la misma ubicación para que el arte del álbum conserve espacio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




