---
description: Opcionalmente, un identificador de socket puede ser un identificador de archivo en Windows Sockets 2. Un identificador de socket de un proveedor winsock se puede usar con otras funciones que no son winsock, como ReadFile, WriteFile, ReadFileEx y WriteFileEx.
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: Identificadores de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91a9c9c642c317e9ab4ef897a20b68184df2c04324bcb76c33dea762e78c2846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740039"
---
# <a name="socket-handles"></a>Identificadores de socket

Opcionalmente, un identificador de socket puede ser un identificador de archivo en Windows Sockets 2. Un identificador de socket de un proveedor winsock se puede usar con otras funciones que no son de Winsock, como [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**WriteFile,**](/windows/win32/api/fileapi/nf-fileapi-writefile) [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)y [**WriteFileEx.**](/windows/win32/api/fileapi/nf-fileapi-writefileex)

El **miembro \_ XP1 IFS \_ HANDLES** de la estructura de información de protocolo de un proveedor determina si un identificador de socket de un proveedor es un identificador del sistema de archivos instalable (IFS). Los identificadores de socket que son identificadores IFS se pueden usar sin una penalización de rendimiento con otras funciones que no son winsock [**(ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) y [**WriteFile,**](/windows/win32/api/fileapi/nf-fileapi-writefile)por ejemplo). Los identificadores de socket que no son IFS cuando se usan con funciones que no son winsock (por ejemplo,**ReadFile** y **WriteFile)** tienen como resultado interacciones entre el proveedor y el sistema de archivos en los que se implica una sobrecarga de procesamiento adicional que puede provocar una reducción significativa del rendimiento. Cuando se usan identificadores de socket con funciones que no son winsock, los códigos de error propagados desde el sistema de archivos base no siempre se asignan a los códigos de error de Winsock. Por lo tanto, se recomienda que los identificadores de socket solo se utilicen con funciones Winsock.

No se debe usar un identificador de socket con la [**función DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) La presencia de proveedores de servicios en capas (LSP) puede provocar un error y no hay ninguna manera de que el proceso de destino importe el identificador de socket.

> [!Note]  
> Los proveedores de servicios por capas están en desuso. A partir de Windows 8 y Windows Server 2012, use [Windows de filtrado.](../fwp/windows-filtering-platform-start-page.md)

 

Windows Sockets 2 ha expandido ciertas funciones que transfieren datos entre sockets mediante identificadores. Las funciones ofrecen ventajas específicas de los sockets para transferir datos e incluyen [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)y [**WSADuplicateSocket.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa)

 

 
