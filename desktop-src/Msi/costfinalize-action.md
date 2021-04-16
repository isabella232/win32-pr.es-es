---
description: La acción CostFinalize finaliza el proceso de costo de instalación interna Iniciado por la acción CostInitialize.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Acción CostFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669681"
---
# <a name="costfinalize-action"></a>Acción CostFinalize

La acción CostFinalize finaliza el proceso de [*costo*](c-gly.md) de instalación interna Iniciado por la acción [CostInitialize](costinitialize-action.md) .

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Cualquier acción estándar o [personalizada](custom-actions.md) que afecte a los costos se debe secuenciar antes de la acción [CostInitialize](costinitialize-action.md) . Llame a la acción [FileCost](filecost-action.md) inmediatamente después de la acción CostInitialize y, a continuación, llame a la acción CostFinalize para que todos los cálculos de costos finales estén disponibles para el instalador a través de la tabla de [componentes](component-table.md) .

La acción CostFinalize se debe ejecutar antes de iniciar cualquier secuencia de interfaz de usuario que permita al usuario ver o modificar los directorios o las selecciones de las tablas de [características](feature-table.md) .

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

La acción CostFinalize consulta la tabla de [condiciones](condition-table.md) para determinar qué características están programadas para instalarse. El costo se realiza para cada componente de la tabla de [componentes](component-table.md) .

La acción CostFinalize también comprueba que se puedan escribir todos los directorios de destino antes de permitir que continúe la instalación.

> [!Note]  
> Durante una [instalación administrativa](administrative-installation.md), CostFinalize establece todas las características para la instalación, excepto las características que tienen 0 creado en la columna LEVEL de la [tabla de características](feature-table.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Costo de archivos](file-costing.md)
</dt> </dl>

 

 



