---
title: API de cliente de DVC
description: Las API de cliente de canal virtual dinámico (DVC) se implementan específicamente para el cliente de Conexión a Escritorio remoto (RDC) de la conexión.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356974"
---
# <a name="dvc-client-apis"></a>API de cliente de DVC

Las API de cliente de canal virtual dinámico (DVC) se implementan específicamente para el cliente de Conexión a Escritorio remoto (RDC) de la conexión. Algunas de las API se implementan mediante el marco de DVC y otras las implementa el desarrollador del complemento. Algunas de las API se utilizan para admitir el complemento de cliente de Conexión a Escritorio remoto (RDC) y no están directamente relacionadas con el transporte de datos.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

Permite que el cliente de Conexión a Escritorio remoto (RDC) cargue el complemento de cliente de Conexión a Escritorio remoto (RDC).

</dd> <dt>

[**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

Administra los valores de configuración para cada agente de escucha para la conexión de canal virtual dinámico (DVC).

</dd> <dt>

[**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

Se usa para notificar al complemento de cliente de Conexión a Escritorio remoto (RDC) acerca de las solicitudes entrantes en un agente de escucha determinado.

</dd> <dt>

[**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

Administra todos los complementos de cliente de Conexión a Escritorio remoto (RDC) y los agentes de escucha del canal virtual dinámico (DVC).

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

No se admite esta interfaz.

</dd> <dt>

[**VirtualChannelGetInstance**](virtualchannelgetinstance.md)
</dt> <dd>

Se llama para que el complemento cree una instancia de la interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos los complementos implementados por el archivo dll.

</dd> </dl>

 

 




