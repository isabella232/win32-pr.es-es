---
title: " undef"
description: La Directiva \ UNDEF quita la definición actual del nombre especificado. Todas las repeticiones posteriores del nombre se procesan sin reemplazo.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714177"
---
# <a name="undef"></a>\#undef

La directiva **\# UNDEF** quita la definición actual del nombre especificado. Todas las repeticiones posteriores del nombre se procesan sin reemplazo.

``` syntax
#undef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Name*
</dt> <dd>

Nombre que se va a quitar. Este valor es cualquier combinación de letras, dígitos y puntuación que sea válida para el preprocesador de C/C++.

</dd> </dl>

## <a name="example"></a>Ejemplo

En este ejemplo se quitan las definiciones de los nombres distintos de cero y USERCLASS:

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




