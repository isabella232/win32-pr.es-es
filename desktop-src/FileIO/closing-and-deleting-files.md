---
description: Para utilizar los recursos del sistema operativo de forma eficaz, una aplicación debe cerrar los archivos cuando ya no se necesiten mediante la función CloseHandle. Si un archivo está abierto cuando una aplicación finaliza, el sistema lo cierra automáticamente.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Cerrar y eliminar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3da31fe7ff38a1bbd1555e2685ceab9ae432574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669697"
---
# <a name="closing-and-deleting-files"></a>Cerrar y eliminar archivos

Para utilizar los recursos del sistema operativo de forma eficaz, una aplicación debe cerrar los archivos cuando ya no se necesiten mediante la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Si un archivo está abierto cuando una aplicación finaliza, el sistema lo cierra automáticamente.

La función [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) se puede usar para eliminar un archivo al cerrar. No se puede eliminar un archivo hasta que se cierren todos los identificadores. Si no se puede eliminar un archivo, no se puede volver a usar su nombre. Para volver a usar un nombre de archivo inmediatamente, cambie el nombre del archivo existente.

Si elimina un archivo o un directorio abierto en un equipo remoto y ya se ha abierto en el equipo remoto sin el permiso leer recurso compartido establecido, no llame a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o a [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) para abrir primero el archivo o el directorio para su eliminación. Si lo hace, se producirá una infracción de uso compartido.

 

 
