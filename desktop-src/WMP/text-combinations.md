---
title: Combinaciones de texto
description: Combinaciones de texto
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Aspectos móviles de Windows Media Player, marquesinas
- máscaras, marquesinas
- referencia de las máscaras, marquesinas
- marquesinas en máscaras, combinaciones de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532224"
---
# <a name="text-combinations"></a>Combinaciones de texto

Este valor es una lista de combinaciones de cuadro de presentación de texto, separadas por comas. Los cuadros de visualización de texto pueden combinarse mediante un carácter más para crear un nuevo valor de presentación de marquesina y cualquier tipo de texto definido en la sección tipo de texto se puede usar en el marco.

Al determinar lo que se va a mostrar, Windows Media Player Mobile evalúa cada elemento de la lista para ver si todos los elementos están disponibles. Si no es así, se evalúa el elemento siguiente, y así sucesivamente, hasta que se hayan encontrado todos los elementos disponibles. Por ejemplo, si desea mostrar el autor y el título, pero no está seguro de si ambos están disponibles, utilice el siguiente valor:


```C++
Title+Author, Title, Author

```



En el ejemplo anterior, se mostrará el título y el autor si se han definido el título y el autor para el elemento multimedia. Si no se definen ambos, el título se evalúa y se muestra si se define. Si no se define el título, se muestra el autor si está definido. Si no se define ninguno, no se muestra nada.

Al usar el signo más para la concatenación, asegúrese de que no haya espacios a ambos lados del signo más.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Marquesina**](marquee.md)
</dt> <dt>

[**Tipo de texto**](text-type.md)
</dt> </dl>

 

 




