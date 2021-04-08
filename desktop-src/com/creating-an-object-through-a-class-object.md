---
title: Crear un objeto a través de un objeto de clase
description: Crear un objeto a través de un objeto de clase
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38787e7bc32151446cda6ff0a4cfe3f23a0f6eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994579"
---
# <a name="creating-an-object-through-a-class-object"></a>Crear un objeto a través de un objeto de clase

Con la creciente importancia de las redes de equipos, es necesario que los clientes y los servidores interactúen de forma sencilla y eficaz, independientemente de que residan en el mismo equipo o en una red. Crucial para esto es la capacidad de un cliente de iniciar un servidor, crear una instancia del objeto del servidor y tener acceso a los métodos de las interfaces en el objeto.

COM proporciona extensiones a este proceso COM básico que lo hacen prácticamente sin problemas a través de una red. Si un cliente es capaz de identificar el servidor a través de su CLSID, llamar a algunas funciones simples permite a COM realizar todo el trabajo de buscar e iniciar el servidor y activar el objeto. Las subclaves del registro permiten a los servidores remotos registrar su ubicación, por lo que el cliente no requiere esa información. En el caso de las aplicaciones que desean aprovechar las características de red, las funciones de creación de objetos COM permiten una mayor flexibilidad y eficacia.

Para obtener más información, vea los temas siguientes:

-   [Objetos de clase COM y CLSID](com-class-objects-and-clsids.md)
-   [Buscar un objeto remoto](locating-a-remote-object.md)
-   [Funciones auxiliares de creación de instancia](instance-creation-helper-functions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes y servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 




