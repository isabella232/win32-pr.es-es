---
title: Secuencia de inicio
description: Pasos para iniciar el protocolo personalizado.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29dbb899905dd96e806ffe17a0eafd0091ad97b547ba9f172527ab0acc1b2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000554"
---
# <a name="start-sequence"></a>Secuencia de inicio

Para iniciar el proveedor de protocolos, Servicios de Escritorio remoto servicio:

-   Recupera el nombre del agente de escucha y el CLSID del objeto de administrador de protocolos ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) del Registro. Para obtener más información, [vea Registrar el Administrador de protocolos.](registering-the-custom-protocol.md)
-   Llama [**a Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) para inicializar el administrador de protocolos.
-   Crea un objeto de administrador de protocolos mediante el CLSID. Incluso si hay varios agentes de escucha registrados para el mismo proveedor de protocolos, el servicio solo crea un objeto de administrador de protocolos.
-   Llama [**a CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) para indicar al objeto de administrador de protocolos que cree un objeto de escucha [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) y lo devuelva al servicio. El objeto de administrador de protocolos debe agregar una referencia al objeto de agente de escucha antes de devolverlo al servicio. El servicio liberará el objeto cuando se detenga el servicio o se elimine el agente de escucha.
-   Llama [**a StartListen en**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) el objeto de agente de escucha para que el agente de escucha pueda empezar a escuchar las conexiones entrantes.
-   Llama [**a StopListen para**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) impedir que el objeto del agente de escucha escuche.
-   Llama [**a Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) para desinitializar el administrador de protocolos.

El agente de escucha [**crea un objeto IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) cuando un cliente intenta conectarse. El objeto de agente de escucha llama a [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) para notificar al servicio Servicios de Escritorio remoto que un nuevo cliente está intentando conectarse o volver a conectarse, y pasa el objeto **IWRdsProtocolConnection** en esa llamada. El Servicios de Escritorio remoto devolverá a su vez un objeto [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) en esa llamada para que el protocolo pueda comunicarse con el servicio Servicios de Escritorio remoto según sea necesario. El servicio agrega una referencia al objeto de devolución de llamada antes de devolverse y el protocolo debe liberar esa referencia cuando se cierre la conexión.

En la ilustración siguiente se muestra la interacción entre los distintos objetos durante el inicio.

![rcm start sequence](images/protocol-startsequence.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Secuencia de llamadas de método](method-call-sequence.md)
</dt> <dt>

[Secuencia de conexión](connection-sequence.md)
</dt> </dl>

 

 




