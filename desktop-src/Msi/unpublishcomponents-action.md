---
description: La acción UnpublishComponents administra la anulación de la inversión de los componentes enumerados en la tabla PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Acción UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1feaca4449ffa344eeda828334f879ebc12905406446dd14623e3b9c4474c6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810265"
---
# <a name="unpublishcomponents-action"></a>Acción UnpublishComponents

La acción UnpublishComponents administra la anulación de la inversión de los componentes enumerados en la tabla PublishComponent. Se trata de componentes en los que otros productos pueden producir errores. Esta acción quita información sobre los componentes publicados de la tabla [PublishComponent](publishcomponent-table.md) para la que la característica correspondiente está seleccionada actualmente para desinstalarse.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID que representa el identificador de componente de una característica anunciada. |
| \[2\] | Calificador del identificador del componente.                               |



 

