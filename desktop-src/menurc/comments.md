---
title: Comentarios (menús y otros recursos)
description: RC admite la sintaxis de estilo C para los comentarios de una sola línea y para los comentarios de bloque. Los comentarios de una sola línea comienzan con dos barras diagonales (//) y se ejecutan hasta el final de la línea. A continuación se muestra un ejemplo de una instrucción de recurso seguido de un Comentario de una sola línea.
ms.assetid: 045268fb-2d6e-446c-8b95-90e42baeb282
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fda05690df9b7e7fff6974d75d8275a2842b68
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800871"
---
# <a name="comments-menus-and-other-resources"></a>Comentarios (menús y otros recursos)

RC admite la sintaxis de estilo C para los comentarios de una sola línea y para los comentarios de bloque. Los comentarios de una sola línea comienzan con dos barras diagonales (//) y se ejecutan hasta el final de la línea. A continuación se muestra un ejemplo de una instrucción de recurso seguido de un Comentario de una sola línea.

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

Los comentarios de bloque comienzan con un delimitador de apertura (/ \* ) y se ejecutan en un delimitador de cierre ( \* /). Los comentarios no se anidan. El siguiente es un ejemplo de un Comentario de bloque al principio de un archivo. rc.

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




