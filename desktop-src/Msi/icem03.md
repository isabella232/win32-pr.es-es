---
description: ICEM03 comprueba que todas las acciones del módulo son acciones base o derivan de una acción base válida.
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074494"
---
# <a name="icem03"></a>ICEM03

ICEM03 comprueba que todas las acciones del módulo son acciones base o derivan de una acción base válida.

Los ICE del módulo de mezcla se almacenan en un archivo .uu. del módulo de mezcla denominado Mergemod.uu y no en el archivo .uu. que contiene los ICE usados para la validación del paquete.

## <a name="result"></a>Resultado

ICEM03 publica los mensajes de error de un módulo que contiene acciones en una tabla de secuencia que no es una acción base o que se deriva de una acción base válida.

## <a name="example"></a>Ejemplo

ICEM03 publica los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[ModuleInstallExecuteSequence Table](moduleinstallexecutesequence-table.md)



| Acción  | Secuencia | BaseAction | Después | Condición |
|---------|----------|------------|-------|-----------|
| Action1 |          | Action2    | 0     |           |
| Action2 |          | Action1    | 0     |           |



 

ICEM03 publica errores para estas dos acciones porque se hacen referencia entre sí como acciones base en la tabla ModuleInstallExecuteSequence. Todas las acciones de las tablas [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence,](moduleadvtexecutesequence-table.md) [ModuleInstallUISequence](moduleinstalluisequence-table.md)y [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) deben ser acciones base o derivar su posición de la combinación de otra acción y una marca antes y después.

Para corregir este error, determine las acciones base para las dos acciones. Agregue un registro para las acciones base con un número de secuencia predeterminado. En Acción1 y Acción2, escriba los nombres de acción base en la columna BaseAction y 0 o 1 en la columna Después.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



