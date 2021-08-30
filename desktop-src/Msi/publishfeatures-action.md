---
description: La acción PublishFeatures escribe el estado de cada característica en el registro del sistema.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Acción PublishFeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6451b3676c5927ef1659108cc3559865fff921bdf48961ce5827a10f405109f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129035"
---
# <a name="publishfeatures-action"></a>Acción PublishFeatures

La acción PublishFeatures escribe el estado de cada característica en el registro del sistema. El estado de la característica puede estar ausente, anunciado o instalado. La acción PublishFeatures también escribe la asignación de componentes de características en el registro del sistema para cada característica instalada.

La acción PublishFeatures consulta las tablas [FeatureComponents](featurecomponents-table.md), [Feature table](feature-table.md)y [Component](component-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción PublishFeatures debe ir antes [que PublishProduct.](publishproduct-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción        |
|-------|-----------------------------------|
| \[1\] | Identificador de la característica anunciada. |



 

## <a name="remarks"></a>Comentarios

La acción PublishFeatures publica la composición de todas las características seleccionadas para anunciarse o instalarse.

 

 



