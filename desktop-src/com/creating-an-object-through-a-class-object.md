---
title: Crear un objeto a través de un objeto de clase
description: Crear un objeto a través de un objeto de clase
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea76e8ecb826d8bba6e9f0ea84af894f4632d3d4bb5f41708d84c2f37e416b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993505"
---
# <a name="creating-an-object-through-a-class-object"></a>Crear un objeto a través de un objeto de clase

Con la importancia creciente de las redes de equipos, es necesario que los clientes y servidores interactúen de forma fácil y eficaz, tanto si residen en la misma máquina como a través de una red. Para ello, es fundamental la capacidad de un cliente de iniciar un servidor, crear una instancia del objeto del servidor y tener acceso a los métodos de las interfaces del objeto .

COM proporciona extensiones a este proceso COM básico que lo hacen prácticamente sin problemas a través de una red. Si un cliente puede identificar el servidor a través de su CLSID, llamar a algunas funciones simples permite a COM realizar todo el trabajo de buscar e iniciar el servidor y activar el objeto. Las subclaves del Registro permiten a los servidores remotos registrar su ubicación, por lo que el cliente no requiere esa información. En el caso de las aplicaciones que desean aprovechar las características de red, las funciones de creación de objetos COM permiten una mayor flexibilidad y eficacia.

Para obtener más información, vea los temas siguientes:

-   [Objetos de clase COM y CLSID](com-class-objects-and-clsids.md)
-   [Buscar un objeto remoto](locating-a-remote-object.md)
-   [Funciones auxiliares de creación de instancias](instance-creation-helper-functions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes y servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 




