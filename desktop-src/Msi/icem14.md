---
description: ICEM14 valida la columna value de la tabla ModuleSubstitution.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf8bb2b20087a7322dd80d4ca8873f84d42823694b00751e714aec7d0bde14a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821415"
---
# <a name="icem14"></a>ICEM14

ICEM14 valida la columna value de la [tabla ModuleSubstitution](modulesubstitution-table.md).

## <a name="result"></a>Resultado

ICEM14 publica los siguientes errores.



| Error                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cadena de reemplazo de la columna ModuleSubstitution.Value de la \[ fila \] 1. \[ 2 \] . \[ 3 \] no se encuentra en la tabla ModuleConfiguration.                                 | \[1 \] . \[ 2 \] . \[ 3 \] hace referencia a una clave principal *table.row.column* para una fila de la tabla ModuleSubstitution. La plantilla de formato del campo Valor de esta fila no corresponde a una fila de atributos configurables en [la tabla ModuleConfiguration](moduleconfiguration-table.md).                                                            |
| En la tabla ModuleSubstitution de la \[ fila \] 1. \[ 2 \] . \[ 3 \] , se indica un elemento configurable en la tabla '%s'. La tabla '%s' no debe contener elementos configurables. | Una de las tablas siguientes se muestra en la columna Tabla de la tabla [ModuleSubstitution: ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration,](moduleconfiguration-table.md) [ModuleExclusion](moduleexclusion-table.md)o [ModuleSignature.](modulesignature-table.md) Estas tablas no pueden contener campos configurables. |
| En la tabla ModuleSubstitution de la \[ fila \] 1. \[ 2 \] . \[ 3 \] , se especifica una cadena de reemplazo vacía.                                                               | La plantilla de formato del campo Valor de esta fila no corresponde a una fila de atributos configurables en [la tabla ModuleConfiguration](moduleconfiguration-table.md).                                                                                                                                                                    |



 

ICEM14 publica la advertencia siguiente.



| Advertencia                                                                  | Significado                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| Existe la tabla ModuleSubstitution, pero falta la tabla ModuleConfiguration | La tabla ModuleConfiguration no está presente. |



 

## <a name="table-used-during-execution"></a>Tabla usada durante la ejecución

[Tabla ModuleSubstitution](modulesubstitution-table.md)

[Tabla ModuleConfiguration](moduleconfiguration-table.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



