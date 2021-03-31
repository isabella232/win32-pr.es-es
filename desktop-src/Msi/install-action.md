---
description: La acción de instalación es una acción de nivel superior llamada para instalar o quitar componentes.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Acción de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082486"
---
# <a name="install-action"></a>Acción de instalación

La acción de instalación es una acción de nivel superior llamada para instalar o quitar componentes. Esta acción consulta la [tabla InstallUISequence](installuisequence-table.md) y la [tabla InstallExecuteSequence](installexecutesequence-table.md) para la acción que se va a ejecutar, la condición para la ejecución de la acción y el lugar de la acción en la secuencia:

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

No se llama a la acción de instalación desde dentro de la secuencia de la tabla de acciones, se pasa a Windows Installer cuando se llama a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) , o se llama al Msiexec.exe ejecutable de línea de comandos con el modificador de línea de comandos '**/i**', o cuando se llama a cualquier función de instalador que puede realizar una tarea de instalación, como [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)o [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).

 

 



