---
description: Opciones de SSPI para aplicaciones distribuidas
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: Opciones de SSPI para aplicaciones distribuidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160961"
---
# <a name="sspi-options-for-distributed-applications"></a>Opciones de SSPI para aplicaciones distribuidas

Los desarrolladores tienen muchas opciones para compilar aplicaciones distribuidas. [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) proporciona una capa de abstracción entre los protocolos de nivel de aplicación y [*los protocolos de seguridad*](../secgloss/s-gly.md). Las aplicaciones pueden aprovechar los protocolos de seguridad SSPI de varias maneras:

-   Llame directamente a rutinas SSPI (para aplicaciones tradicionales basadas en sockets).

    Las rutinas usan mensajes de solicitud/respuesta para implementar el protocolo [*de aplicación*](../secgloss/a-gly.md) que lleva datos relacionados con la seguridad de SSPI.

-   Use COM para llamar a las opciones de seguridad que se implementan mediante RPC autenticado y SSPI en niveles inferiores.

    Estas aplicaciones no llaman directamente a las funciones SSPI.

-   Use [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (WinSock) con la interfaz winSock extendida para permitir que los proveedores de transporte usen características de seguridad.

    Este enfoque integra el proveedor de [*compatibilidad de*](../secgloss/s-gly.md) seguridad (SSP) en la pila de red y proporciona servicios de seguridad y transporte a través de una interfaz común.

-   Use Windows [Internet Extensions API](../wininet/portal.md) (WinInet) y una interfaz diseñada para admitir protocolos de seguridad de Internet, como [*el protocolo Capa de sockets seguros*](../secgloss/s-gly.md) (SSL).

    Las aplicaciones usan la interfaz SSPI para el [proveedor de seguridad de](secure-channel.md) Canal seguro (Schannel) para implementar la seguridad de WinInet. Schannel es la implementación de Microsoft de SSL.

Varias funciones SSPI devuelven marcas de tiempo que representan el intervalo de vida de varios objetos. [*Los paquetes*](../secgloss/s-gly.md) de seguridad pueden mantener el tiempo y proporcionar marcas de tiempo de maneras diferentes, pero el uso de la hora local simplifica el trabajo de las aplicaciones que usan funciones SSPI.

 

 
