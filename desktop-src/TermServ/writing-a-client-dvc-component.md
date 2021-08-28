---
title: Escritura de un módulo DVC de cliente
description: Para escribir un módulo de cliente de canal virtual dinámico (DVC), primero debe implementar y registrar un complemento de cliente Conexión a Escritorio remoto (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa9f365034ff7771baf8eaeca102d7156f592e71d0cedffc97cef6d75b81fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008274"
---
# <a name="writing-a-client-dvc-module"></a>Escritura de un módulo DVC de cliente

Para escribir un módulo de cliente de canal virtual dinámico (DVC), primero debe implementar y registrar un complemento de cliente Conexión a Escritorio remoto (RDC). El complemento DVC es una implementación de [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registrada como un objeto de Modelo de objetos componentes (COM).

> [!Note]  
> El complemento debe implementarse en un modelo de subprocesamiento libre. No se admite la implementación del modelo de apartamento.

 

A continuación se muestra una lista de interfaces implementadas por objetos de los que el complemento crea instancias.



| Interfaz                                                        | Descripción                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | Permite que el Conexión a Escritorio remoto cliente de Conexión a Escritorio remoto (RDC) que el cliente de Conexión a Escritorio remoto (RDC) cargue.<br/>                                                                 |
| [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | Notifica al Conexión a Escritorio remoto cliente de Conexión a Escritorio remoto (RDC) acerca de las solicitudes entrantes en un agente de escucha determinado.<br/>                                                                             |
| [**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | Recibe notificaciones sobre los cambios de estado del canal o los datos recibidos. Cada instancia de esta interfaz está asociada a una instancia de [**IWTSVirtualChannel.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)<br/> |



 

A continuación se muestra una lista de interfaces implementadas por objetos de los que el cliente de Conexión a Escritorio remoto (RDC) crea instancias y forman parte del marco de trabajo.



| Interfaz                                                      | Descripción                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | Administra todos los Conexión a Escritorio remoto cliente (RDC), los agentes de escucha DVC o los canales virtuales estáticos.<br/> |
| [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | Administra los valores de configuración de cada agente de escucha para la conexión DVC.<br/>                                |
| [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | Controla el estado del canal, así como las escrituras en el canal.<br/>                                           |



 

En la ilustración siguiente se muestra la relación entre el cliente Conexión a Escritorio remoto (RDC) y el complemento de cliente Conexión a Escritorio remoto (RDC).

![relación de cliente y complemento](images/tsclient.png)

 

 





