---
description: La acción BindImage enlaza cada archivo ejecutable o DLL que se debe enlazar a los archivos DLL importados por él.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Acción BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d621728de551c182d6678561b2ef5daf649fb8fae840f47a460d83a4d38f3635
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638781"
---
# <a name="bindimage-action"></a>Acción BindImage

La acción BindImage enlaza cada archivo ejecutable o DLL que se debe enlazar a los archivos DLL importados por él. La acción BindImage actúa en cada archivo de la [tabla BindImage,](bindimage-table.md) pero solo en los que se van a instalar localmente. El instalador calcula la dirección virtual de cada función importada de todos los archivos DLL y, a continuación, guarda la dirección virtual calculada en la tabla de direcciones de importación [](i-gly.md) (IAT) de la imagen de importación.

La acción BindImage llama internamente a **bindImageEx** Windows API.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción BindImage debe ir después de [la acción InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción     |
|-------|--------------------------------|
| \[1\] | Identificador de archivo del ejecutable. |



 

 

 



