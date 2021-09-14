---
title: Álbum de arte
description: Álbum de arte
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Reproductor de Windows Media Máscaras móviles, arte de álbum
- máscaras, arte de álbum
- referencia de máscaras, arte de álbum
- archivos de arte para máscaras, arte de álbum
- arte de álbum en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890185"
---
# <a name="album-art"></a>Álbum de arte

Al crear una máscara para Reproductor de Windows Media 10 Mobile o versiones posteriores, es posible que quiera mostrar el material de álbum relacionado con el elemento multimedia que se está reproduciendo actualmente. Al diseñar la máscara, querrá reservar espacio en la imagen de fondo para que contenga el arte del álbum.

La sección Album Art del archivo de definición de máscara debe comenzar con la siguiente línea:


```C++
[ Album Art ]

```



A continuación, debe agregar información que especifique la ubicación y el tamaño de la imagen del álbum en la máscara. Debe escribir cuatro enteros positivos, separados por comas que definen la izquierda, la parte superior, el ancho y el alto de la imagen del álbum, en píxeles, con respecto a la imagen de fondo. En el ejemplo siguiente se muestra cómo especificar dimensiones:


```C++
//  <Location>
//  ----------
   5,37,230,155

```



Si planea incluir una sección de vídeo en la máscara, puede usar el mismo tamaño y ubicación para el arte del álbum a la hora de ahorrar espacio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




