---
description: La acción InstallExecuteAgain ejecuta un script que contiene todas las operaciones de la secuencia de acciones desde el inicio de la instalación, la última acción InstallExecuteAgain o la última acción InstallExecute.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: Acción InstallExecuteAgain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2133fcf7acee7027337864eb8e33b6b297499e96979155f066538edbd6fec00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893985"
---
# <a name="installexecuteagain-action"></a>Acción InstallExecuteAgain

La acción InstallExecuteAgain ejecuta un script que contiene todas las operaciones de la secuencia de acciones desde el inicio de la instalación, la última acción InstallExecuteAgain o la última [acción InstallExecute](installexecute-action.md). La acción InstallExecute actualiza el sistema sin finalizar la transacción. InstallExecuteAgain realiza la misma operación que la acción [InstallExecute,](installexecute-action.md) pero solo se debe usar después de InstallExecute.

InstallExecuteAgain siempre debe establecerse para que no se ejecute durante la eliminación. Para obtener información, [vea Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallExecute se encuentra entre [la acción InstallInitialize](installinitialize-action.md) y [la acción InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Comentarios

La acción InstallExecuteAgain hace lo mismo que [la acción InstallExecute](installexecute-action.md). Dado que las tablas de secuencia solo tienen una clave principal, la columna Acción, no se puede repetir la misma acción en una tabla de secuencia determinada. Existen dos acciones que hacen lo mismo, InstallExecute e InstallExecuteAgain, para los casos en los que la funcionalidad de InstallExecute se necesita dos veces en la tabla [InstallExecuteSequence](installexecutesequence-table.md). Para obtener más información, [vea Usar una tabla de secuencia.](using-a-sequence-table.md)

 

 



