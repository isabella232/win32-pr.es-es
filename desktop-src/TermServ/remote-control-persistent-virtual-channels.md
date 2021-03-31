---
title: Canales virtuales persistentes de control remoto
description: Un canal virtual persistente de control remoto no se cierra cuando un control remoto se conecta o se desconecta para la sesión conectada al cliente. Los datos se seguirán transmitiendo y recibiendo a través de este canal.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419087"
---
# <a name="remote-control-persistent-virtual-channels"></a>Canales virtuales persistentes de control remoto

En Windows XP, un archivo DLL puede especificar uno o más canales virtuales como *persistentes para el control remoto*. Un canal virtual persistente de control remoto no se cierra cuando un control remoto se conecta o se desconecta para la sesión conectada al cliente. Los datos se seguirán transmitiendo y recibiendo a través de este canal. Los canales virtuales que el archivo DLL no especifica como control remoto persistente se cerrarán en este escenario.

Los canales virtuales persistentes del control remoto se especifican durante la llamada a **VirtualChannelInit**. Consulte la página de referencia de [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) para obtener información específica sobre este.

 

 




