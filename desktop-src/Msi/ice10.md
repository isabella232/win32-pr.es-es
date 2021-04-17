---
description: ICE10 valida que el estado de anuncio de las características secundarias coincida con el de su característica primaria.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac8f1304f4444a0f087d747328cdea4b3d714ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667772"
---
# <a name="ice10"></a>ICE10

ICE10 valida que el estado de anuncio de las características secundarias coincida con el de su característica primaria.

Es posible que una característica secundaria no permita el anuncio mientras su característica primaria permita el anuncio. Por lo tanto, la siguiente combinación de atributos primarios y secundarios no es válida.

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

Esta combinación no es válida porque desactivaría el elemento primario cada vez que se supone que se anunciara el elemento primario. Sin embargo, se permite el orden inverso. Un elemento secundario se puede marcar para favorecer el anuncio mientras el elemento primario está marcado para no permitir el anuncio.

La acción personalizada ICE10 determina el estado de las características primarias y secundarias de la columna Attributes de la tabla de [características](feature-table.md) . Tenga en cuenta que es válido establecer el estado de una característica en 0 y tener su conjunto primario o secundario establecido en favorecer o deshabilitar el anuncio.

## <a name="result"></a>Resultado

ICE10 publica un error si la columna Attributes de la tabla de [características](feature-table.md) contiene una incoherencia en el estado de anuncio.

## <a name="example"></a>Ejemplo

ICE10 envía el siguiente mensaje de error para el ejemplo que se muestra.

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

Tenga en cuenta que en este ejemplo Microsoft Excel y Microsoft Word son características secundarias de Microsoft Office.

Tabla de [características](feature-table.md) (parcial)



| Característica | Característica \_ principal | Atributos |
|---------|-----------------|------------|
| Office  | Null            | 4          |
| Excel   | Office          | 4          |
| Word    | Office          | 8          |



 

En el ejemplo, Word se establece en no permitir anuncio, lo que entra en conflicto con el estado de anuncio de su elemento primario, Office.

En algunos casos, ICE10 envía el siguiente error:

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

Esto hace referencia a una referencia de clave externa no válida. La solución consiste en tener el punto "secundario" a su característica primaria correcta o agregar una entrada para la característica primaria "primaria" a la tabla de [características](feature-table.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



