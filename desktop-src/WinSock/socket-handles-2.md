---
description: Un identificador de socket puede ser opcionalmente un identificador de archivo en Windows Sockets 2. Un identificador de socket de un proveedor Winsock se puede usar con otras funciones que no son de Winsock, como ReadFile, WriteFile, ReadFileEx y WriteFileEx.
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: Identificadores de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6ca8ed935819e018a59c52fb43dcf816530c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715860"
---
# <a name="socket-handles"></a>Identificadores de socket

Un identificador de socket puede ser opcionalmente un identificador de archivo en Windows Sockets 2. Un identificador de socket de un proveedor Winsock se puede usar con otras funciones que no son de Winsock, como [**readfile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)y [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex).

El miembro **XP1 \_ IFS \_ Handles** de la estructura de información de protocolo para un proveedor determina si un identificador de socket de un proveedor es un identificador de sistema de archivos instalable (IFS). Los identificadores de socket que son identificadores IFS se pueden usar sin una penalización de rendimiento con otras funciones que no son de Winsock (por ejemplo,[**readfile**](/windows/win32/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile)). Los identificadores de socket que no son IFS cuando se usan con funciones que no son de Winsock (**readfile** y **WriteFile**, por ejemplo) producen interacciones entre el proveedor y el sistema de archivos donde implica una sobrecarga de procesamiento adicional que puede dar lugar a una penalización significativa del rendimiento. Cuando se usan identificadores de socket con funciones que no son de Winsock, los códigos de error propagados desde el sistema de archivos base no se asignan siempre a los códigos de error de Winsock. Por lo tanto, se recomienda usar identificadores de socket solo con funciones de Winsock.

No se debe usar un identificador de socket con la función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) . La presencia de proveedores de servicios por capas (LSP) puede provocar que se produzca un error y que el proceso de destino no importe el identificador de socket.

> [!Note]  
> Los proveedores de servicios superpuestos están desusados. A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).

 

Windows Sockets 2 ha expandido ciertas funciones que transfieren datos entre Sockets mediante los controladores. Las funciones ofrecen ventajas específicas para los sockets para transferir datos e incluyen [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)y [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa).

 

 
