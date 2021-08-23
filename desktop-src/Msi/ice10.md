---
description: ICE10 valida que el estado de anuncio de las características secundarias coincide con el de su característica primaria.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80071bdb7f219904c03d7c6b5b947a1bd818af2c3ebc270b0bfb17f2cf185280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581215"
---
# <a name="ice10"></a>ICE10

ICE10 valida que el estado de anuncio de las características secundarias coincide con el de su característica primaria.

Es posible que una característica secundaria no permita anuncios mientras que su característica primaria permite anuncios. Por lo tanto, la siguiente combinación de atributos primarios y secundarios no es válida.

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

Esta combinación no es válida porque desactivaría el elemento primario cada vez que se supone que se debe anunciar el elemento primario. Sin embargo, se permite lo contrario. Un elemento secundario se puede marcar para favorecer el anuncio mientras el elemento primario está marcado para no permitir anuncios.

La acción personalizada ICE10 determina el estado de las características primarias y secundarias de la columna Atributos de la [tabla Característica.](feature-table.md) Tenga en cuenta que es válido establecer el estado de una característica en 0 y establecer su elemento primario o secundario para favorecer o no el anuncio.

## <a name="result"></a>Resultado

ICE10 publica un error si la columna Atributos de la [tabla Característica](feature-table.md) contiene un error de coincidencia en el estado de anuncio.

## <a name="example"></a>Ejemplo

ICE10 publica el siguiente mensaje de error para el ejemplo mostrado.

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

Tenga en cuenta en este ejemplo que Microsoft Excel y Microsoft Word son características secundarias de Microsoft Office.

[Tabla](feature-table.md) de características (parcial)



| Característica | Elemento \_ primario de la característica | Atributos |
|---------|-----------------|------------|
| Office  | Null            | 4          |
| Excel   | Office          | 4          |
| Word    | Office          | 8          |



 

En el ejemplo, Word se establece en no permitir anuncios, lo que entra en conflicto con el estado de anuncio permitido de su elemento primario, Office.

En algunos casos, ICE10 publica el siguiente error:

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

Esto hace referencia a una referencia de clave externa no válida. La corrección es hacer que "Child" apunte a su característica primaria correcta o agregar una entrada para la característica primaria "Parent" a la [tabla Feature.](feature-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



