---
title: " undef"
description: La directiva \ undef quita la definición actual del nombre especificado. Todas las apariciones posteriores del nombre se procesan sin reemplazo.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571632"
---
# <a name="undef"></a>\#undef

La **\# directiva undef** quita la definición actual del nombre especificado. Todas las apariciones posteriores del nombre se procesan sin reemplazo.

``` syntax
#undef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Nombre*
</dt> <dd>

Nombre que se va a quitar. Este valor es cualquier combinación de letras, dígitos y signos de puntuación que sea válido para el preprocesador de C/C++.

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

 

 




