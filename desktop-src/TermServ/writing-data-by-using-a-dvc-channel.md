---
title: Escribir datos mediante un canal DVC
description: Escribir datos de canal mediante un canal virtual dinámico (DVC) es simétrico tanto para el servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto) como para el cliente.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd6f26e926958ceba5418a72849b75a66b11d2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071016"
---
# <a name="writing-data-by-using-a-dvc-channel"></a>Escribir datos mediante un canal DVC

Escribir datos de canal mediante un canal virtual dinámico (DVC) es simétrico tanto para el servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto) como para el cliente. El método [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) de la [**interfaz IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) implementa la escritura de datos de canal.

En la ilustración siguiente se muestra el envío y la recepción del paquete de datos entre el cliente y el servidor de DVC (complemento DVC).

![enviar y recibir un paquete de datos entre el cliente y el servidor dvc](images/writedvcchannel.png)

 

 




