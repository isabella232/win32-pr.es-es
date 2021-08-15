---
description: Estrategias para comunicarse con varios clientes de canalización y atender varias instancias de canalización.
ms.assetid: c764bde5-e053-4124-b859-1d2839ada918
title: Instancias de canalización con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 188ec90912132e5cdd972ac2b0a4ab3f4c1f97ebbb7bc35e20b75b04eebbfa15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481966"
---
# <a name="named-pipe-instances"></a>Instancias de canalización con nombre

El servidor de canalización más sencillo crea una instancia única de una canalización, se conecta a un solo cliente, se comunica con el cliente, se desconecta del cliente, cierra el identificador de canalización y finaliza. Sin embargo, es más común que un servidor de canalización se comunique con varios clientes de canalización. Un servidor de canalización podría usar una única instancia de canalización para conectarse con varios clientes de canalización mediante la conexión y la desconexión de cada cliente en secuencia, pero el rendimiento sería deficiente. El servidor de canalización debe crear varias instancias de canalización para controlar de forma eficaz varios clientes simultáneamente.

Hay tres estrategias básicas para el mantenimiento de varias instancias de canalización.

-   Cree un subproceso independiente para cada instancia de la canalización. Para obtener un ejemplo de un servidor de canalización multiproceso, vea [Servidor de canalización multiproceso](multithreaded-pipe-server.md).
-   Use operaciones superpuestas especificando una [**estructura OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) en las funciones [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)y [**ConnectNamedPipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) Para obtener un ejemplo, vea [Servidor de canalización con nombre que usa E/S superpuesta.](named-pipe-server-using-overlapped-i-o.md)
-   Use operaciones superpuestas mediante las funciones [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx,**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) que especifican una rutina de finalización que se ejecutará cuando se complete la operación. Para obtener un ejemplo, vea [Servidor de canalización con nombre mediante rutinas de finalización](named-pipe-server-using-completion-routines.md).

El servidor de canalización multiproceso es más fácil de escribir, ya que el subproceso de cada instancia controla las comunicaciones para un cliente de canalización única. El sistema asigna tiempo de procesador a cada subproceso según sea necesario. Pero cada subproceso usa recursos del sistema, lo que es una desventaja para un servidor de canalización que controla un gran número de clientes.

Con un servidor de un solo subproceso, es más fácil coordinar las operaciones que afectan a varios clientes y es más fácil proteger los recursos compartidos frente al acceso simultáneo por parte de varios clientes. El desafío de un servidor de un solo subproceso es que requiere coordinación de operaciones superpuestas para asignar tiempo de procesador para controlar las necesidades simultáneas de los clientes.

 

 
