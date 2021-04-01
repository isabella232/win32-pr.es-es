---
description: Los monitores reciben tramas de red capturadas en modo en tiempo real. Los fotogramas se capturan mediante un proveedor de paquetes de red (NPP) mediante la interfaz COM Providers IRTC y se pasan al monitor en uno de los monitores dos subprocesos de ejecución.
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Real-Time capturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913650"
---
# <a name="real-time-captures"></a>Real-Time capturas

Los monitores reciben tramas de red capturadas en modo en tiempo real. Los fotogramas se capturan mediante un [*proveedor de paquetes de red*](n.md) (NPP) mediante la interfaz com [IRTC](irtc.md) del proveedor y se pasan al monitor en uno de los dos subprocesos de ejecución del monitor.

Los monitores pueden limitar el número de fotogramas que se deben procesar pasando un [*filtro de captura*](c.md) al NPP que suministra los fotogramas. Normalmente, un monitor específico está diseñado para ver tipos específicos de tráfico, como HTTP, RIPX o SMB. A diferencia de los expertos, que usan analizadores sofisticados para seleccionar la información que se va a analizar, un monitor debe examinar cada fotograma en busca de las condiciones que se diseñaron para detectar. El motivo que subyace a este enfoque marco a fotograma es el rendimiento. Un monitor debe procesar sus fotogramas lo suficientemente rápido como para que no quede detrás del controlador que proporciona los fotogramas al NPP. De lo contrario, se perderán los datos.

 

 



