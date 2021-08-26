---
title: Acerca del Administrador de grupos de multidifusión
description: En esta documentación se describe la tecnología de Administrador de grupos de multidifusión (MGM).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- RRAS del Administrador de grupos de multidifusión
- RRAS del Administrador de grupos de multidifusión, descrito
- RRAS del servicio de enrutamiento y acceso remoto, Administrador de grupos de multidifusión
- RRAS del servicio de enrutamiento y acceso remoto, administrador de grupos de multidifusión, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f83dc2b212f7d70d04b4a3ec08bf07e664fa2d67d9c638233a4e8e914369c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030935"
---
# <a name="about-multicast-group-manager"></a>Acerca del Administrador de grupos de multidifusión

En esta documentación se describe la tecnología de Administrador de grupos de multidifusión (MGM).

La multidifusión permite a un host enviar datos solo a los destinos que solicitan específicamente recibir los datos. De esta manera, la multidifusión difiere del envío de datos de difusión, ya que los datos de difusión se envían a todos los hosts.

La multidifusión ahorra ancho de banda de red porque los datos de multidifusión solo los reciben los hosts que solicitan los datos y los datos viajan a través de cualquier vínculo solo una vez. La multidifusión ahorra ancho de banda del servidor porque un servidor solo tiene que enviar un mensaje de multidifusión por red en lugar de un mensaje de unidifusión por receptor. Algunos ejemplos de aplicaciones de multidifusión populares son las reuniones en línea y la radio de Internet.

La API de MGM permite a los desarrolladores escribir protocolos de enrutamiento de multidifusión que interoperan con enrutadores que ejecutan el administrador de grupos de multidifusión.

Cuando se habilita más de un protocolo de enrutamiento de multidifusión en un enrutador, el administrador de grupos de multidifusión coordina las operaciones entre todos los protocolos de enrutamiento. El administrador de grupos de multidifusión informa a cada protocolo de enrutamiento cuando se producen cambios de pertenencia a grupos y cuando se reciben datos de multidifusión de un nuevo origen o destinados a un nuevo grupo.

La API de MGM proporciona las siguientes características:

-   Registro de protocolos
-   Administración de grupos
-   Enumeración de entrada de reenvío de multidifusión (MFE)
-   Definiciones de devolución de llamada para protocolos de enrutamiento de multidifusión

En esta introducción se describen los componentes de la arquitectura de multidifusión, los escenarios de cliente que se usan para interoperar con el administrador de grupos de multidifusión y las consideraciones de programación para usar la API de MGM.

 

 




