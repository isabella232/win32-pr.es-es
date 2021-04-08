---
title: API del proveedor de Protocolo de escritorio remoto
description: La API de proveedor de Protocolo de escritorio remoto se usa para crear un protocolo que proporcione comunicación entre el servicio Servicios de Escritorio remoto y varios clientes.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993817"
---
# <a name="remote-desktop-protocol-provider-api"></a>API del proveedor de Protocolo de escritorio remoto

La API de proveedor de Protocolo de escritorio remoto se usa para crear un protocolo que proporcione comunicación entre el servicio Servicios de Escritorio remoto y varios clientes.

Cuando se carga Windows Server, se inicia el servicio Servicios de Escritorio remoto (también conocido como administrador de conexiones remotas (RCM)). El servicio también inicia objetos de escucha para los proveedores de Protocolo de escritorio remoto que, a su vez, escuchan las conexiones de cliente. El servicio y los proveedores de protocolo son objetos de modo usuario que se comunican mediante las API descritas en esta documentación. Los proveedores de protocolos pueden comunicarse con los controladores de modo kernel mediante controles de entrada y salida (ioctl). Esto se muestra en la siguiente ilustración.

![arquitectura de API de protocolo personalizado](images/protocol-architecture.png)

Microsoft implementó el Protocolo de escritorio remoto (RDP) para proporcionar comunicación entre el servicio Servicios de Escritorio remoto y las conexiones de cliente. Puede crear su propio protocolo con las interfaces, estructuras, uniones y tipos de enumeración que componen la API de proveedor de Protocolo de escritorio remoto. Para obtener más información, vea los siguientes temas.

<dl> <dt>

[Creación de un proveedor de Protocolo de escritorio remoto](creating-a-custom-remote-protocol.md)
</dt> <dd>

Información sobre cómo crear un proveedor de Protocolo de escritorio remoto. El administrador de protocolos se implementa como un servidor COM y se registra en una ubicación en la que se busca cuando se inicia el servicio Servicios de Escritorio remoto.

</dd> <dt>

[Referencia del proveedor de Protocolo de escritorio remoto](custom-remote-protocol-reference.md)
</dt> <dd>

Contiene interfaces, estructuras, uniones y tipos de enumeración que permiten crear un Protocolo de escritorio remoto personalizado (RDP).

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Servicios de Escritorio remoto](about-terminal-services.md)
</dt> </dl>

 

 




