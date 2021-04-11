---
title: Interfaces de proveedor de Protocolo de escritorio remoto
description: Interfaces admitidas por la API del proveedor de Protocolo de escritorio remoto.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85494e26c391095fbf97e8e408ee6b6181756c03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993816"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a>Interfaces de proveedor de Protocolo de escritorio remoto

La API del proveedor de Protocolo de escritorio remoto admite las siguientes interfaces.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

Expone los métodos llamados por el servicio Servicios de Escritorio remoto para configurar una conexión de cliente.

</dd> <dt>

[**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

Expone métodos que proporcionan información sobre el estado de una conexión de cliente y que realizan acciones para el cliente. El servicio Servicios de Escritorio remoto implementa esta interfaz y la llama el protocolo.

</dd> <dt>

[**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

Expone los métodos utilizados por el servicio de Servicios de Escritorio remoto para realizar el protocolo de enlace de licencias durante una secuencia de conexión.

</dd> <dt>

[**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

Expone métodos que solicitan que el protocolo inicie y deje de escuchar solicitudes de conexión de cliente.

</dd> <dt>

[**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

Expone métodos que notifican al servicio Servicios de Escritorio remoto que un cliente se ha conectado.

</dd> <dt>

[**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

Expone los métodos llamados por el servicio Servicios de Escritorio remoto para actualizar el estado de inicio de sesión y determinar cómo dirigir los mensajes de error de inicio de sesión.

</dd> <dt>

[**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

Expone los métodos que el servicio Servicios de Escritorio remoto utiliza para comunicarse con el proveedor de protocolo.

</dd> <dt>

[**IWRdsProtocolSettings**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

Expone métodos para recuperar y agregar la configuración relacionada con la Directiva.

</dd> <dt>

[**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

Expone los métodos llamados por el protocolo para notificar al servicio Servicios de Escritorio remoto que inicie o detenga el lado de destino de una sombra.

</dd> <dt>

[**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

Expone métodos que envían una notificación al proveedor del Protocolo sobre el estado de la sombra de la sesión.

</dd> <dt>

[**IWRdsRemoteFXGraphicsConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

Expone métodos relacionados con la manipulación y el conocimiento de los gráficos en la conexión del cliente.

</dd> <dt>

[Interfaces de proveedor de protocolo de escritorio en desuso](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

Las siguientes interfaces están desusadas y ya no deben usarse. En el caso de los proyectos nuevos, use en su lugar las interfaces del proveedor de Protocolo de escritorio remoto.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del proveedor de Protocolo de escritorio remoto](custom-remote-protocol-reference.md)
</dt> <dt>

[Enumeraciones de proveedor de Protocolo de escritorio remoto](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Estructuras de proveedor de Protocolo de escritorio remoto](custom-remote-protocol-structures.md)
</dt> <dt>

[Uniones de proveedor de Protocolo de escritorio remoto](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




