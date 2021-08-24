---
description: Para usar los recursos del sistema operativo de forma eficaz, una aplicación debe cerrar los archivos cuando ya no sean necesarios mediante la función CloseHandle. Si un archivo está abierto cuando finaliza una aplicación, el sistema lo cierra automáticamente.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Cerrar y eliminar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c74ad36f2f099b8d2430f52cc2c40b789862c691f56df1ccebcd20e82586ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696305"
---
# <a name="closing-and-deleting-files"></a>Cerrar y eliminar archivos

Para usar los recursos del sistema operativo de forma eficaz, una aplicación debe cerrar los archivos cuando ya no sean necesarios mediante la [**función CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Si un archivo está abierto cuando finaliza una aplicación, el sistema lo cierra automáticamente.

La [**función DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) se puede usar para eliminar un archivo al cerrarse. Un archivo no se puede eliminar hasta que se cierren todos los identificadores. Si no se puede eliminar un archivo, su nombre no se puede reutilizar. Para volver a usar un nombre de archivo inmediatamente, cambie el nombre del archivo existente.

Si va a eliminar un archivo o directorio abierto en un equipo remoto y ya se ha abierto en el equipo remoto sin el conjunto de permisos de recurso compartido de lectura, no llame a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ni [**a OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) para abrir primero el archivo o directorio para su eliminación. Si lo hace, se provocará una infracción de uso compartido.

 

 
