---
title: Crear un objeto a través de un objeto de clase
description: Crear un objeto a través de un objeto de clase
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38787e7bc32151446cda6ff0a4cfe3f23a0f6eda
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369499"
---
# <a name="creating-an-object-through-a-class-object"></a>Crear un objeto a través de un objeto de clase

Con la importancia cada vez mayor de las redes de equipos, es necesario que los clientes y servidores interactúen de forma fácil y eficaz, tanto si residen en la misma máquina como en una red. Para ello, es fundamental la capacidad de un cliente para iniciar un servidor, crear una instancia del objeto del servidor y tener acceso a los métodos de las interfaces del objeto .

COM proporciona extensiones a este proceso COM básico que hacen que sea prácticamente sin problemas a través de una red. Si un cliente puede identificar el servidor a través de su CLSID, llamar a algunas funciones sencillas permite a COM realizar todo el trabajo de buscar e iniciar el servidor y activar el objeto. Las subclaves del Registro permiten a los servidores remotos registrar su ubicación, por lo que el cliente no requiere esa información. En el caso de las aplicaciones que desean aprovechar las características de red, las funciones de creación de objetos COM permiten una mayor flexibilidad y eficacia.

Para obtener más información, vea los temas siguientes:

-   [Objetos de clase COM y CLSID](com-class-objects-and-clsids.md)
-   [Buscar un objeto remoto](locating-a-remote-object.md)
-   [Funciones auxiliares de creación de instancias](instance-creation-helper-functions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes y servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 




