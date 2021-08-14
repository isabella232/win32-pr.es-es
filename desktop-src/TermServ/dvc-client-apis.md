---
title: API de cliente de DVC
description: Las API de cliente de canal virtual dinámico (DVC) se implementan específicamente para el cliente Conexión a Escritorio remoto (RDC) de la conexión.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557f51adbf10562465f93a101e502632a791d5c272b278c5a8b7ea6124637913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130821"
---
# <a name="dvc-client-apis"></a>API de cliente de DVC

Las API de cliente de canal virtual dinámico (DVC) se implementan específicamente para el cliente Conexión a Escritorio remoto (RDC) de la conexión. Algunas de las API se implementan mediante el marco DVC y otras las implementa el desarrollador del complemento. Algunas de las API se usan para admitir el complemento de cliente Conexión a Escritorio remoto (RDC) y no están directamente relacionadas con el transporte de datos.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

Permite que el Conexión a Escritorio remoto de cliente de Conexión a Escritorio remoto (RDC) que el cliente de Conexión a Escritorio remoto (RDC) cargue.

</dd> <dt>

[**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

Administra los valores de configuración de cada agente de escucha para la conexión dinámica del canal virtual (DVC).

</dd> <dt>

[**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

Se usa para notificar al Conexión a Escritorio remoto cliente de Conexión a Escritorio remoto (RDC) las solicitudes entrantes en un agente de escucha determinado.

</dd> <dt>

[**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

Administra todos los Conexión a Escritorio remoto cliente (RDC) y los agentes de escucha de canal virtual dinámico (DVC).

</dd> <dt>

[**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

Se usa para controlar el estado del canal y escribe en el canal.

</dd> <dt>

[**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

Recibe notificaciones sobre los cambios de estado del canal o los datos recibidos.

</dd> <dt>

[**IWTSVirtualChannelCallback2**](iwtsvirtualchannelcallback2.md)
</dt> <dd>

Esta interfaz no se admite.

</dd> <dt>

[**VirtualChannelGetInstance**](virtualchannelgetinstance.md)
</dt> <dd>

Se llama para que el complemento cree una instancia de la interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos los complementos implementados por el archivo DLL.

</dd> </dl>

 

 




