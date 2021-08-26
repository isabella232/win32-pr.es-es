---
description: 'Hay dos tipos distintos de aplicaciones de red de socket: Servidor y Cliente.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: Acerca de los servidores y clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d8016d1fc9c23b901a03a924cd0e3ade3982dc2e1bf0db277eac47170d89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898645"
---
# <a name="about-servers-and-clients"></a>Acerca de los servidores y clientes

Hay dos tipos distintos de aplicaciones de red de socket: Servidor y Cliente.

Los servidores y los clientes tienen comportamientos diferentes; por lo tanto, el proceso de crearlos es diferente. Lo que sigue es el modelo general para crear un servidor TCP/IP de streaming y un cliente.

## <a name="server"></a>Servidor

1.  Inicialice Winsock.
2.  Cree un socket.
3.  Enlace el socket.
4.  Escucha en el socket de un cliente.
5.  Acepte una conexión de un cliente.
6.  Recibir y enviar datos.
7.  Desconectarte.

## <a name="client"></a>Cliente

1.  Inicialice Winsock.
2.  Cree un socket.
3.  Conectarse al servidor.
4.  Enviar y recibir datos.
5.  Desconectarte.

> [!Note]  
> Algunos de los pasos son los mismos para un cliente y un servidor. Estos pasos se implementan casi exactamente iguales. Algunos de los pasos de esta guía serán específicos del tipo de aplicación que se va a crear.

 

Primer paso: [Creación de una aplicación Winsock básica](creating-a-basic-winsock-application.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



