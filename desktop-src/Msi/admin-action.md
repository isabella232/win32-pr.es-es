---
description: La acción ADMIN es una acción de nivel superior que se usa para realizar instalaciones administrativas.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Acción admin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785bd69a8de7da1df9a812f7e89d589b6e939b3eedd6b3cecb66bf86407636cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145938"
---
# <a name="admin-action"></a>Acción admin

La acción ADMIN es una acción de nivel superior que se usa para realizar [instalaciones administrativas.](administrative-installation.md)

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Comentarios

No se llama a la acción ADMIN desde dentro de la secuencia de la tabla de acciones, el instalador de Windows ejecuta esta acción cuando se llama a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) con el parámetro *szCommandLine* establecido en "ACTION=ADMIN" o se llama al ejecutable de línea de comandos Msiexec.exe con el modificador de línea de comandos "/a".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Tabla AdminExecuteSequence](adminexecutesequence-table.md)
</dt> </dl>

 

 



