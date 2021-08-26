---
title: Canales virtuales persistentes de control remoto
description: Un canal virtual persistente de control remoto no se cierra cuando un control remoto se conecta o se desconecta para la sesión conectada al cliente. Los datos se seguirán transmitiendo y recibiendo a través de este canal.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71206b8272fb516da9a3c39bed7f7d54edbc5227958d975bf11b114db9c13869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988785"
---
# <a name="remote-control-persistent-virtual-channels"></a>Canales virtuales persistentes de control remoto

En Windows XP, un archivo DLL puede especificar uno o varios canales virtuales como *persistente de control remoto.* Un canal virtual persistente de control remoto no se cierra cuando un control remoto se conecta o se desconecta para la sesión conectada al cliente. Los datos se seguirán transmitiendo y recibiendo a través de este canal. Los canales virtuales que el archivo DLL no especifica como persistente de control remoto se cerrarán en este escenario.

Los canales virtuales persistentes de control remoto se especifican durante la llamada a **VirtualChannelInit.** Consulte la página de referencia de [**VirtualChannelInit para**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) obtener información específica al respecto.

 

 




