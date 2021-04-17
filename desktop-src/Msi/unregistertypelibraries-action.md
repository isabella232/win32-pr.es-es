---
description: La acción UnregisterTypeLibraries anula el registro de las bibliotecas de tipos del sistema. Esta acción se aplica a cada archivo que aparece en la tabla TypeLib que se desencadena para desinstalarse.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Acción UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653073"
---
# <a name="unregistertypelibraries-action"></a>Acción UnregisterTypeLibraries

La acción UnregisterTypeLibraries anula el registro de las bibliotecas de tipos del sistema. Esta acción se aplica a cada archivo que aparece en la tabla [typelib](typelib-table.md) que se desencadena para desinstalarse.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción UnregisterTypeLibraries debe ser anterior a la acción [RemoveFiles](removefiles-action.md) .

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                        |
|-------|---------------------------------------------------|
| \[1\] | [GUID](guid.md) de una biblioteca de tipos no registrada. |



 

 

 



