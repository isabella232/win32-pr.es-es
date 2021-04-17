---
description: La acción RemoveShortcuts administra la eliminación de un acceso directo anunciado cuya característica está seleccionada para la desinstalación o un acceso directo no anunciado cuyo componente está seleccionado para la desinstalación. Para obtener más información, vea la tabla de acceso directo.
ms.assetid: 897e8a13-d9c5-4f98-8785-c0f053a11f3d
title: Acción RemoveShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151f5fac6733e61b7ba27320a5e79c522abcc3e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652786"
---
# <a name="removeshortcuts-action"></a>Acción RemoveShortcuts

La acción RemoveShortcuts administra la eliminación de un acceso directo anunciado cuya característica está seleccionada para la desinstalación o un acceso directo no anunciado cuyo componente está seleccionado para la desinstalación. Para obtener más información, vea la [tabla de acceso directo](shortcut-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RemoveShortcuts debe ser anterior a la acción [CreateShortcuts](createshortcuts-action.md) .

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | Identificador del acceso directo quitado. |



 

 

 



