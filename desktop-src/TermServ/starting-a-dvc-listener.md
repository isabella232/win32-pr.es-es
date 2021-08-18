---
title: Inicio de un agente de escucha dvc
description: Para establecer una conexión correcta entre dos módulos de canal virtual dinámico (DVC) que se ejecutan en el cliente y el servidor de Conexión a Escritorio remoto (RDC), un agente de escucha DVC debe estar en ejecución y en estado de escucha.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d440069cb64597c16a14323a67926376bf1c425f5a29c77e451c52866a5399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000455"
---
# <a name="starting-a-dvc-listener"></a>Inicio de un agente de escucha dvc

Para establecer una conexión correcta entre dos módulos de canal virtual dinámico (DVC) que se ejecutan en el cliente y el servidor de Conexión a Escritorio remoto (RDC), un agente de escucha DVC debe estar en ejecución y en estado de escucha.

La creación de instancias de un agente de escucha suele producirse en el [**método Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) del complemento DVC. Sin embargo, la creación de instancias no se limita al **método Initialize** y se puede iniciar en cualquier punto de la ejecución del complemento. La interfaz [**IWTSListener,**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) a la que se crea una instancia de [**IWTSVirtualChannelManager,**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)describe el agente de escucha. Una instancia del administrador de canales se pasa al complemento en el punto de inicialización. El complemento puede mantener una referencia interna a la instancia siempre que sea necesario.

Un complemento puede crear instancias de tantos agentes de escucha como sea necesario. [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)controlará cualquier conexión entrante, que se proporciona en el [**método CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) de [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager). Para obtener un ejemplo, vea la implementación de **CDVCSamplePlugin::Initialize** en el código de ejemplo del complemento de cliente [DVC.](dvc-client-plug-in-example.md)

 

 




