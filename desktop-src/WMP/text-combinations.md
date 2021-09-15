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
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569769"
---
# <a name="text-combinations"></a>Combinaciones de texto

Este valor es una lista de combinaciones de cuadros de presentación de texto, separados por comas. Los cuadros de presentación de texto se pueden unir mediante un carácter más para crear un nuevo valor de presentación de marquesina y cualquier tipo de texto definido en la sección Tipo de texto se puede usar en el marco.

Al determinar qué mostrar, Reproductor de Windows Media Mobile evalúa cada elemento de la lista para ver si todas las partes están disponibles. Si no es así, se evalúa el siguiente elemento, y así sucesivamente, hasta que se hayan encontrado todos los elementos disponibles. Por ejemplo, si desea mostrar Autor y Título, pero no está seguro de si ambos están disponibles, use el siguiente valor:


```C++
Title+Author, Title, Author

```



En el ejemplo anterior, se mostrará Title+Author si el título y el autor se han definido para el elemento multimedia. Si no se definen ambos, el título se evalúa y se muestra si se define. Si el título no está definido, se muestra el autor si se define. Si no se define ninguno, no se muestra nada.

Al usar el signo más para la concatenación, asegúrese de que no tiene espacios en ninguno de los lados del signo más.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Marquesina**](marquee.md)
</dt> <dt>

[**Tipo de texto**](text-type.md)
</dt> </dl>

 

 




