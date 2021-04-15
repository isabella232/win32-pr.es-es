---
title: Carátula de álbum
description: Carátula de álbum
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Aspectos móviles de Windows Media Player, carátulas de álbum
- máscaras, carátulas de álbum
- referencia para máscaras, carátulas de álbum
- archivos de imagen para máscaras, carátulas de álbum
- carátula de álbum en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695269"
---
# <a name="album-art"></a>Carátula de álbum

Cuando se crea una máscara para Windows Media Player 10 Mobile o posterior, es posible que desee mostrar carátulas de álbum relacionada con el elemento multimedia que se está reproduciendo. Al diseñar la máscara, querrá reservar espacio en la imagen de fondo para que contenga la carátula del álbum.

La sección carátula de álbum del archivo de definición de máscara debe comenzar con la línea siguiente:


```C++
[ Album Art ]

```



A continuación, debe agregar información que especifique la ubicación y el tamaño de la carátula del álbum en la máscara. Debe escribir cuatro enteros positivos, separados por comas que definan la izquierda, la parte superior, el ancho y el alto de la carátula del álbum, en píxeles, con respecto a la imagen de fondo. En el ejemplo siguiente se muestra cómo especificar dimensiones:


```C++
//  <Location>
//  ----------
   5,37,230,155

```



Si planea incluir una sección de vídeo en la máscara, puede usar el mismo tamaño y la misma ubicación que la carátula de álbum para ahorrar espacio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




