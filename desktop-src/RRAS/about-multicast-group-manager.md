---
title: Acerca del administrador de grupo de multidifusión
description: En esta documentación se describe la tecnología del administrador de grupos de multidifusión (MGM).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- RRAS de administrador de grupo de multidifusión
- RRAS de administrador de grupo de multidifusión, descrito
- RRAS del servicio de enrutamiento y acceso remoto, administrador de grupo de multidifusión
- RRAS del servicio de enrutamiento y acceso remoto, administrador de grupo de multidifusión, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676172"
---
# <a name="about-multicast-group-manager"></a>Acerca del administrador de grupo de multidifusión

En esta documentación se describe la tecnología del administrador de grupos de multidifusión (MGM).

La multidifusión permite a un host enviar datos solo a los destinos que solicitan específicamente la recepción de los datos. De esta manera, la multidifusión difiere del envío de datos de difusión, ya que los datos de difusión se envían a todos los hosts.

La multidifusión ahorra ancho de banda de red, ya que los datos de multidifusión solo los reciben los hosts que solicitan los datos, y los datos viajan solo una vez. La multidifusión ahorra ancho de banda de servidor porque un servidor solo tiene que enviar un mensaje de multidifusión por red en lugar de un mensaje de unidifusión por receptor. Ejemplos de aplicaciones de multidifusión populares son las reuniones en línea y la radio por Internet.

La API MGM permite a los desarrolladores escribir protocolos de enrutamiento de multidifusión que interoperan con los enrutadores que ejecutan el administrador del grupo de multidifusión.

Cuando se habilita más de un protocolo de enrutamiento de multidifusión en un enrutador, el administrador del grupo de multidifusión coordina las operaciones entre todos los protocolos de enrutamiento. El administrador del grupo de multidifusión informa a cada protocolo de enrutamiento cuando se producen cambios en la pertenencia a grupos y cuando se reciben datos de multidifusión procedentes de un nuevo origen o de un nuevo grupo.

La API MGM proporciona las siguientes características:

-   Registro de protocolo
-   Administración de grupos
-   Enumeración de entradas de reenvío de multidifusión (MFE)
-   Definiciones de devolución de llamada para los protocolos de enrutamiento de multidifusión

En esta información general se describen los componentes de la arquitectura de multidifusión, los escenarios de cliente que se usan para interoperar con el administrador de grupos de multidifusión y las consideraciones de programación para usar la API MGM.

 

 




