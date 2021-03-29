---
title: Instrucciones de aplicación de servicio de nombres
description: Al desarrollar una aplicación distribuida, debe proporcionar a los usuarios de la aplicación un método para especificar el nombre con el que pueden registrar la aplicación en la base de datos del servicio de nombres.
ms.assetid: cda997b3-6031-4c0f-affc-c766ba4b7fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67af441da7a51917ae92751345e860e6b0fc92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994412"
---
# <a name="name-service-application-guidelines"></a>Instrucciones de aplicación de servicio de nombres

Al desarrollar una aplicación distribuida, debe proporcionar a los usuarios de la aplicación un método para especificar el nombre con el que pueden registrar la aplicación en la base de datos del servicio de nombres. Este método puede constar de un archivo de datos, una entrada de la línea de comandos o un cuadro de diálogo.

Aunque la arquitectura del servicio de nombres de RPC admite varios métodos para organizar las entradas del servidor de una aplicación, se optimiza para las búsquedas. Como resultado, las actualizaciones frecuentes pueden afectar al rendimiento del servicio de nombres y de la aplicación. Para evitar la exportación innecesaria de información, elija un diseño que permita al servidor determinar si su información está en la base de datos del servicio de nombres. Además, cada instancia de servidor debe exportarse a su propio nombre de entrada. De lo contrario, será difícil que una instancia cambie sus UUID de objeto o de protocolo compatibles sin alterar la información de otra instancia.

El método siguiente evita estos errores y proporciona un buen rendimiento, independientemente del servicio de nombres que use la red.

Para empezar, diseñe la aplicación de forma que la primera vez que se inicie una instancia de servidor determinada, seleccione un nombre de entrada de servidor único y guarde este nombre en el registro junto con la información de configuración de la aplicación. A continuación, haga que exporte los identificadores de enlace y el UUID de objeto, si los hay, a su entrada de servicio de nombres.

Las siguientes invocaciones de la instancia de servidor deben comprobar que la entrada del servicio de nombres esté presente y que contenga el conjunto correcto de UUID de objeto y los identificadores de enlace. Una entrada que falta puede significar que un administrador la ha quitado o que se ha producido un corte de suministro eléctrico de la información del servicio de nombres. Es importante comprobar que los identificadores de enlace de la entrada son correctos; Si un administrador agrega compatibilidad con TCP/IP a un equipo, por ejemplo, los servidores RPC escucharán en esa secuencia de protocolos cuando llamen a [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs). Sin embargo, si el servidor no actualiza la entrada del servicio de nombres, no se informará a los clientes de que se admite TCP.

Cuando el cliente importa, debe especificar **null** como nombre de la entrada. Si se especifica **null** , las funciones de la biblioteca RPC de Microsoft buscan la interfaz en todas las entradas del servicio de nombres en el dominio o grupo de trabajo del equipo cliente, con lo que se busca la información de cada instancia.

Si utiliza UUID de objeto para representar objetos conocidos como las impresoras, puede utilizar una variación de este método. En lugar de exportar enlaces a una entrada, diseñe la aplicación para que cada instancia cree una entrada para cada objeto compatible, como "/.:/ Printers/LASER1 "y"/.:/ Printers/Laser2 ". A continuación, haga que el servidor exporte sus identificadores de enlace a cada entrada del servidor, junto con el UUID del objeto correspondiente a esa entrada.

En este caso, un cliente puede buscar un recurso por su nombre importando desde la entrada del servidor correspondiente; no requiere el UUID del objeto del recurso. Si tiene el UUID de recurso, pero no el nombre, puede importar desde la entrada **null** .

 

 




