---
description: La acción UnregisterTypeLibraries anula el registro de las bibliotecas de tipos del sistema. Esta acción se aplica a cada archivo enumerado en la tabla TypeLib que se desencadena para desinstalarse.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Acción UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6066dbac7e63696f838375261fbb63e8348faf630a7439ec7531cdd71d4ace97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810125"
---
# <a name="unregistertypelibraries-action"></a>Acción UnregisterTypeLibraries

La acción UnregisterTypeLibraries anula el registro de las bibliotecas de tipos del sistema. Esta acción se aplica a cada archivo enumerado en la [tabla TypeLib](typelib-table.md) que se desencadena para desinstalarse.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción UnregisterTypeLibraries debe ir antes de [la acción RemoveFiles.](removefiles-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                        |
|-------|---------------------------------------------------|
| \[1\] | [GUID](guid.md) de una biblioteca de tipos no registrada. |



 

 

 



