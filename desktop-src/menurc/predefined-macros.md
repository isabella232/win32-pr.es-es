---
title: Macros predefinidas
description: RC no admite las macros predefinidas de ANSI C ( \_ \_ Date \_ \_ , \_ \_ file \_ \_ , \_ \_ line \_ \_ , \_ \_ stdc \_ \_ , \_ \_ Time \_ \_ , \_ \_ timestamp \_ \_ ). Por lo tanto, no puede incluir estas macros en los archivos de encabezado que incluirá en el script de recursos.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 351674bc86ab56753bb49dba9e65edd97a7b1a04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148794"
---
# <a name="predefined-macros"></a>Macros predefinidas

RC no admite las macros predefinidas de ANSI C (**\_ \_ Date \_ \_**, **\_ \_ file \_ \_**, **\_ \_ line \_ \_**, **\_ \_ stdc \_ \_**, **\_ \_ Time \_ , TIMESTAMP \_** **\_ \_ ). \_ \_** Por lo tanto, no puede incluir estas macros en los archivos de encabezado que incluirá en el script de recursos.

RC define RC \_ invocado, lo que permite compilar condicionalmente partes de los archivos de encabezado, dependiendo de si el compilador es el compilador de C o el compilador de RC. Esto es importante porque el compilador RC admite solo un subconjunto de las instrucciones compatibles con un compilador de C.

Para compilar condicionalmente el código con el compilador RC, el código envolvente que RC no puede compilar con \# ifndef RC \_ Invoke y **\# endif**.

El siguiente ejemplo se toma de los ejemplos del SDK de. Muestra cómo crear un archivo de encabezado que se puede compilar de forma condicional.

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




