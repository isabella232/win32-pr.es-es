---
description: Los valores del Registro deben establecerse para que los verbos controle situaciones en las que un usuario puede seleccionar un solo elemento, varios elementos o una selección de un elemento. Un verbo requiere valores del Registro independientes para cada una de estas tres situaciones que admite el verbo.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Cómo emplear el modelo de selección de verbos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89028c7d2ce153582f45c140a0f32ca9f1714601c3e68bf36693b5955c904f71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049858"
---
# <a name="how-to-employ-the-verb-selection-model"></a>Cómo emplear el modelo de selección de verbos

Los valores del Registro deben establecerse para que los verbos controle situaciones en las que un usuario puede seleccionar un solo elemento, varios elementos o una selección de un elemento. Un verbo requiere valores del Registro independientes para cada una de estas tres situaciones que admite el verbo.

## <a name="instructions"></a>Instructions


Especifique el valor MultiSelectModel para todos los verbos. Si no se especifica el valor MultiSelectModel, se deduce del tipo de implementación de verbo que ha elegido. En el caso de los métodos basados en COM (como DropTarget y **ExecuteCommand),** se supone que el reproductor y para los demás métodos es **Document.**

Los valores posibles para el modelo de selección de verbos son los siguientes:

1.  Especifique **Single** para los verbos que solo admiten una selección única.
2.  Especifique **Player** para los verbos que admiten cualquier número de elementos.
3.  Especifique **Document** para los verbos que crean una ventana de nivel superior para cada elemento. Al hacerlo, se limita el número de elementos que se activan y se evita que se quedándose sin recursos del sistema si el usuario abre demasiadas ventanas.

## <a name="remarks"></a>Comentarios

Cuando el número de elementos seleccionados no coincide con el modelo de selección de verbos o es mayor que los límites predeterminados descritos en la tabla siguiente, el verbo no aparece.



| Tipo de implementación de verbo | Documento | Reproductor    |
|-----------------------------|----------|-----------|
| Heredado                      | 15 elementos | 100 elementos |
| COM                         | 15 elementos | Sin límite  |



 

A continuación se incluyen entradas del Registro de ejemplo que usan el valor MultiSelectModel.

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



