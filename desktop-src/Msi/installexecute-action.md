---
description: La acción InstallExecute ejecuta un script que contiene todas las operaciones de la secuencia de acciones desde el inicio de la instalación o la última acción InstallExecute o InstallExecuteAgain.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Acción InstallExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 249a83f283b3abee97fbddf99d755b158678726fbb36c066791e3f87ae718f46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946133"
---
# <a name="installexecute-action"></a>Acción InstallExecute

La acción InstallExecute ejecuta un script que contiene todas las operaciones de la secuencia de acciones desde el inicio de la instalación o la última acción InstallExecute o [InstallExecuteAgain](installexecuteagain-action.md). La acción InstallExecute actualiza el sistema sin finalizar la transacción.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallExecute se produce entre [la acción InstallInitialize](installinitialize-action.md) y [la acción InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Comentarios

La [acción InstallExecuteAgain](installexecuteagain-action.md) hace lo mismo que la acción InstallExecute. Dado que las tablas de secuencia solo tienen una clave principal, la columna Acción, no se puede repetir la misma acción en una tabla de secuencia determinada. Existen dos acciones que hacen lo mismo, InstallExecute e InstallExecuteAgain, en los casos en los que la funcionalidad de InstallExecute se necesita dos veces en la [tabla InstallExecuteSequence](installexecutesequence-table.md). Para obtener más información, [vea Usar una tabla de secuencia.](using-a-sequence-table.md)

 

 



