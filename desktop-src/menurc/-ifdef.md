---
title: " ifdef"
description: La Directiva \ ifdef controla la compilación condicional del archivo de recursos comprobando el nombre especificado.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418736"
---
# <a name="ifdef"></a>\#ifdef

La directiva **\# ifdef** controla la compilación condicional del archivo de recursos comprobando el nombre especificado. Si el nombre se ha definido mediante una directiva de **\# definición** o mediante la opción de línea de comandos **/d** con el compilador de recursos, **\# ifdef** indica al compilador que continúe con la instrucción inmediatamente después de la directiva **\# ifdef** . Si no se ha definido el nombre, **\# ifdef** indica al compilador que omita todas las instrucciones hasta la siguiente directiva **\# endif** .

``` syntax
#ifdef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Name*
</dt> <dd>

Nombre que se va a comprobar mediante la Directiva.

</dd> </dl>

## <a name="example"></a>Ejemplo

En este ejemplo se compila la instrucción [**Bitmap**](bitmap-resource.md) solo si se define DEBUG:

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




