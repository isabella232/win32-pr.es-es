---
description: Las funciones de instalador se pueden usar para ejecutar acciones específicas o secuencias de acción.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Ejecutar acciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666796"
---
# <a name="running-actions"></a>Ejecutar acciones

Las funciones de instalador se pueden usar para ejecutar acciones específicas o secuencias de acción. Estas acciones pueden ser acciones [estándar](standard-actions.md) o [personalizadas](custom-actions.md) . En el procedimiento siguiente se describe cómo ejecutar acciones:

**Para ejecutar una secuencia de acciones**

1.  Ejecute una secuencia de acciones definida en una tabla mediante una llamada a la función [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) .

    El instalador consulta la tabla indicada y ejecuta cada acción si su expresión condicional se evalúa como TRUE.

2.  Compruebe las expresiones condicionales mediante una llamada a la función [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .
3.  Ejecute la acción mediante una llamada a la función [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) . La acción puede ser una acción estándar, una acción personalizada o un cuadro de diálogo de la interfaz de usuario.
4.  Si se produjo un error durante la ejecución de esta acción, llame a la función [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) . El instalador procesará el error.

 

 



