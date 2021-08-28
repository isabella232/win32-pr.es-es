---
description: La acción CostInitialize inicia el proceso de costo de instalación.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Acción CostInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959e9e250292a44050c1f4b9feb3fb29f7530fe2a1f53aa77a62bf3680ea9eeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948372"
---
# <a name="costinitialize-action"></a>Acción CostInitialize

La acción CostInitialize inicia el proceso de costo [*de instalación.*](c-gly.md)

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Las acciones estándar [o personalizadas](custom-actions.md) que afecten a los costos deben secuenciarse antes de la acción CostInitialize. Llame a [la acción FileCost](filecost-action.md) inmediatamente después de la acción CostInitialize. A continuación, llame a la acción [CostFinalize](costfinalize-action.md) después de la acción CostInitialize para que todos los cálculos de costos finales estén disponibles para el instalador a través de [la tabla Componente.](component-table.md)

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Comentarios

La acción CostInitialize carga la tabla Component y [la tabla Feature](feature-table.md) en la memoria.

Para obtener más información sobre el proceso [*de cálculo*](c-gly.md) de costos en el instalador, vea [File Costing](file-costing.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Costo de archivos](file-costing.md)
</dt> </dl>

 

 



