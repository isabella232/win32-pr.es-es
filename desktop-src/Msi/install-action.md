---
description: La acción INSTALL es una acción de nivel superior denominada para instalar o quitar componentes.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Acción INSTALL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171809"
---
# <a name="install-action"></a>Acción INSTALL

La acción INSTALL es una acción de nivel superior denominada para instalar o quitar componentes. Esta acción consulta la tabla [InstallUISequence](installuisequence-table.md) y la tabla [InstallExecuteSequence](installexecutesequence-table.md) para que la acción se ejecute, la condición de ejecución de la acción y el lugar de la acción en la secuencia:

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Observaciones

No se llama a la acción INSTALL desde la secuencia de la tabla de acciones, se pasa al instalador de Windows cuando se llama a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o se llama al archivo ejecutable de línea de comandos Msiexec.exe con el modificador de línea de comandos **'/i',** o cuando se llama a cualquier función del instalador que pueda realizar una tarea de instalación, como [**MsiConfigureFeature,**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)o [**MsiInstallMissingFile.**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)

 

 



