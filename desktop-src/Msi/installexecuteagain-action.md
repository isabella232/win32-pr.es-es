---
description: La acción InstallExecuteAgain ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la última acción InstallExecuteAgain o la última acción InstallExecute.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: Acción InstallExecuteAgain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001066"
---
# <a name="installexecuteagain-action"></a>Acción InstallExecuteAgain

La acción InstallExecuteAgain ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la última acción InstallExecuteAgain o la última [acción InstallExecute](installexecute-action.md). La acción InstallExecute actualiza el sistema sin finalizar la transacción. InstallExecuteAgain realiza la misma operación que la [acción InstallExecute](installexecute-action.md) , pero solo debe usarse después de InstallExecute.

InstallExecuteAgain siempre debe establecerse para que no se ejecute durante la eliminación. Para obtener más información, vea [usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallExecute se incluye entre las acciones [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

La acción InstallExecuteAgain hace lo mismo que la [acción InstallExecute](installexecute-action.md). Dado que las tablas de secuencia solo tienen una clave principal, la columna de acción, no se puede repetir la misma acción en una tabla de secuencia determinada. Existen dos acciones que hacen lo mismo, InstallExecute y InstallExecuteAgain, para los casos en los que la funcionalidad de InstallExecute se necesita dos veces en la [tabla InstallExecuteSequence](installexecutesequence-table.md). Para obtener más información, vea [usar una tabla de secuencia](using-a-sequence-table.md).

 

 



