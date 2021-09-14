---
description: FileCostaction inicia el costo dinámico de las acciones de instalación estándar.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Acción FileCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074783"
---
# <a name="filecost-action"></a>Acción FileCost

FileCostaction inicia el costo dinámico [*de*](c-gly.md)las acciones de instalación estándar.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Cualquier acción estándar [o personalizada que afecte](custom-actions.md) al costo debe secuenciarse antes de la acción [CostInitialize.](costinitialize-action.md) Llame a la acción FileCost inmediatamente después de la acción CostInitialize. A continuación, llame a la acción [CostFinalize](costfinalize-action.md) después de la acción CostInitialize para que todos los cálculos de costos finales estén disponibles para el instalador a través de [la tabla Component.](component-table.md)

La [acción CostInitialize](costinitialize-action.md) debe ejecutarse antes de la acción FileCost. A continuación, el instalador determina el costo [](file-table.md) de espacio en disco de cada archivo de [](v-gly.md) la tabla Archivo, por componente (vea Tabla de [componentes),](component-table.md)teniendo en cuenta tanto la agrupación en clústeres de volúmenes como la presencia de archivos existentes que es posible que deba sobrescribirse. También se tienen en cuenta todas las acciones que consumen o liberan espacio en disco. Si se encuentra un archivo existente, se realiza una comprobación de la versión del archivo para determinar si el nuevo archivo realmente debe instalarse o no. Si el archivo existente tiene un número de versión igual o mayor, el archivo existente no se sobrescribe y no se incurre en ningún costo de espacio en disco. En todos los casos, el instalador usa los resultados de la comprobación del número de versión para establecer el estado de instalación de cada archivo.

La acción FileCost inicializa el cálculo de costos con el instalador. El costo [*dinámico real*](c-gly.md) no se produce hasta que se ejecuta la acción [CostFinalize.](costfinalize-action.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Costo de archivos](file-costing.md)
</dt> </dl>

 

 



