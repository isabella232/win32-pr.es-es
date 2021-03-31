---
description: Opciones de SSPI para aplicaciones distribuidas
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: Opciones de SSPI para aplicaciones distribuidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907607"
---
# <a name="sspi-options-for-distributed-applications"></a>Opciones de SSPI para aplicaciones distribuidas

Los desarrolladores tienen muchas opciones para compilar aplicaciones distribuidas. La [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) proporciona una capa de abstracción entre los protocolos de nivel de aplicación y los [*protocolos de seguridad*](../secgloss/s-gly.md). Las aplicaciones pueden aprovechar los protocolos de seguridad SSPI de varias maneras:

-   Llamar a rutinas SSPI directamente (para aplicaciones tradicionales basadas en socket).

    Las rutinas usan mensajes de solicitud/respuesta para implementar el [*Protocolo de aplicación*](../secgloss/a-gly.md) que transporta los datos relacionados con la seguridad de SSPI.

-   Use COM para llamar a las opciones de seguridad que se implementan mediante RPC autenticado y SSPI en niveles inferiores.

    Estas aplicaciones no llaman directamente a las funciones SSPI.

-   Use [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (Winsock) con la interfaz Winsock extendida para permitir que los proveedores de transporte utilicen las características de seguridad.

    Este enfoque integra el [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) en la pila de red y proporciona servicios de transporte y seguridad a través de una interfaz común.

-   Use la [API de extensiones de Internet de Windows](../wininet/portal.md) (WinInet) y una interfaz diseñada para admitir protocolos de seguridad de Internet como el protocolo [*capa de sockets seguros*](../secgloss/s-gly.md) (SSL).

    Las aplicaciones usan la interfaz SSPI en el proveedor de seguridad de [canal seguro](secure-channel.md) (Schannel) para implementar la seguridad de Wininet. Schannel es la implementación de Microsoft de SSL.

Varias funciones SSPI devuelven marcas de tiempo que representan la duración de varios objetos. Los [*paquetes de seguridad*](../secgloss/s-gly.md) pueden mantener el tiempo y proporcionar marcas de tiempo de maneras diferentes, pero el uso de la hora local simplifica el trabajo de las aplicaciones que usan funciones SSPI.

 

 
