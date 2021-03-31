---
description: FileCostaction inicia las acciones de instalación estándar de forma dinámica.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Acción FileCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083505"
---
# <a name="filecost-action"></a>Acción FileCost

FileCostaction inicia el [*costo*](c-gly.md)dinámico de las acciones de instalación estándar.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Cualquier acción estándar o [personalizada](custom-actions.md) que afecte a los costos se debe secuenciar antes de la acción [CostInitialize](costinitialize-action.md) . Llame a la acción FileCost inmediatamente después de la acción CostInitialize. Después, llame a la acción [CostFinalize](costfinalize-action.md) que sigue a la acción CostInitialize para que todos los cálculos de costos finales estén disponibles para el instalador a través de la tabla de [componentes](component-table.md) .

La acción [CostInitialize](costinitialize-action.md) se debe ejecutar antes de la acción FileCost. A continuación, el instalador determina el costo de espacio en disco de todos los archivos de la tabla de [archivos](file-table.md) , en función de cada componente (consulte [tabla de componentes](component-table.md)), que realiza la agrupación en clústeres de [*volúmenes*](v-gly.md) y la presencia de archivos existentes que es posible que deban sobrescribirse en la cuenta. También se consideran todas las acciones que consumen o liberan espacio en disco. Si se encuentra un archivo existente, se realiza una comprobación de la versión del archivo para determinar si realmente es necesario instalar el nuevo archivo o no. Si el archivo existente tiene un número de versión igual o mayor, el archivo existente no se sobrescribe y no se genera ningún costo de espacio en disco. En todos los casos, el instalador utiliza los resultados de la comprobación del número de versión para establecer el estado de instalación de cada archivo.

La acción FileCost inicializa el cálculo de costos con el instalador. No se produce un [*costo*](c-gly.md) dinámico real hasta que se ejecuta la acción [CostFinalize](costfinalize-action.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Costo de archivos](file-costing.md)
</dt> </dl>

 

 



