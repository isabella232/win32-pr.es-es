---
description: La acción InstallExecute ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la última acción InstallExecute o InstallExecuteAgain.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Acción InstallExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153877"
---
# <a name="installexecute-action"></a>Acción InstallExecute

La acción InstallExecute ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la última acción InstallExecute o [InstallExecuteAgain](installexecuteagain-action.md). La acción InstallExecute actualiza el sistema sin finalizar la transacción.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallExecute se incluye entre las acciones [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

La [acción InstallExecuteAgain](installexecuteagain-action.md) hace lo mismo que la acción InstallExecute. Dado que las tablas de secuencia solo tienen una clave principal, la columna de acción, no se puede repetir la misma acción en una tabla de secuencia determinada. Existen dos acciones que hacen lo mismo, InstallExecute y InstallExecuteAgain, para los casos en los que la funcionalidad de InstallExecute se necesita dos veces en la [tabla InstallExecuteSequence](installexecutesequence-table.md). Para obtener más información, vea [usar una tabla de secuencia](using-a-sequence-table.md).

 

 



