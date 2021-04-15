---
title: " ifndef"
description: La Directiva \ ifndef controla la compilación condicional del archivo de recursos comprobando el nombre especificado.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695324"
---
# <a name="ifndef"></a>\#ifndef

La directiva **\# ifndef** controla la compilación condicional del archivo de recursos comprobando el nombre especificado. Si el nombre no se ha definido o si su definición se ha quitado mediante la directiva **\# UNDEF** , **\# ifndef** indica al compilador que continúe procesando las instrucciones hasta la siguiente directiva **\# endif**, **\# else** o **\# Elif** y, a continuación, vaya a la instrucción después de la directiva **\# endif** . Si se define el nombre, **\# ifndef** indica al compilador que vaya a la siguiente directiva **\# endif**, **\# else** o **\# Elif** .

``` syntax
#ifndef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Name*
</dt> <dd>

Nombre que se va a comprobar mediante la Directiva.

</dd> </dl>

## <a name="example"></a>Ejemplo

En este ejemplo se compila la instrucción [**Bitmap**](bitmap-resource.md) solo si no se define Optimize:

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




