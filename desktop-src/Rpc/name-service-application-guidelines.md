---
title: Directrices de aplicación de servicio de nombres
description: Al desarrollar la aplicación distribuida, debe proporcionar a los usuarios de la aplicación un método para especificar el nombre con el que pueden registrar la aplicación en la base de datos de servicio de nombres.
ms.assetid: cda997b3-6031-4c0f-affc-c766ba4b7fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e0e79f8ddb9e2076da8d7b8d2c275cb1b1941f6867bfea68dd46bc6c352d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927834"
---
# <a name="name-service-application-guidelines"></a>Directrices de aplicación de servicio de nombres

Al desarrollar la aplicación distribuida, debe proporcionar a los usuarios de la aplicación un método para especificar el nombre con el que pueden registrar la aplicación en la base de datos de servicio de nombres. Este método puede constar de un archivo de datos, una entrada de línea de comandos o un cuadro de diálogo.

Aunque la arquitectura del servicio de nombres RPC admite varios métodos para organizar las entradas de servidor de una aplicación, está optimizada para búsquedas. Como resultado, las actualizaciones frecuentes pueden dificultar el rendimiento del servicio de nombres y la aplicación. Para evitar exportar información innecesariamente, elija un diseño que permita al servidor determinar si su información está en la base de datos del servicio de nombres. Además, cada instancia de servidor debe exportarse a su propio nombre de entrada. De lo contrario, será difícil para una instancia cambiar sus UUD de objeto admitidos o secuencias de protocolo sin alterar la información de otra instancia.

El método siguiente evita estos problemas y proporciona un buen rendimiento, independientemente del servicio de nombres que use la red.

Para empezar, diseñe la aplicación para que la primera vez que se inicie una instancia de servidor determinada, seleccione un nombre de entrada de servidor único y guarde este nombre en el Registro junto con la otra información de configuración de la aplicación. A continuación, haga que exporte sus identificadores de enlace y UUID de objeto, si los hay, a su entrada de servicio de nombre.

Las invocaciones posteriores de la instancia del servidor deben comprobar que la entrada del servicio de nombres está presente y contiene el conjunto correcto de UUID de objeto y identificadores de enlace. Una entrada que falta puede significar que un administrador la quitó o que una interrupción del suministro eléctrico provocó la pérdida de la información del servicio de nombres. Es importante comprobar que los identificadores de enlace de la entrada son correctos; si un administrador agrega compatibilidad con TCP/IP a un equipo, por ejemplo, los servidores RPC escucharán en esa secuencia de protocolo cuando llamen a [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs). Sin embargo, si el servidor no actualiza la entrada del servicio de nombres, no se informará a los clientes de que se admite TCP.

Cuando el cliente importa, debe especificar **NULL como** nombre de entrada. Si se especifica **NULL,** las funciones de la biblioteca RPC de Microsoft buscan la interfaz en todas las entradas del servicio de nombres del dominio o grupo de trabajo del equipo cliente, con lo que se busca la información de cada instancia.

Si usa UUID de objeto para representar objetos conocidos como impresoras, puede usar una variación de este método. En lugar de exportar enlaces a una entrada, diseñe la aplicación para que cada instancia cree una entrada para cada objeto admitido, como "/.:/ printers/Laser1" y "/.:/ printers/Laser2". A continuación, haga que el servidor exporte sus identificadores de enlace a cada entrada del servidor, junto con el UUID del objeto pertinente para esa entrada.

En este caso, un cliente puede buscar un recurso por nombre importando desde la entrada del servidor correspondiente; no requiere el UUID del objeto del recurso. Si tiene el UUID del recurso, pero no el nombre, puede importar desde la **entrada** NULL.

 

 




