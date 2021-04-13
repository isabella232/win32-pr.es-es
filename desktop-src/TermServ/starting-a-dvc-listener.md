---
title: Inicio de un agente de escucha de DVC
description: Para establecer una conexión correcta entre dos módulos de canal virtual dinámico (DVC) que se ejecutan en el cliente y servidor de Conexión a Escritorio remoto (RDC), un agente de escucha de DVC debe estar en ejecución y en un estado de escucha.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b625d5547facd0487af170af9d59eddd6bfed87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357700"
---
# <a name="starting-a-dvc-listener"></a>Inicio de un agente de escucha de DVC

Para establecer una conexión correcta entre dos módulos de canal virtual dinámico (DVC) que se ejecutan en el cliente y servidor de Conexión a Escritorio remoto (RDC), un agente de escucha de DVC debe estar en ejecución y en un estado de escucha.

La creación de instancias de un agente de escucha suele producirse en el método [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) del complemento DVC. Sin embargo, la creación de instancias no se limita al método **Initialize** y se puede iniciar en cualquier punto de la ejecución del complemento. El agente de escucha se describe mediante la interfaz [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) con la que se crea una instancia de [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager). Una instancia del administrador de canales se pasa al complemento en el punto de inicialización. El complemento puede mantener una referencia interna a la instancia siempre que sea necesario.

Un complemento puede crear instancias de todos los agentes de escucha que necesite. Las conexiones entrantes se controlarán mediante [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), que se proporciona en el método [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) de [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager). Para obtener un ejemplo, vea la implementación de **CDVCSamplePlugin:: Initialize** en el ejemplo de código de [ejemplo del complemento de cliente de DVC](dvc-client-plug-in-example.md) .

 

 




