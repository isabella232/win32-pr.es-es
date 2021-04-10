---
description: ICEM14 valida la columna de valor de la tabla ModuleSubstitution.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155293"
---
# <a name="icem14"></a>ICEM14

ICEM14 valida la columna de valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

## <a name="result"></a>Resultado

ICEM14 expone los siguientes errores.



| Error                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La cadena de reemplazo en la columna ModuleSubstitution. Value de la fila \[ 1 \] . \[ 2 \] . \[ 3 \] no se encuentra en la tabla ModuleConfiguration.                                 | \[1 \] . \[ 2 \] . \[ 3 \] hace referencia a una clave principal *TABLE. Row. Column* para una fila de la tabla ModuleSubstitution. La plantilla de formato en el campo de valor de esta fila no se corresponde con una fila de atributos configurables de la [tabla ModuleConfiguration](moduleconfiguration-table.md).                                                            |
| En la tabla ModuleSubstitution de la fila \[ 1 \] . \[ 2 \] . \[ 3 \] , se indica un elemento configurable en la tabla '% s '. La tabla '% s ' no debe contener elementos configurables. | Una de las tablas siguientes aparece en la columna tabla de la tabla ModuleSubstitution: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md)o [ModuleSignature](modulesignature-table.md). Estas tablas no pueden contener campos configurables. |
| En la tabla ModuleSubstitution de la fila \[ 1 \] . \[ 2 \] . \[ 3 \] , se especifica una cadena de reemplazo vacía.                                                               | La plantilla de formato en el campo de valor de esta fila no se corresponde con una fila de atributos configurables de la [tabla ModuleConfiguration](moduleconfiguration-table.md).                                                                                                                                                                    |



 

ICEM14 envía la siguiente advertencia.



| Advertencia                                                                  | Significado                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| La tabla ModuleSubstitution existe pero falta la tabla ModuleConfiguration | Falta la tabla ModuleConfiguration. |



 

## <a name="table-used-during-execution"></a>Tabla utilizada durante la ejecución

[Tabla ModuleSubstitution](modulesubstitution-table.md)

[Tabla ModuleConfiguration](moduleconfiguration-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de módulo de combinación ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



