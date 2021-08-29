---
title: Comentarios (menús y otros recursos)
description: RC admite la sintaxis de estilo C para comentarios de una sola línea y comentarios de bloque. Los comentarios de una sola línea comienzan con dos barras diagonales (//) y se ejecutan hasta el final de la línea. A continuación se muestra un ejemplo de una instrucción de recurso seguida de un comentario de una sola línea.
ms.assetid: 045268fb-2d6e-446c-8b95-90e42baeb282
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c907543e5238d5cdfe71e4f97f2908abe3425ee54a5649707e9a0a8b45e32237
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847405"
---
# <a name="comments-menus-and-other-resources"></a>Comentarios (menús y otros recursos)

RC admite la sintaxis de estilo C para comentarios de una sola línea y comentarios de bloque. Los comentarios de una sola línea comienzan con dos barras diagonales (//) y se ejecutan hasta el final de la línea. A continuación se muestra un ejemplo de una instrucción de recurso seguida de un comentario de una sola línea.

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

Los comentarios de bloque comienzan con un delimitador de apertura (/ ) y \* se ejecutan hasta un delimitador de cierre ( \* /). Los comentarios no se anidan. A continuación se muestra un ejemplo de un comentario de bloque al principio de un archivo .rc.

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




