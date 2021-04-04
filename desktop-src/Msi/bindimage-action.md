---
description: La acción BindImage enlaza cada archivo ejecutable o DLL que se debe enlazar a los archivos dll importados por él.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Acción BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909057"
---
# <a name="bindimage-action"></a>Acción BindImage

La acción BindImage enlaza cada archivo ejecutable o DLL que se debe enlazar a los archivos dll importados por él. La acción BindImage actúa en cada archivo de la tabla [BindImage](bindimage-table.md) , pero solo en los que se van a instalar localmente. El instalador calcula la dirección virtual de cada función importada de todos los archivos dll y, a continuación, guarda la dirección virtual calculada en la [*tabla de direcciones de importación*](i-gly.md) (IAT) de la imagen de importación.

La acción BindImage llama internamente a la API de Windows **BindImageEx** .

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción BindImage debe aparecer después de la acción [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción     |
|-------|--------------------------------|
| \[1\] | Identificador del archivo ejecutable. |



 

 

 



