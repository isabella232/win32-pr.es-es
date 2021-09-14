---
title: " ifdef"
description: La directiva \ ifdef controla la compilación condicional del archivo de recursos comprobando el nombre especificado.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252453"
---
# <a name="ifdef"></a>\#ifdef

La **\# directiva ifdef** controla la compilación condicional del archivo de recursos comprobando el nombre especificado. Si el nombre se ha definido mediante una directiva **\# define** o mediante la opción de línea de comandos **/d** con el compilador de recursos, **\# ifdef** ordena al compilador que continúe con la instrucción inmediatamente después de la **\# directiva ifdef.** Si no se ha definido el nombre, **\# ifdef** dirige al compilador a omitir todas las instrucciones hasta la siguiente **\# directiva endif.**

``` syntax
#ifdef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Nombre*
</dt> <dd>

Nombre que va a comprobar la directiva.

</dd> </dl>

## <a name="example"></a>Ejemplo

En este ejemplo se compila la [**instrucción BITMAP**](bitmap-resource.md) solo si se define Debug:

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




