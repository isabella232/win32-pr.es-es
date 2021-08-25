---
description: Descripciones de las funciones que se usan al trabajar con mailslots, clientes y servidores.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Operaciones de Mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fefce55c70971f5d611c41d473180897706bc04960509818cb0d092c7f83825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829505"
---
# <a name="mailslot-operations"></a>Operaciones de Mailslot

Al trabajar con mailslots, los clientes y servidores solo deben usar las funciones que se deban analizar en las tablas siguientes. No use otras funciones, aunque acepten identificadores de archivo o nombres de archivo como parámetros, ya que no están diseñados para trabajar con mailslots.

## <a name="mailslot-server-functions"></a>Funciones de servidor mailslot

Los servidores Mailslot tienen un uso exclusivo de tres funciones, como se muestra en la tabla siguiente.



| Función                                   | Descripción                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | Crea un mailslot y devuelve un identificador mailslot.                                                                                                                                                            |
| [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | Recupera el tamaño máximo del mensaje, el tamaño de mailslot, el tamaño del siguiente mensaje en mailslot, el número de mensajes en mailslot y la cantidad de tiempo que una operación de lectura puede esperar un mensaje. |
| [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | Cambia el tiempo de espera de lectura de un mailslot.                                                                                                                                                                    |



 

Los servidores mailslot también usan las siguientes funciones.



| Función                                                         | Descripción                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | Duplica el identificador mailslot.                     |
| [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) | Recupera mensajes de un mailslot.                 |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Recupera la fecha y hora en que se creó un mailslot. |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Establece la fecha y hora en que se creó un mailslot.      |
| [**GetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | Recupera las propiedades del identificador mailslot.        |
| [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | Establece las propiedades del identificador mailslot.             |



 

## <a name="mailslot-client-functions"></a>Funciones de cliente mailslot

Un proceso de cliente usa las siguientes funciones al interactuar con un mailslot.



| Función                                                             | Descripción                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | Cierra un identificador mailslot para un proceso de cliente.  |
| [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | Crea un identificador mailslot para un proceso de cliente. |
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | Duplica un identificador mailslot.                   |
| [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) | Escribe datos en un mailslot.                      |



 

 

 
