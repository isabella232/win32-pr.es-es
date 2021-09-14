---
title: " define"
description: La directiva \ define asigna el valor especificado al nombre especificado. Todas las apariciones posteriores del nombre se reemplazan por el valor .
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360076"
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

 

 




