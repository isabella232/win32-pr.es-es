---
description: ICE72 comprueba que las acciones personalizadas no integradas no se usan en la tabla AdvtExecuteSequence.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f931e705dbca734348f62ba4b1ca106b43bb80a52c50f0e94ecab7139c624da2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946582"
---
# <a name="ice72"></a>ICE72

ICE72 comprueba que las acciones personalizadas no integradas no se usan en la [tabla AdvtExecuteSequence](advtexecutesequence-table.md). En concreto, solo se permiten acciones personalizadas de tipo 19, tipo 35 y tipo 51 en la tabla AdvtExecuteSequence. Si se usan otras acciones personalizadas, es posible que el anuncio no se comporte según lo previsto.

## <a name="result"></a>Resultado

ICE72 devuelve un error si la tabla AdvExecuteSequence usa acciones personalizadas que no son del tipo 35, 51 y 19.

## <a name="example"></a>Ejemplo

ICE72 notifica el siguiente error para el ejemplo mostrado:

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

Para corregir el error, quite "CA1" de la tabla AdvtExecuteSequence.

[Tabla AdvtExecuteSequence](advtexecutesequence-table.md) (parcial)



| Acción |
|--------|
| CA1    |
| CA35   |



 

[Tabla CustomAction](customaction-table.md) (parcial)



| Acción | Tipo |
|--------|------|
| CA1    | 1    |
| CA35   | 35   |



 

## <a name="tables-used-during-execution"></a>Tablas usadas durante la ejecución

[Tabla AdvtExecuteSequence](advtexecutesequence-table.md)

[CustomAction (tabla)](customaction-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipo de acción personalizada 19](custom-action-type-19.md)
</dt> <dt>

[Tipo de acción personalizada 35](custom-action-type-35.md)
</dt> <dt>

[Tipo de acción personalizada 51](custom-action-type-51.md)
</dt> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



