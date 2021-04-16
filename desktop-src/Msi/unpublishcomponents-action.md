---
description: La acción UnpublishComponents administra el desanuncio de los componentes enumerados en la tabla PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Acción UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104424307"
---
# <a name="unpublishcomponents-action"></a>Acción UnpublishComponents

La acción UnpublishComponents administra el desanuncio de los componentes enumerados en la tabla PublishComponent. Se trata de componentes que pueden ser errores en otros productos. Esta acción quita información sobre los componentes publicados de la [tabla PublishComponent](publishcomponent-table.md) para los que la característica correspondiente está seleccionada actualmente para desinstalarse.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID que representa el identificador de componente de una característica anunciada. |
| \[2\] | Calificador del ID. de componente.                               |



 

