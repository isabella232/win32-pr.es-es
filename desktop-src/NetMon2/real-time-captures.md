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
# <a name="real-time-captures"></a><span data-ttu-id="2c778-104">Real-Time capturas</span><span class="sxs-lookup"><span data-stu-id="2c778-104">Real-Time Captures</span></span>

<span data-ttu-id="2c778-105">Los monitores reciben tramas de red capturadas en modo en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="2c778-105">Monitors receive captured network frames in real-time mode.</span></span> <span data-ttu-id="2c778-106">Los fotogramas se capturan mediante un [*proveedor de paquetes de red*](n.md) (NPP) mediante la interfaz com [IRTC](irtc.md) del proveedor y se pasan al monitor en uno de los dos subprocesos de ejecución del monitor.</span><span class="sxs-lookup"><span data-stu-id="2c778-106">The frames are captured by a [*network packet provider*](n.md) (NPP) using the provider's [IRTC](irtc.md) COM interface, and passed on to the monitor in one of the monitor's two execution threads.</span></span>

<span data-ttu-id="2c778-107">Los monitores pueden limitar el número de fotogramas que se deben procesar pasando un [*filtro de captura*](c.md) al NPP que suministra los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2c778-107">Monitors can limit the number of frames they have to process by passing a [*capture filter*](c.md) to the NPP that is supplying the frames.</span></span> <span data-ttu-id="2c778-108">Normalmente, un monitor específico está diseñado para ver tipos específicos de tráfico, como HTTP, RIPX o SMB.</span><span class="sxs-lookup"><span data-stu-id="2c778-108">Typically, a specific monitor is designed to watch for specific types of traffic, such as HTTP, RIPX, or SMB.</span></span> <span data-ttu-id="2c778-109">A diferencia de los expertos, que usan analizadores sofisticados para seleccionar la información que se va a analizar, un monitor debe examinar cada fotograma en busca de las condiciones que se diseñaron para detectar.</span><span class="sxs-lookup"><span data-stu-id="2c778-109">Unlike experts, which use sophisticated parsers to select the information to be analyzed, a monitor must examine each frame for the conditions it was designed to detect.</span></span> <span data-ttu-id="2c778-110">El motivo que subyace a este enfoque marco a fotograma es el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2c778-110">The reason behind this frame-by-frame approach is performance.</span></span> <span data-ttu-id="2c778-111">Un monitor debe procesar sus fotogramas lo suficientemente rápido como para que no quede detrás del controlador que proporciona los fotogramas al NPP.</span><span class="sxs-lookup"><span data-stu-id="2c778-111">A monitor must process its frames quickly enough so that it does not fall behind the driver supplying the frames to the NPP.</span></span> <span data-ttu-id="2c778-112">De lo contrario, se perderán los datos.</span><span class="sxs-lookup"><span data-stu-id="2c778-112">Otherwise, data will be lost.</span></span>

 

 



