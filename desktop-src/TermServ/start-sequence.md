---
title: Secuencia de inicio
description: Pasos para iniciar el protocolo personalizado.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af0716e39d1df96bbdf29f4a3abbb14e32bc752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268365"
---
# <a name="start-sequence"></a>Secuencia de inicio

Para iniciar el proveedor de protocolo, el servicio de Servicios de Escritorio remoto:

-   Recupera el nombre del agente de escucha y el CLSID del objeto de administrador de protocolos ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) del registro. Para obtener más información, consulte [registrar el administrador de protocolos](registering-the-custom-protocol.md).
-   Llama a [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) para inicializar el administrador de protocolos.
-   Crea un objeto de administrador de protocolos mediante el CLSID. Aunque haya varios agentes de escucha registrados para el mismo proveedor de protocolo, el servicio solo crea un objeto de administrador de protocolos.
-   Llama a [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) para indicar al objeto de administrador de protocolos que debe crear un objeto de escucha de [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) y devolverlo al servicio. El objeto de administrador de protocolos debe agregar una referencia al objeto de agente de escucha antes de devolverlo al servicio. El servicio liberará el objeto cuando el servicio se detenga o se elimine el agente de escucha.
-   Llama a [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) en el objeto de agente de escucha para que el agente de escucha pueda empezar a escuchar las conexiones entrantes.
-   Llama a [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) para detener la escucha del objeto de escucha.
-   Llama a [**UnInitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) para anular la inicialización del administrador de protocolos.

El agente de escucha crea un objeto [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) cuando un cliente intenta conectarse. El objeto de agente de escucha llama a [**Alconnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) para notificar al servicio servicios de escritorio remoto que un nuevo cliente está intentando conectarse o volver a conectarse, y pasa el objeto **IWRdsProtocolConnection** en esa llamada. A su vez, el servicio Servicios de Escritorio remoto devolverá un objeto [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) en esa llamada para que el protocolo pueda comunicarse con el servicio servicios de escritorio remoto según sea necesario. El servicio agrega una referencia al objeto de devolución de llamada antes de devolver y el protocolo debe liberar esa referencia cuando se cierre la conexión.

En la ilustración siguiente se muestra la interacción entre los distintos objetos durante el inicio.

![secuencia de inicio de RCM](images/protocol-startsequence.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuencia de llamada al método](method-call-sequence.md)
</dt> <dt>

[Secuencia de conexión](connection-sequence.md)
</dt> </dl>

 

 




