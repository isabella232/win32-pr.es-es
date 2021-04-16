---
description: Aunque se anima a los proveedores de servicios de Windows Sockets a implementar Sockets como objetos del sistema de archivos instalables (IFS), la arquitectura de Winsock también admite proveedores de servicios cuyos identificadores de Socket no son objetos IFS.
ms.assetid: ed5e10f4-fa17-4a07-9cac-43767915b8e9
title: Asignación de descriptores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095301798eb850fc4eb63e1939712379b5ead85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705639"
---
# <a name="descriptor-allocation"></a>Asignación de descriptores

Aunque se anima a los proveedores de servicios de Windows Sockets a implementar Sockets como objetos del sistema de archivos instalables (IFS), la arquitectura de Winsock también admite proveedores de servicios cuyos identificadores de Socket no son objetos IFS. Los proveedores con identificadores de IFS indican esto a través del \_ \_ bit de atributo de XP1 IFS handles en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . (Nota: XP1 \_ \_El bit de atributo de los identificadores de IFS no se incluyó en la versión 2.0.8 de la especificación de API, pero se ha agregado a través del mecanismo de erratas.) Los clientes de Winsock SPI pueden aprovechar los proveedores cuyos descriptores de socket son identificadores IFS mediante el uso de estos descriptores con las funciones estándar de e/s de Windows, como [readfile](/windows/win32/api/fileapi/nf-fileapi-readfile) y [WriteFile](/windows/win32/api/fileapi/nf-fileapi-writefile).

Siempre que un proveedor de IFS crea un nuevo descriptor de socket, es obligatorio que el proveedor llame a [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) antes de proporcionar el nuevo identificador a un cliente de Windows Sockets SPI. Esta función toma un identificador de proveedor y un identificador IFS propuesto del proveedor como entrada y devuelve un identificador modificado (posiblemente). El proveedor IFS debe proporcionar solo el identificador modificado a su cliente, y todas las solicitudes del cliente solo hará referencia a este identificador modificado. Se garantiza que el identificador modificado es indistinguible del identificador propuesto en lo que se refiere al sistema operativo. Por lo tanto, en la mayoría de los casos, el proveedor de servicios solo usará el identificador modificado en todo su procesamiento interno. El propósito de esta función de modificación es permitir que el \_32.dll Ws2 optimice enormemente el proceso de identificación del proveedor de servicios asociado a un socket determinado.

Los proveedores que no devuelven identificadores IFS deben obtener un identificador válido del \_32.dll Ws2 a través de la llamada a [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) . El proveedor nonIFS debe ofrecer solo un identificador proporcionado por 2.DLL de Windows Sockets a su cliente, y todas las solicitudes del cliente solo hará referencia a estos identificadores. Como comodidad para los implementadores de proveedores de servicios, uno de los parámetros de entrada proporcionados por un proveedor en **WPUCreateSocketHandle** es un valor de contexto DWORD. El \_32.dll Ws2 asocia este valor de contexto al identificador de socket asignado y permite a un proveedor de servicios recuperar el valor de contexto en cualquier momento a través de la llamada a [**WPUQuerySocketHandleContext**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuquerysockethandlecontext) . Un uso típico de este valor de contexto sería almacenar un puntero a una estructura de datos de mantenimiento del proveedor de servicios que se usa para almacenar información de estado del socket.

 

 
