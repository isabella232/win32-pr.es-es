---
title: " define"
description: La directiva \ define asigna el valor especificado al nombre especificado. Todas las apariciones posteriores del nombre se reemplazan por el valor .
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8e8f99dc592eefb1fb79201883e8a32837633814b79d7819e84d283709a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826055"
---
# <a name="define"></a>\#Definir

La **\# directiva define** asigna el valor especificado al nombre especificado. Todas las apariciones posteriores del nombre se reemplazan por el valor .

``` syntax
#define name value
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*Nombre*
</dt> <dd>

Nombre que se va a definir. Este valor es cualquier combinación de letras, dígitos y signos de puntuación que sea válido para el preprocesador de C/C++.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Valor*
</dt> <dd>

Entero, cadena de caracteres o línea de texto.

</dd> </dl>

## <a name="example"></a>Ejemplo

En este ejemplo se asignan valores a los nombres NONZERO y USERCLASS:

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directivas de preprocesador](preprocessor-directives.md)
</dt> </dl>

 

 




