---
description: La acción ADMIN es una acción de nivel superior que se usa para realizar instalaciones administrativas.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Acción de administración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909126"
---
# <a name="admin-action"></a>Acción de administración

La acción ADMIN es una acción de nivel superior que se usa para realizar [instalaciones administrativas](administrative-installation.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

No se llama a la acción ADMIN desde la secuencia de la tabla de acciones, Windows Installer ejecuta esta acción cuando se llama a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) con el parámetro *szCommandLine* establecido en "Action = admin" o se llama al Msiexec.exe ejecutable de la línea de comandos con el modificador de la línea de comandos '/a '.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Tabla AdminExecuteSequence](adminexecutesequence-table.md)
</dt> </dl>

 

 



