---
description: Los valores del registro se deben establecer para que los verbos controlen las situaciones en las que un usuario puede seleccionar un solo elemento, varios elementos o una selección de un elemento. Un verbo requiere valores de registro independientes para cada una de estas tres situaciones que admite el verbo.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Cómo emplear el modelo de selección de verbos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985447"
---
# <a name="how-to-employ-the-verb-selection-model"></a>Cómo emplear el modelo de selección de verbos

Los valores del registro se deben establecer para que los verbos controlen las situaciones en las que un usuario puede seleccionar un solo elemento, varios elementos o una selección de un elemento. Un verbo requiere valores de registro independientes para cada una de estas tres situaciones que admite el verbo.

## <a name="instructions"></a>Instrucciones


Especifique el valor de MultiSelectModel para todos los verbos. Si no se especifica el valor MultiSelectModel, se deduce del tipo de implementación de verbo que ha elegido. En el caso de los métodos basados en COM (como DropTarget y ExecuteCommand), se supone que el **jugador** y para el resto **de métodos se** supone.

Los valores posibles para el modelo de selección de verbos son los siguientes:

1.  Especifique **Single** para los verbos que solo admiten una sola selección.
2.  Especifique **Player** para los verbos que admiten cualquier número de elementos.
3.  Especifique el **documento** para los verbos que crean una ventana de nivel superior para cada elemento. Esto limita el número de elementos que están activados y ayuda a evitar quedarse sin recursos del sistema si el usuario abre demasiadas ventanas.

## <a name="remarks"></a>Observaciones

Cuando el número de elementos seleccionados no coincide con el modelo de selección de verbos o es mayor que los límites predeterminados que se describen en la tabla siguiente, el verbo no aparece.



| Tipo de implementación de verbo | Documento | Reproductor    |
|-----------------------------|----------|-----------|
| Heredado                      | 15 elementos | 100 elementos |
| COM                         | 15 elementos | Sin límite  |



 

A continuación se muestran las entradas del registro de ejemplo que usan el valor MultiSelectModel.

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

 

 



