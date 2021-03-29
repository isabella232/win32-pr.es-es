---
description: Cuando un proceso abre un archivo mediante la función CreateFile, se asocia un identificador de archivo hasta que el proceso finaliza o el identificador se cierra con la función CloseHandle.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Identificadores de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912862"
---
# <a name="file-handles"></a>Identificadores de archivo

Cuando un proceso abre un archivo mediante la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , se asocia un *identificador de archivo* hasta que el proceso finaliza o el identificador se cierra con la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . El identificador de archivo se utiliza para identificar el archivo en muchas llamadas a funciones.

Cada objeto de archivo y identificador de archivo es generalmente único para cada proceso que abre un archivo, lo único que se produce cuando se duplica un identificador de archivo mantenido por un proceso, o cuando un proceso secundario hereda los identificadores de archivo del proceso primario. En estas situaciones, estos identificadores de archivo son únicos, pero se ve un solo objeto de archivo compartido. Consulte [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) para obtener más información sobre la duplicación de identificadores de archivos que se mantienen en los procesos.

Tenga en cuenta que, mientras que los identificadores de archivo suelen ser privados para un proceso, los datos de archivo a los que apunta el punto de control no son. Por lo tanto, los procesos y subprocesos que comparten el mismo archivo deben sincronizar su acceso. Para la mayoría de las operaciones en un archivo, un proceso identifica el archivo a través de su grupo privado de identificadores.

 

 
