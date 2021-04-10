---
title: Servidores de In-Process
description: Servidores de In-Process
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268735"
---
# <a name="in-process-servers"></a>Servidores de In-Process

Si implementa una aplicación de servidor OLE como un servidor en proceso, una DLL que se ejecuta en el espacio de proceso de la aplicación contenedora, en lugar de un servidor local, un archivo EXE que se ejecuta en su propio espacio de proceso, la comunicación entre el contenedor y el servidor se simplifica porque la comunicación entre los dos puede adoptar la forma de llamadas de función normales. No es necesario realizar llamadas a procedimientos remotos porque las dos aplicaciones se ejecutan en el mismo espacio de proceso. Como cabría esperar, los objetos que administran el cálculo de referencias de parámetros también son innecesarios, aunque se pueden agregar en el archivo DLL sin interferir con la comunicación entre el contenedor y el servidor.

Cuando una aplicación de servidor OLE se implementa como un servidor en proceso, no es necesario un controlador de objetos independiente porque el propio servidor reside en el espacio de proceso del cliente. La diferencia principal entre un servidor en proceso y un controlador de objetos es que el servidor puede administrar el objeto en estado de ejecución mientras el controlador no puede. Una consecuencia de esta diferencia es que un servidor debe proporcionar una interfaz de usuario para manipular el objeto en ejecución, mientras que un controlador delega este requisito en el servidor del objeto. En la creación de un servidor de tipo en curso, se puede Agregar en el controlador predeterminado de OLE, lo que permite administrar las tareas básicas, como la visualización, el almacenamiento y las notificaciones, mientras que solo se implementan los servicios que el controlador no proporciona o no implementa de la forma que necesite.

Para obtener más información, vea los temas siguientes:

-   [Ventajas](advantages.md)
-   [Desventajas](disadvantages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 




