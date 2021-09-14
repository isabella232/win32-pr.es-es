---
title: Protocolo de escritorio remoto Provider API
description: Use la API Protocolo de escritorio remoto provider para crear un protocolo que proporcione comunicación entre el servicio Servicios de Escritorio remoto y varios clientes.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073366"
---
# <a name="remote-desktop-protocol-provider-api"></a>Protocolo de escritorio remoto Provider API

Use la API Protocolo de escritorio remoto provider para crear un protocolo que proporcione comunicación entre el servicio Servicios de Escritorio remoto y varios clientes.

Cuando Windows Server, se inicia Servicios de Escritorio remoto servicio de Connection Manager remoto (RCM). El servicio también inicia objetos de agente de escucha para los Protocolo de escritorio remoto que, a su vez, escuchan las conexiones de cliente. El servicio y los proveedores de protocolos son objetos en modo de usuario que se comunican mediante las API que se de abordan en esta documentación. Los proveedores de protocolos pueden comunicarse con controladores en modo kernel mediante controles de entrada y salida (IOCTLs). Esto se muestra en la siguiente ilustración.

![arquitectura de api de protocolo personalizado](images/protocol-architecture.png)

Microsoft ha implementado el Protocolo de escritorio remoto (RDP) para proporcionar comunicación entre el servicio Servicios de Escritorio remoto y las conexiones de cliente. Puede crear su propio protocolo mediante las interfaces, estructuras, uniones y tipos de enumeración que integran Protocolo de escritorio remoto Provider API. Para obtener más información, vea los temas siguientes:

<dl> <dt>

[Creación de un Protocolo de escritorio remoto de recursos](creating-a-custom-remote-protocol.md)
</dt> <dd>

Información sobre la creación de Protocolo de escritorio remoto proveedor. El administrador de protocolos se implementa como un servidor COM y se registra en una ubicación en la que se busca Servicios de Escritorio remoto servicio.

</dd> <dt>

[referencia Protocolo de escritorio remoto proveedor de recursos](custom-remote-protocol-reference.md)
</dt> <dd>

Contiene interfaces, estructuras, uniones y tipos de enumeración que permiten crear un Protocolo de escritorio remoto personalizado (RDP).

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Servicios de Escritorio remoto](about-terminal-services.md)
</dt> </dl>

 

 




