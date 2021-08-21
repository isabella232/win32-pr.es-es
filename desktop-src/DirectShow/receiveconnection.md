---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a8a91cbf9870d6c53592ff823f710eb5875fa939592309425df0a0bca6f0e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072769"
---
# <a name="receiveconnection"></a>ReceiveConnection

Este mecanismo permite que un pin de salida proponga un cambio de formato en su elemento del mismo nivel de bajada, cuando el nuevo formato requiere un búfer mayor. El pin de salida hace lo siguiente:

1.  Llama [**a IPin::ReceiveConnection en**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) el pin de entrada de bajada.
2.  Si `ReceiveConnection` se realiza correctamente, llama [**a IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) en el pin de entrada.

Además, es posible que el pin de salida tenga que llamar a [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) y, a continuación, desasignar y volver a confirmar el asignador para cambiar los tamaños de búfer. Asegúrese de entregar todos los ejemplos pendientes en el formato anterior antes de cambiar el tamaño del búfer.

Algunos descodificadores MPEG-2 usan este mecanismo para cambiar entre la salida MPEG-1 y MPEG-2 o si cambia el tamaño del vídeo.

 

 



