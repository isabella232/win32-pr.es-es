---
title: Combinaciones de texto
description: Combinaciones de texto
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Reproductor de Windows Media Máscaras móviles, marques
- máscaras, marques
- referencia de máscaras, marques
- marques en máscaras, combinaciones de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0d937d0ae2f90fe37ea8f4af1208443bbb127d622a83ecb5f556ddff596824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933424"
---
# <a name="text-combinations"></a>Combinaciones de texto

Este valor es una lista de combinaciones de cuadros de presentación de texto, separados por comas. Los cuadros de presentación de texto se pueden unir mediante un carácter más para crear un nuevo valor de presentación de marquesina y cualquier tipo de texto definido en la sección Tipo de texto se puede usar en el marco.

Al determinar qué mostrar, Reproductor de Windows Media Mobile evalúa cada elemento de la lista para ver si todas las partes están disponibles. Si no es así, se evalúa el siguiente elemento, y así sucesivamente, hasta que se hayan encontrado todos los elementos disponibles. Por ejemplo, si desea mostrar Autor y Título, pero no está seguro de si ambos están disponibles, use el siguiente valor:


```C++
Title+Author, Title, Author

```



En el ejemplo anterior, se mostrará Title+Author si el título y el autor se han definido para el elemento multimedia. Si ambos no están definidos, el título se evalúa y se muestra si se define. Si el título no está definido, se muestra el autor si se define. Si no se define ninguno, no se muestra nada.

Al usar el signo más para la concatenación, asegúrese de que no tiene espacios en ninguno de los lados del signo más.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Marquesina**](marquee.md)
</dt> <dt>

[**Tipo de texto**](text-type.md)
</dt> </dl>

 

 




