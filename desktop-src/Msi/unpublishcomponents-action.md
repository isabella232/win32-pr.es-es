---
description: La acción UnpublishComponents administra la anulación de la inversión de los componentes enumerados en la tabla PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Acción UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171613"
---
# <a name="unpublishcomponents-action"></a>Acción UnpublishComponents

La acción UnpublishComponents administra la anulación de la inversión de los componentes enumerados en la tabla PublishComponent. Se trata de componentes en los que otros productos pueden producir errores. Esta acción quita información sobre los componentes publicados de la [tabla PublishComponent](publishcomponent-table.md) para la que la característica correspondiente está seleccionada actualmente para desinstalarse.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID que representa el identificador de componente de una característica anunciada. |
| \[2\] | Calificador del identificador del componente.                               |



 

