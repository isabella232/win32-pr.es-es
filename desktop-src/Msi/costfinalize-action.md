---
description: La acción CostFinalize finaliza el proceso de costo de instalación interno iniciado por la acción CostInitialize.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: CostFinalize Action
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158756"
---
# <a name="costfinalize-action"></a>CostFinalize Action

La acción CostFinalize finaliza el proceso de [*costo*](c-gly.md) de instalación interno iniciado por la [acción CostInitialize.](costinitialize-action.md)

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Cualquier acción estándar [o personalizada que](custom-actions.md) afecte al costo debe secuenciarse antes de la acción [CostInitialize.](costinitialize-action.md) Llame a [la acción FileCost](filecost-action.md) inmediatamente después de la acción CostInitialize y, a continuación, llame a la acción CostFinalize para que todos los cálculos de costos finales estén disponibles para el instalador a través de la tabla [Component.](component-table.md)

La acción CostFinalize debe ejecutarse antes de iniciar cualquier secuencia [](feature-table.md) de interfaz de usuario que permita al usuario ver o modificar directorios o selecciones de tabla de características.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Observaciones

La acción CostFinalize consulta la [tabla Condición](condition-table.md) para determinar qué características están programadas para instalarse. El costo se realiza para cada componente de la [tabla](component-table.md) Component.

La acción CostFinalize también comprueba que todos los directorios de destino se pueden escribir antes de permitir que la instalación continúe.

> [!Note]  
> Durante una [instalación administrativa,](administrative-installation.md)CostFinalize establece todas las características para la instalación, excepto las características que tienen 0 en la columna Nivel de la [tabla Característica](feature-table.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Costo de archivos](file-costing.md)
</dt> </dl>

 

 



