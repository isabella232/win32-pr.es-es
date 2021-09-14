---
description: La acción PublishFeatures escribe el estado de cada característica en el registro del sistema.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Acción PublishFeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069725"
---
# <a name="publishfeatures-action"></a>Acción PublishFeatures

La acción PublishFeatures escribe el estado de cada característica en el registro del sistema. El estado de la característica puede estar ausente, anunciarse o estar instalado. La acción PublishFeatures también escribe la asignación de características y componentes en el registro del sistema para cada característica instalada.

La acción PublishFeatures consulta las tablas [FeatureComponents](featurecomponents-table.md), [Feature table](feature-table.md)y [Component](component-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción PublishFeatures debe ir antes [de PublishProduct.](publishproduct-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción        |
|-------|-----------------------------------|
| \[1\] | Identificador de la característica anunciada. |



 

## <a name="remarks"></a>Observaciones

La acción PublishFeatures publica la composición de todas las características seleccionadas para anunciarse o instalarse.

 

 



