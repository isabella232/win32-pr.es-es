---
description: Descripciones de las funciones que se van a usar al trabajar con buzones de trabajo, clientes y servidores.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Operaciones de buzón de correo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716157"
---
# <a name="mailslot-operations"></a>Operaciones de buzón de correo

Cuando se trabaja con buzones de trabajo, los clientes y los servidores deben utilizar solo las funciones descritas en las tablas siguientes. No use otras funciones, aunque acepten identificadores de archivo o nombres de archivo como parámetros, ya que no están diseñados para trabajar con los buzones de archivos.

## <a name="mailslot-server-functions"></a>Funciones de servidor de buzón de correo

Los servidores de buzón de correo tienen el uso exclusivo de tres funciones, como se muestra en la tabla siguiente.



| Función                                   | Descripción                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | Crea un buzón de correo y devuelve un identificador de buzón de correo.                                                                                                                                                            |
| [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | Recupera el tamaño máximo del mensaje, el tamaño del procesador de mensajes, el tamaño del siguiente mensaje en el buzón de correo, el número de mensajes del buzón de correo y la cantidad de tiempo que una operación de lectura puede esperar a un mensaje. |
| [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | Cambia el tiempo de espera de lectura de un buzón de correo.                                                                                                                                                                    |



 

Los servidores de buzón de correo también usan las siguientes funciones.



| Función                                                         | Descripción                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | Duplica el identificador de buzón de correo.                     |
| [**Readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) | Recupera mensajes de un buzón de correo.                 |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Recupera la fecha y hora en que se creó un buzón. |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Establece la fecha y hora en que se creó un buzón.      |
| [**GetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | Recupera las propiedades del identificador de buzón de correo.        |
| [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | Establece las propiedades del identificador de buzón de correo.             |



 

## <a name="mailslot-client-functions"></a>Funciones de cliente de buzón de correo

Un proceso de cliente utiliza las siguientes funciones al interactuar con un buzón de correo.



| Función                                                             | Descripción                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | Cierra un identificador de buzón de correo para un proceso de cliente.  |
| [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | Crea un identificador de buzón de correo para un proceso de cliente. |
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | Duplica un identificador de buzón de correo.                   |
| [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) | Escribe datos en un buzón de correo.                      |



 

 

 
