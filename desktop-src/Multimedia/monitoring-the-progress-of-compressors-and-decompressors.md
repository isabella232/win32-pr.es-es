---
title: Supervisar el progreso de los compresores y descompresores
description: Supervisar el progreso de los compresores y descompresores
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- Administrador de compresión de vídeo (VCM), supervisión
- VCM (Administrador de compresión de vídeo), supervisar
- ICSetStatusProc función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ef5449e8d4e985217ee60f075d22b16dcc5c3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685556"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a><span data-ttu-id="513f7-106">Supervisar el progreso de los compresores y descompresores</span><span class="sxs-lookup"><span data-stu-id="513f7-106">Monitoring the Progress of Compressors and Decompressors</span></span>

<span data-ttu-id="513f7-107">La aplicación puede supervisar el progreso de una operación larga realizada por un compresor o descompresor enviándole la dirección de una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="513f7-107">Your application can monitor the progress of a lengthy operation performed by a compressor or decompressor by sending it the address of a callback function.</span></span> <span data-ttu-id="513f7-108">Puede usar la función [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) para enviar la dirección al compresor o descompresor.</span><span class="sxs-lookup"><span data-stu-id="513f7-108">You can use the [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) function to send the address to the compressor or decompressor.</span></span> <span data-ttu-id="513f7-109">Cuando el compresor o el descompresor reciben esta dirección, envía mensajes de estado a la función.</span><span class="sxs-lookup"><span data-stu-id="513f7-109">When the compressor or decompressor receives this address, it sends status messages to the function.</span></span> <span data-ttu-id="513f7-110">Estos mensajes indican si la operación se inicia, se detiene, se produce o se continúa.</span><span class="sxs-lookup"><span data-stu-id="513f7-110">These messages indicate whether the operation is starting, stopping, yielding, or proceeding.</span></span>

 

 




