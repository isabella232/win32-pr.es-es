---
description: Las funciones del instalador se pueden usar para ejecutar acciones o secuencias de acciones específicas.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Acciones en ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9e167144a620589bc6f0641d7344a2d31254cd003412e746a41759c1143506
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039655"
---
# <a name="running-actions"></a>Acciones en ejecución

Las funciones del instalador se pueden usar para ejecutar acciones o secuencias de acciones específicas. Estas acciones pueden ser acciones [estándar](standard-actions.md) [o personalizadas.](custom-actions.md) En el procedimiento siguiente se describe cómo ejecutar acciones:

**Para ejecutar una secuencia de acciones**

1.  Ejecute una secuencia de acciones definidas en una tabla mediante una llamada a la [**función MsiSequence.**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)

    El instalador consulta la tabla indicada y ejecuta cada acción si su expresión condicional se evalúa como TRUE.

2.  Compruebe las expresiones condicionales llamando a [**la función MsiEvaluateCondition.**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)
3.  Ejecute la acción llamando a la [**función MsiDoAction.**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) La acción puede ser una acción estándar, una acción personalizada o un cuadro de diálogo de interfaz de usuario.
4.  Si se produjo un error durante la ejecución de esta acción, llame a la [**función MsiProcessMessage.**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) El instalador procesará el error.

 

 



