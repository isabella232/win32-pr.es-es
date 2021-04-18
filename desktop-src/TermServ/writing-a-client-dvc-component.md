---
title: Escritura de un módulo DVC de cliente
description: Para escribir un módulo de cliente de canal virtual dinámico (DVC), primero debe implementar y registrar un complemento de cliente Conexión a Escritorio remoto (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685565"
---
# <a name="writing-a-client-dvc-module"></a>Escritura de un módulo DVC de cliente

Para escribir un módulo de cliente de canal virtual dinámico (DVC), primero debe implementar y registrar un complemento de cliente Conexión a Escritorio remoto (RDC). El complemento DVC es una implementación de [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registrada como un objeto de modelo de objetos componentes (com).

> [!Note]  
> El complemento debe implementarse en un modelo de subprocesamiento libre. No se admite la implementación de modelo de apartamento.

 

A continuación se muestra una lista de interfaces que se implementan mediante objetos a los que se crea una instancia del complemento.



| Interfaz                                                        | Descripción                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | Permite que el cliente de Conexión a Escritorio remoto (RDC) cargue el complemento de cliente de Conexión a Escritorio remoto (RDC).<br/>                                                                 |
| [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | Notifica al complemento de cliente de Conexión a Escritorio remoto (RDC) sobre las solicitudes entrantes en un agente de escucha determinado.<br/>                                                                             |
| [**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | Recibe notificaciones sobre los cambios de estado del canal o los datos recibidos. Cada instancia de esta interfaz está asociada a una instancia de [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).<br/> |



 

A continuación se muestra una lista de interfaces implementadas por objetos a los que se crean instancias mediante el cliente Conexión a Escritorio remoto (RDC) y que forman parte del marco de trabajo.



| Interfaz                                                      | Descripción                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | Administra todos los complementos de cliente de Conexión a Escritorio remoto (RDC), agentes de escucha de DVC o canales virtuales estáticos.<br/> |
| [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | Administra los valores de configuración para cada agente de escucha para la conexión de DVC.<br/>                                |
| [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | Controla el estado del canal, así como las operaciones de escritura en el canal.<br/>                                           |



 

En la ilustración siguiente se muestra la relación entre el cliente de Conexión a Escritorio remoto (RDC) y el complemento de cliente de Conexión a Escritorio remoto (RDC).

![relación del cliente y el complemento](images/tsclient.png)

 

 





