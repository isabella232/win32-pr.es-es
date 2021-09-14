---
description: Una canalización con nombre es una canalización con nombre un solo sentido o dúplex para la comunicación entre el servidor de canalización y uno o varios clientes de canalización.
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: Canalizaciones con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0675244e09b7c202b4fa6b67f6268392b1b260f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172294"
---
# <a name="named-pipes"></a>Canalizaciones con nombre

Una *canalización con nombre* es una canalización con nombre un solo sentido o dúplex para la comunicación entre el servidor de canalización y uno o varios clientes de canalización. Todas las instancias de una canalización con nombre comparten el mismo nombre de canalización, pero cada instancia tiene sus propios búferes y identificadores, y proporciona un canal independiente para la comunicación entre cliente y servidor. El uso de instancias de permite que varios clientes de canalización usen la misma canalización con nombre simultáneamente.

Cualquier proceso puede acceder a canalizaciones con nombre, sujetas a comprobaciones de seguridad, lo que hace que las canalizaciones con nombre sea una forma sencilla de comunicación entre procesos relacionados o no relacionados.

Cualquier proceso puede actuar como servidor y cliente, lo que permite la comunicación punto a punto. Como se usa aquí, el término servidor de canalización hace referencia a un proceso que crea una canalización con nombre y el término cliente de canalización hace referencia a un proceso que se conecta a una instancia de una canalización con nombre. La función del lado servidor para crear instancias de una canalización con nombre [**es CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) La función del lado servidor para aceptar una conexión es [**ConnectNamedPipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) Un proceso de cliente se conecta a una canalización con nombre mediante la [**función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**o CallNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)

Las canalizaciones con nombre se pueden usar para proporcionar comunicación entre procesos en el mismo equipo o entre procesos en equipos diferentes a través de una red. Si el servicio de servidor se está ejecutando, todas las canalizaciones con nombre son accesibles de forma remota. Si piensa usar una canalización con nombre solo localmente, deniegue el acceso a NT AUTHORITY \\ NETWORK o cambie a RPC local.

Para obtener más información, vea los temas siguientes:

-   [Nombres de canalización](pipe-names.md)
-   [Modos de apertura de canalización con nombre](named-pipe-open-modes.md)
-   [Modos de tipo de canalización con nombre, lectura y espera](named-pipe-type-read-and-wait-modes.md)
-   [Instancias de canalización con nombre](named-pipe-instances.md)
-   [Operaciones de canalización con nombre](named-pipe-operations.md)
-   [Entrada y salida sincrónicas y superpuestas](synchronous-and-overlapped-input-and-output.md)
-   [Derechos de acceso y seguridad de canalización con nombre](named-pipe-security-and-access-rights.md)
-   [Suplantación de un cliente de canalización con nombre](impersonating-a-named-pipe-client.md)
-   [Uso de canalizaciones](using-pipes.md)

 

 
