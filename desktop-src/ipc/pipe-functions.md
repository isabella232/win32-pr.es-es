---
description: La siguiente función se usa con canalizaciones anónimas.
ms.assetid: 9e80783e-9641-4cbd-9c28-a8efe6b9efaa
title: Funciones de canalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0ef895fe8b987f19f025b6a21ef4c3a5dc3cb24db5458595c25708066e8a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481609"
---
# <a name="pipe-functions"></a>Funciones de canalización

La siguiente función se usa con canalizaciones anónimas.



| Función                         | Descripción                |
|----------------------------------|----------------------------|
| [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) | Crea una canalización anónima. |



 

Las siguientes funciones se usan con canalizaciones con nombre.



| Función                                                                 | Descripción                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)                                   | Se conecta a una canalización de tipo mensaje, escribe y lee desde la canalización y, a continuación, cierra la canalización.                                                                                                                                       |
| [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)                             | Permite que un proceso de servidor de canalización con nombre espere a que un proceso de cliente se conecte a una instancia de una canalización con nombre.                                                                                                                         |
| [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)                               | Crea una instancia de una canalización con nombre y devuelve un identificador para las operaciones de canalización posteriores. Un proceso de cliente se conecta a una canalización con nombre mediante la [**función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**o CallNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) |
| [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe)                       | Desconecta el extremo del servidor de una instancia de canalización con nombre de un proceso de cliente.                                                                                                                                                          |
| [**GetNamedPipeClientComputerName**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientcomputernamea) | Recupera el nombre del equipo cliente para la canalización con nombre especificada.                                                                                                                                                                    |
| [**GetNamedPipeClientProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientprocessid)       | Recupera el identificador de proceso de cliente para la canalización con nombre especificada.                                                                                                                                                               |
| [**GetNamedPipeClientSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientsessionid)       | Recupera el identificador de sesión de cliente para la canalización con nombre especificada.                                                                                                                                                               |
| [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea)               | Recupera información sobre una canalización con nombre especificada.                                                                                                                                                                                 |
| [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo)                             | Recupera información sobre la canalización con nombre especificada.                                                                                                                                                                               |
| [**GetNamedPipeServerProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserverprocessid)       | Recupera el identificador de proceso de servidor para la canalización con nombre especificada.                                                                                                                                                               |
| [**GetNamedPipeServerSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserversessionid)       | Recupera el identificador de sesión del servidor para la canalización con nombre especificada.                                                                                                                                                               |
| [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)    | Suplanta una aplicación cliente de canalización con nombre.                                                                                                                                                                                       |
| [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)                                   | Copia los datos de una canalización con nombre o anónima en un búfer sin quitarlo de la canalización.                                                                                                                                         |
| [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)               | Establece el modo de lectura y el modo de bloqueo de la canalización con nombre especificada.                                                                                                                                                               |
| [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)                           | Combina las funciones que escriben un mensaje en y leen un mensaje de la canalización con nombre especificada en una sola operación de red.                                                                                                    |
| [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)                                   | Espera hasta que transcurra un intervalo de tiempo de espera o una instancia de la canalización con nombre especificada está disponible para una conexión.                                                                                                            |



 

 

 
