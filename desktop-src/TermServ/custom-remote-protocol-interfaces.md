---
title: Protocolo de escritorio remoto interfaces de proveedor de servicios
description: Interfaces compatibles con la API Protocolo de escritorio remoto proveedor de aplicaciones.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bde36cb70f937559dce20a73a485ec109a2cf6c6ae6c687655963c70e6ce22b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681235"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a>Protocolo de escritorio remoto interfaces de proveedor de servicios

Las siguientes interfaces son compatibles con la API Protocolo de escritorio remoto provider.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

Expone los métodos a los que llama Servicios de Escritorio remoto servicio para configurar una conexión de cliente.

</dd> <dt>

[**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

Expone métodos que proporcionan información sobre el estado de una conexión de cliente y que realizan acciones para el cliente. Esta interfaz se implementa mediante el servicio Servicios de Escritorio remoto y se llama mediante el protocolo .

</dd> <dt>

[**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

Expone los métodos usados por Servicios de Escritorio remoto servicio para realizar el protocolo de enlace de licencias durante una secuencia de conexión.

</dd> <dt>

[**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

Expone métodos que solicitan que el protocolo inicie y deje de escuchar las solicitudes de conexión de cliente.

</dd> <dt>

[**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

Expone métodos que notifican al Servicios de Escritorio remoto que un cliente se ha conectado.

</dd> <dt>

[**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

Expone los métodos a los que llama Servicios de Escritorio remoto servicio para actualizar el estado de inicio de sesión y determinar cómo dirigir los mensajes de error de inicio de sesión.

</dd> <dt>

[**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

Expone los métodos que el Servicios de Escritorio remoto utiliza para comunicarse con el proveedor de protocolos.

</dd> <dt>

[**IWRdsProtocolSettings**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

Expone métodos para recuperar y agregar configuraciones relacionadas con directivas.

</dd> <dt>

[**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

Expone los métodos a los que llama el protocolo para notificar al servicio Servicios de Escritorio remoto que inicie o detenga el lado de destino de una sombra.

</dd> <dt>

[**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

Expone métodos que notifican al proveedor de protocolos el estado del sombreado de sesión.

</dd> <dt>

[**IWRdsRemoteFXGraphicsConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

Expone métodos relacionados con la manipulación y comprensión de los gráficos en la conexión de cliente.

</dd> <dt>

[Interfaces de proveedor de protocolos de escritorio en desuso](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

Las interfaces siguientes han quedado en desuso y ya no se deben usar. Para los proyectos nuevos, use las interfaces Protocolo de escritorio remoto provider interfaces en su lugar.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[referencia Protocolo de escritorio remoto proveedor de recursos](custom-remote-protocol-reference.md)
</dt> <dt>

[Protocolo de escritorio remoto provider enumerations](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Protocolo de escritorio remoto de proveedores de servicios](custom-remote-protocol-structures.md)
</dt> <dt>

[Protocolo de escritorio remoto de proveedor de servicios](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




