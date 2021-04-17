---
description: 'Hay dos tipos distintos de aplicaciones de red de socket: servidor y cliente.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: Acerca de los servidores y clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a951d23ba1c6ad4f0f5ffd1f674b056a36c3f8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696408"
---
# <a name="about-servers-and-clients"></a>Acerca de los servidores y clientes

Hay dos tipos distintos de aplicaciones de red de socket: servidor y cliente.

Los servidores y los clientes tienen distintos comportamientos. por lo tanto, el proceso de crearlos es diferente. A continuación se muestra el modelo general para crear un cliente y un servidor TCP/IP de transmisión por secuencias.

## <a name="server"></a>Servidor

1.  Inicialice Winsock.
2.  Cree un socket.
3.  Enlazar el socket.
4.  Escuche en el socket para un cliente.
5.  Acepte una conexión desde un cliente.
6.  Recibir y enviar datos.
7.  Desconectarte.

## <a name="client"></a>Remoto

1.  Inicialice Winsock.
2.  Cree un socket.
3.  Conectarse al servidor.
4.  Enviar y recibir datos.
5.  Desconectarte.

> [!Note]  
> Algunos de los pasos son los mismos para un cliente y un servidor. Estos pasos se implementan casi exactamente igual. Algunos de los pasos de esta guía serán específicos para el tipo de aplicación que se va a crear.

 

Primer paso: [creación de una aplicación de Winsock básica](creating-a-basic-winsock-application.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



