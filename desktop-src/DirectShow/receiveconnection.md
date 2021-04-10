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
# <a name="receiveconnection"></a><span data-ttu-id="36910-103">ReceiveConnection</span><span class="sxs-lookup"><span data-stu-id="36910-103">ReceiveConnection</span></span>

<span data-ttu-id="36910-104">Este mecanismo permite a un PIN de salida proponer un cambio de formato a su elemento de nivel inferior, cuando el nuevo formato requiere un búfer mayor.</span><span class="sxs-lookup"><span data-stu-id="36910-104">This mechanism enables an output pin to propose a format change to its downstream peer, when the new format requires a larger buffer.</span></span> <span data-ttu-id="36910-105">El PIN de salida hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="36910-105">The output pin does the following:</span></span>

1.  <span data-ttu-id="36910-106">Llama a [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) en el PIN de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="36910-106">Calls [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the downstream input pin.</span></span>
2.  <span data-ttu-id="36910-107">Si se `ReceiveConnection` realiza correctamente, llama a [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="36910-107">If `ReceiveConnection` succeeds, calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) on the input pin.</span></span>

<span data-ttu-id="36910-108">Además, el PIN de salida puede tener que llamar a [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) y, después, anular la confirmación y volver a confirmar el asignador para cambiar los tamaños de búfer.</span><span class="sxs-lookup"><span data-stu-id="36910-108">In addition, the output pin may need to call [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) and then decommit and recommit the allocator in order to change buffer sizes.</span></span> <span data-ttu-id="36910-109">Asegúrese de proporcionar todos los ejemplos pendientes en el formato anterior antes de cambiar el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="36910-109">Make sure to deliver all pending samples in the old format before changing the buffer size.</span></span>

<span data-ttu-id="36910-110">Algunos descodificadores MPEG-2 usan este mecanismo para cambiar entre los resultados MPEG-1 y MPEG-2, o si el tamaño del vídeo cambia.</span><span class="sxs-lookup"><span data-stu-id="36910-110">Some MPEG-2 decoders use this mechanism to switch between MPEG-1 and MPEG-2 output or if the video size changes.</span></span>

 

 



