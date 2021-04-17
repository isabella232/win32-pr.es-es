---
description: Estrategias para comunicarse con varios clientes de canalización y servicio de varias instancias de canalización.
ms.assetid: c764bde5-e053-4124-b859-1d2839ada918
title: Instancias de canalización con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b7d1ec591996e83853ae6faede899ecd4e4ea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697430"
---
# <a name="named-pipe-instances"></a>Instancias de canalización con nombre

El servidor de canalización más sencillo crea una instancia única de una canalización, se conecta a un solo cliente, se comunica con el cliente, se desconecta del cliente, cierra el identificador de canalización y termina. Sin embargo, es más común que un servidor de canalización se comunique con varios clientes de canalización. Un servidor de canalización podría usar una instancia de una sola canalización para conectarse con varios clientes de canalización mediante la conexión y la desconexión de cada cliente en secuencia, pero el rendimiento sería bajo. El servidor de canalización debe crear varias instancias de canalización para controlar eficazmente varios clientes simultáneamente.

Hay tres estrategias básicas para atender varias instancias de canalización.

-   Cree un subproceso independiente para cada instancia de la canalización. Para obtener un ejemplo de un servidor de canalización multiproceso, vea [servidor de canalización multiproceso](multithreaded-pipe-server.md).
-   Use operaciones superpuestas especificando una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) en las funciones [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)y [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) . Para obtener un ejemplo, vea [servidor de canalización con nombre mediante e/s superpuesta](named-pipe-server-using-overlapped-i-o.md).
-   Use las operaciones superpuestas con las funciones [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) , que especifican la rutina de finalización que se va a ejecutar cuando se complete la operación. Para obtener un ejemplo, vea [servidor de canalización con nombre mediante rutinas de finalización](named-pipe-server-using-completion-routines.md).

El servidor de canalización multiproceso es más fácil de escribir, ya que el subproceso de cada instancia controla las comunicaciones para un cliente de una sola canalización. El sistema asigna tiempo de procesador a cada subproceso según sea necesario. Pero cada subproceso utiliza recursos del sistema, lo que es una desventaja para un servidor de canalización que controla un gran número de clientes.

Con un servidor de un solo subproceso, es más fácil coordinar las operaciones que afectan a varios clientes y es más fácil proteger los recursos compartidos frente al acceso simultáneo de varios clientes. El desafío de un servidor de un solo subproceso es que requiere la coordinación de las operaciones superpuestas para asignar el tiempo de procesador para controlar las necesidades simultáneas de los clientes.

 

 
