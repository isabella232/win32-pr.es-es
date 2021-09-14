---
description: La acción LaunchConditions consulta la tabla LaunchCondition y evalúa cada instrucción condicional registrada allí. Si se produce un error en cualquiera de estas instrucciones condicionales, se muestra un mensaje de error al usuario y se finaliza la instalación.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Acción LaunchConditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071979"
---
# <a name="launchconditions-action"></a>Acción LaunchConditions

La acción LaunchConditions consulta la [tabla LaunchCondition](launchcondition-table.md) y evalúa cada instrucción condicional registrada allí. Si se produce un error en cualquiera de estas instrucciones condicionales, se muestra un mensaje de error al usuario y se finaliza la instalación.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción LaunchConditions es opcional. Normalmente, esta acción es la primera de la secuencia, pero la acción [AppSearch](appsearch-action.md) se puede secuenciar antes de la acción LaunchConditions. Si hay condiciones de inicio que no se aplican a todos los modos de instalación, se debe usar la propiedad de modo de instalación adecuada en una expresión condicional en la tabla de secuencia adecuada.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

 

 



