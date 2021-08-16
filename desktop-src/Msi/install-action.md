---
description: La acción INSTALL es una acción de nivel superior denominada para instalar o quitar componentes.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Acción DE INSTALACIÓN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5f648084b7386465f6bb59dd6b523cb51489e4cb83677c0b5cb47fe845be42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811005"
---
# <a name="install-action"></a>Acción DE INSTALACIÓN

La acción INSTALL es una acción de nivel superior denominada para instalar o quitar componentes. Esta acción consulta la tabla [InstallUISequence y](installuisequence-table.md) la tabla [InstallExecuteSequence](installexecutesequence-table.md) para la acción que se va a ejecutar, la condición para la ejecución de la acción y el lugar de la acción en la secuencia:

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Comentarios

No se llama a la acción INSTALL desde la secuencia de la tabla de acciones, se pasa al instalador de Windows cuando se llama a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o se llama al ejecutable de línea de comandos Msiexec.exe con el modificador de línea de comandos **'/i',** o cuando se llama a cualquier función del instalador que pueda realizar una tarea de instalación, como [**MsiConfigureFeature,**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)o [**MsiInstallMissingFile.**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)

 

 



