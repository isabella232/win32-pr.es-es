---
title: Escribir datos mediante un canal de DVC
description: Escritorio remoto la escritura de datos del canal mediante el uso de un canal virtual dinámico (DVC) es simétrica tanto para el servidor host de sesión de escritorio remoto (host de sesión de RD) como para el cliente.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd6f26e926958ceba5418a72849b75a66b11d2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685564"
---
# <a name="writing-data-by-using-a-dvc-channel"></a>Escribir datos mediante un canal de DVC

Escritorio remoto la escritura de datos del canal mediante el uso de un canal virtual dinámico (DVC) es simétrica tanto para el servidor host de sesión de escritorio remoto (host de sesión de RD) como para el cliente. La escritura de datos del canal se implementa mediante el método [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) de la interfaz [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) .

En la ilustración siguiente se muestra el envío y la recepción del paquete de datos entre el cliente y el servidor DVC (complemento DVC).

![envío y recepción de un paquete de datos entre el cliente y el servidor de DVC](images/writedvcchannel.png)

 

 




