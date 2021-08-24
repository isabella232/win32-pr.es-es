---
title: In-Process server
description: In-Process server
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccc4c65db19e4ed567a2fe6105fa4d81e9c52cc9165556d9f388d8af181eee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854535"
---
# <a name="in-process-servers"></a>In-Process server

Si implementa una aplicación de servidor OLE como un servidor en proceso (un archivo DLL que se ejecuta en el espacio de proceso de la aplicación contenedora) en lugar de como un servidor local (un exe que se ejecuta en su propio espacio de proceso), la comunicación entre el contenedor y el servidor se simplifica porque la comunicación entre los dos puede tomar la forma de llamadas de función normales. Las llamadas a procedimientos remotos no son necesarias porque las dos aplicaciones se ejecutan en el mismo espacio de proceso. Como se esperaría, los objetos que administran la serialización de parámetros también son innecesarios, aunque pueden agregarse dentro del archivo DLL sin interferir con la comunicación entre el contenedor y el servidor.

Cuando una aplicación de servidor OLE se implementa como un servidor en proceso, no se requiere un controlador de objetos independiente porque el propio servidor reside en el espacio de proceso del cliente. La principal diferencia entre un servidor en proceso y un controlador de objetos es que el servidor puede administrar el objeto en un estado en ejecución mientras el controlador no puede. Una consecuencia de esta diferencia es que un servidor debe proporcionar una interfaz de usuario para manipular el objeto en ejecución, mientras que un controlador delega este requisito en el servidor del objeto. Al crear un servidor en proceso, puede agregar en el controlador predeterminado OLE, lo que le permite controlar tareas básicas, como la presentación, el almacenamiento y las notificaciones, mientras implementa solo los servicios que el controlador no proporciona o no implementa de la manera que necesita.

Para obtener más información, vea los temas siguientes:

-   [Ventajas](advantages.md)
-   [Desventajas](disadvantages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 




