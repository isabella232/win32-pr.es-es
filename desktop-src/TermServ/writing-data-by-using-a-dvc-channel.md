---
title: Escribir datos mediante un canal DVC
description: Escribir datos de canal mediante un canal virtual dinámico (DVC) es simétrico tanto para el servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto) como para el cliente.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e3f73b8e7a3d7db8ac109e84c9c638845af441b58568156782710fdac0968a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058253"
---
# <a name="writing-data-by-using-a-dvc-channel"></a>Escribir datos mediante un canal DVC

Escribir datos de canal mediante un canal virtual dinámico (DVC) es simétrico tanto para el servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto) como para el cliente. El método [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) de la [**interfaz IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) implementa la escritura de datos de canal.

En la ilustración siguiente se muestra el envío y la recepción del paquete de datos entre el cliente y el servidor de DVC (complemento DVC).

![enviar y recibir un paquete de datos entre el cliente y el servidor dvc](images/writedvcchannel.png)

 

 




