---
title: Cadenas de formato de tipo
description: Los caracteres de formato indican objetos de interés para el motor de NDR.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076086"
---
# <a name="type-format-strings"></a>Cadenas de formato de tipo

Los caracteres de formato indican objetos de interés para el motor de NDR. Hay un carácter de formato para cada tipo básico, para varios tipos complejos y para descripciones de punteros, empaquetado, alineación y otros objetos varios. En el caso de los tipos compuestos, se reconocen varias categorías de estructuras y matrices en función de sus propiedades de rendimiento. Una cadena de formato para cada categoría comienza con un token de FC que identifica la cadena de formato en particular. Los caracteres de formato de las categorías de estructuras y matrices pueden compartir las correcciones en el nombre del token de FC inicial que se muestra en la tabla siguiente.



| Carácter de formato | Descripción                                    |
|------------------|------------------------------------------------|
| C                | Indica la información de conformidad en el tipo. |
| V                | Indica la información de la varianza en el tipo.    |
| P                | Indica que los punteros son una parte del tipo.     |



 

Por ejemplo, FC \_ CSTRUCT y la \_ CArray de FC identifican la estructura compatible y los descriptores de matriz compatibles, respectivamente.

A continuación se muestran caracteres de formato con significados especiales.



| Carácter de formato | Descripción                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| FC \_ PP           | Indica el principio de la sección de Descripción del puntero de una estructura o una matriz. |



 

Las cadenas de formato de tipo NDR de RPC se describen con más detalle en los temas siguientes:

-   [Tipos simples](simple-types-tfs.md)
-   [Punteros](pointers-tfs.md)
-   [Matrices](arrays-tfs.md)
-   [Cadenas](strings-tfs.md)
-   [Descriptores de correlación](correlation-descriptors-tfs.md)
-   [Estructuras](structures-tfs.md)
-   [Diseño de puntero](pointer-layout-tfs.md)
-   [Uniones](unions-tfs.md)
-   [Transmitir \_ como y representar \_ como](transmit-as-and-represent-as-tfs.md)
-   [Serialización de usuario](user-marshal-tfs.md)

 

 




