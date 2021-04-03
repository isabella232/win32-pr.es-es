---
title: " define"
description: La Directiva \ define asigna el valor dado al nombre especificado. Todas las repeticiones posteriores del nombre se reemplazan por el valor.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777485"
---
# <a name="define"></a>\#define

La directiva **\# define** asigna el valor dado al nombre especificado. Todas las repeticiones posteriores del nombre se reemplazan por el valor.

``` syntax
#define name value
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Name*
</dt> <dd>

Nombre que se va a definir. Este valor es cualquier combinación de letras, dígitos y puntuación que sea válida para el preprocesador de C/C++.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valor*
</dt> <dd>

Entero, cadena de caracteres o línea de texto.

</dd> </dl>

## <a name="example"></a>Ejemplo

Este ejemplo asigna valores a los nombres NonZero y USERCLASS:

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




