---
description: La acción InstallExecute ejecuta un script que contiene todas las operaciones de la secuencia de acciones desde el inicio de la instalación o la última acción InstallExecute o InstallExecuteAgain.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Acción InstallExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072072"
---
# <a name="installexecute-action"></a>Acción InstallExecute

La acción InstallExecute ejecuta un script que contiene todas las operaciones de la secuencia de acciones desde el inicio de la instalación o la última acción InstallExecute o [InstallExecuteAgain](installexecuteagain-action.md). La acción InstallExecute actualiza el sistema sin finalizar la transacción.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallExecute se encuentra entre [la acción InstallInitialize](installinitialize-action.md) y [la acción InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Observaciones

La [acción InstallExecuteAgain](installexecuteagain-action.md) hace lo mismo que la acción InstallExecute. Dado que las tablas de secuencia solo tienen una clave principal, la columna Acción, no se puede repetir la misma acción en una tabla de secuencia determinada. Existen dos acciones que hacen lo mismo, InstallExecute e InstallExecuteAgain, en los casos en los que la funcionalidad de InstallExecute es necesaria dos veces en la tabla [InstallExecuteSequence](installexecutesequence-table.md). Para obtener más información, [vea Usar una tabla de secuencia.](using-a-sequence-table.md)

 

 



