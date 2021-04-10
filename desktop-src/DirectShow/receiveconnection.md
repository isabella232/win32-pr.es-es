---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fd9fe31f87a34dc3bfdfc4ecfb532255138b9c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152386"
---
# <a name="receiveconnection"></a>ReceiveConnection

Este mecanismo permite a un PIN de salida proponer un cambio de formato a su elemento de nivel inferior, cuando el nuevo formato requiere un búfer mayor. El PIN de salida hace lo siguiente:

1.  Llama a [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) en el PIN de entrada de nivel inferior.
2.  Si se `ReceiveConnection` realiza correctamente, llama a [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) en el PIN de entrada.

Además, el PIN de salida puede tener que llamar a [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) y, después, anular la confirmación y volver a confirmar el asignador para cambiar los tamaños de búfer. Asegúrese de proporcionar todos los ejemplos pendientes en el formato anterior antes de cambiar el tamaño del búfer.

Algunos descodificadores MPEG-2 usan este mecanismo para cambiar entre los resultados MPEG-1 y MPEG-2, o si el tamaño del vídeo cambia.

 

 



