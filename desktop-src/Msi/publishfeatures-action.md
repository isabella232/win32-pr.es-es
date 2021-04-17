---
description: La acción PublishFeatures escribe el estado de cada característica en el registro del sistema.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Acción PublishFeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677772"
---
# <a name="publishfeatures-action"></a>Acción PublishFeatures

La acción PublishFeatures escribe el estado de cada característica en el registro del sistema. El estado de la característica puede estar ausente, anunciado o instalado. La acción PublishFeatures también escribe la asignación del componente de característica en el registro del sistema para cada característica instalada.

La acción PublishFeatures consulta la tabla de [FeatureComponents](featurecomponents-table.md), la [tabla de características](feature-table.md)y la [tabla de componentes](component-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción PublishFeatures debe ser anterior a [PublishProduct](publishproduct-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción        |
|-------|-----------------------------------|
| \[1\] | Identificador de la característica anunciada. |



 

## <a name="remarks"></a>Observaciones

La acción PublishFeatures publica la composición de todas las características que se seleccionan para ser anunciadas o instaladas.

 

 



