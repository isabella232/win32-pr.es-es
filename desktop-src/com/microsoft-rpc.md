---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772787"
---
# <a name="microsoft-rpc"></a>Microsoft RPC

Microsoft RPC es un modelo de programación en un entorno de computación distribuida. El objetivo de RPC es proporcionar una comunicación transparente para que el cliente parezca que se comunica directamente con el servidor. La implementación de RPC de Microsoft es compatible con el RPC del entorno de computación distribuida (DCE) de Open Software Foundation (OSF).

Puede configurar RPC para usar uno o más transportes, uno o más servicios de nombre y uno o varios servidores de seguridad. RPC administra las interfaces a esos proveedores. Dado que Microsoft RPC está diseñado para trabajar con varios proveedores, puede elegir los proveedores que mejor funcionan para la red. El transporte es responsable de la transmisión de los datos a través de la red. El servicio de nombres toma un nombre de objeto, como un moniker, y busca su ubicación en la red. El servidor de seguridad ofrece a las aplicaciones la opción de denegar el acceso a usuarios o grupos específicos. Vea [reglas de diseño de interfaz](interface-design-rules.md) para obtener información más detallada sobre la seguridad de las aplicaciones.

Además de las bibliotecas en tiempo de ejecución de RPC, Microsoft RPC incluye el lenguaje de definición de interfaz (IDL) y su compilador. Aunque el archivo IDL es una parte estándar de RPC, Microsoft lo ha mejorado para ampliar su funcionalidad con el fin de admitir interfaces COM personalizadas. El compilador de Lenguaje de definición de interfaz de Microsoft (MIDL) utiliza el archivo IDL que describe la interfaz personalizada para generar varios archivos que se describen en [Building and registrating a proxy dll](building-and-registering-a-proxy-dll.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canal](channel.md)
</dt> <dt>

[Comunicación entre objetos](inter-object-communication.md)
</dt> <dt>

[Detalles de serialización](marshaling-details.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Stub](stub.md)
</dt> </dl>

 

 




