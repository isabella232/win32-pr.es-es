---
description: La acción InstallFinalize ejecuta un script que contiene todas las operaciones de la secuencia de acciones desde el inicio de la instalación o la ejecución de las acciones InstallExecute o InstallExecuteAgain.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: Acción InstallFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db8bd3ac9473fab868e5f7d83e760b39ca4dd6136faec987b5a7d2a3777bdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787045"
---
# <a name="installfinalize-action"></a>Acción InstallFinalize

La acción InstallFinalize ejecuta un script que contiene todas las operaciones de la secuencia de acciones desde el inicio de la instalación o la ejecución de las acciones [InstallExecute](installexecute-action.md) o [InstallExecuteAgain.](installexecuteagain-action.md) Esta acción marca el final de una transacción que comienza con [la acción InstallInitialize.](installinitialize-action.md)

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La [acción InstallInitialize](installinitialize-action.md) debe ir antes de la acción InstallFinalize.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Comentarios

Si se detecta que el producto está marcado para su eliminación completa,  las operaciones se agregan automáticamente al script para quitar la información de agregar o quitar programas en la información de **Panel de control** del producto, para anular el registro y anular la publicación del producto, y para quitar la base de datos local almacenada en caché de %WINDOWS%, si existe.

Los cambios del sistema realizados antes de la acción no se pueden restaurar después de ejecutar la acción InstallFinalize. La acción InstallFinalize actualiza el sistema con todas las operaciones determinadas hasta ese momento y, a continuación, finaliza la transacción.

 

 



