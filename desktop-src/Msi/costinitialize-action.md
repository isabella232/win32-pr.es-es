---
description: La acción CostInitialize inicia el proceso de costo de la instalación.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Acción CostInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667675"
---
# <a name="costinitialize-action"></a>Acción CostInitialize

La acción CostInitialize inicia el proceso de [*costo*](c-gly.md) de la instalación.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Cualquier acción estándar o [personalizada](custom-actions.md) que afecte a los costos se debe secuenciar antes de la acción CostInitialize. Llame a la acción [FileCost](filecost-action.md) inmediatamente después de la acción CostInitialize. Después, llame a la acción [CostFinalize](costfinalize-action.md) que sigue a la acción de acción CostInitialize para que todos los cálculos de costos finales estén disponibles para el instalador a través de la tabla de [componentes](component-table.md) .

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

La acción CostInitialize carga la tabla de componentes y la tabla de [características](feature-table.md) en la memoria.

Para obtener más información sobre el proceso de [*costo*](c-gly.md) en el instalador, consulte [costo de archivos](file-costing.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Costo de archivos](file-costing.md)
</dt> </dl>

 

 



