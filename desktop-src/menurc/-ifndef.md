---
title: " ifndef"
description: La directiva \ ifndef controla la compilación condicional del archivo de recursos comprobando el nombre especificado.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23728acabc0ca0179c544a66657a2d1b8343d5eae24556018e0e65025420bfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472991"
---
# <a name="ifndef"></a>\#ifndef

La **\# directiva ifndef** controla la compilación condicional del archivo de recursos comprobando el nombre especificado. Si no se ha definido el nombre o si su definición se ha quitado mediante la directiva **\# undef,** **\# ifndef** indica al compilador que continúe procesando instrucciones hasta la siguiente directiva **\# endif**, **\# else** o **\# elif** y, a continuación, omite la instrucción después de la **\# directiva endif.** Si se define el nombre, **\# ifndef** indica al compilador que vaya directamente a la siguiente **\# directiva endif**, **\# else** o **\# elif.**

``` syntax
#ifndef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Nombre*
</dt> <dd>

Nombre que va a comprobar la directiva.

</dd> </dl>

## <a name="example"></a>Ejemplo

En este ejemplo se compila la [**instrucción BITMAP**](bitmap-resource.md) solo si no se define Optimize:

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




