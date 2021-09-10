---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369439"
---
# <a name="microsoft-rpc"></a>Microsoft RPC

Rpc de Microsoft es un modelo para programar en un entorno informático distribuido. El objetivo de RPC es proporcionar comunicación transparente para que el cliente parezca comunicarse directamente con el servidor. La implementación de RPC de Microsoft es compatible con la RPC de Open Software Foundation (OSF) Distributed Computing Environment (DCE).

Puede configurar RPC para que use uno o varios transportes, uno o varios servicios de nombres y uno o varios servidores de seguridad. Las interfaces para esos proveedores se controlan mediante RPC. Dado que Rpc de Microsoft está diseñado para trabajar con varios proveedores, puede elegir los proveedores que mejor funcionen para la red. El transporte es responsable de transmitir los datos a través de la red. El servicio de nombres toma un nombre de objeto, como un moniker, y encuentra su ubicación en la red. El servidor de seguridad ofrece a las aplicaciones la opción de denegar el acceso a usuarios o grupos específicos. Consulte [Reglas de diseño de interfaz](interface-design-rules.md) para obtener información más detallada sobre la seguridad de las aplicaciones.

Además de las bibliotecas en tiempo de ejecución de RPC, Microsoft RPC incluye el lenguaje de definición de interfaz (IDL) y su compilador. Aunque el archivo IDL es una parte estándar de RPC, Microsoft lo ha mejorado para ampliar su funcionalidad para admitir interfaces COM personalizadas. El compilador Lenguaje de definición de interfaz de Microsoft (MIDL) usa el archivo IDL que describe la interfaz personalizada para generar varios archivos que se describen en Compilar y registrar un archivo [DLL de proxy.](building-and-registering-a-proxy-dll.md)

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

 

 




