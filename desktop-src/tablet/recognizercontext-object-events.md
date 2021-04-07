---
description: En la tabla siguiente se describen los subprocesos en los que se pueden activar los eventos del objeto RecognizerContext. EventThreadsRecognitionFires en el subproceso de reconocimiento en segundo plano o en el subproceso que llama al método Recognize del objeto RecognizerContext. RecognitionWithAlternatesFires en el subproceso de reconocimiento en segundo plano.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Eventos de objeto RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002498"
---
# <a name="recognizercontext-object-events"></a><span data-ttu-id="ef15a-103">Eventos de objeto RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="ef15a-103">RecognizerContext Object Events</span></span>

<span data-ttu-id="ef15a-104">En la tabla siguiente se describen los subprocesos en los que se pueden activar los eventos del objeto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="ef15a-104">The following table describes which threads the [**RecognizerContext**](inkrecognizercontext-class.md) object events can fire on.</span></span>



| <span data-ttu-id="ef15a-105">Evento</span><span class="sxs-lookup"><span data-stu-id="ef15a-105">Event</span></span>                                                                               | <span data-ttu-id="ef15a-106">Subprocesos</span><span class="sxs-lookup"><span data-stu-id="ef15a-106">Threads</span></span>                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef15a-107">**Reconocimiento**</span><span class="sxs-lookup"><span data-stu-id="ef15a-107">**Recognition**</span></span>](inkrecognizercontext-recognition.md)                             | <span data-ttu-id="ef15a-108">Se desencadena en el subproceso de reconocimiento en segundo plano o en el subproceso que llama al método [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="ef15a-108">Fires on the background recognition thread, or on the thread which calls the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method.</span></span><br/> |
| [<span data-ttu-id="ef15a-109">**RecognitionWithAlternates**</span><span class="sxs-lookup"><span data-stu-id="ef15a-109">**RecognitionWithAlternates**</span></span>](inkrecognizercontext-recognitionwithalternates.md) | <span data-ttu-id="ef15a-110">Se desencadena en el subproceso de reconocimiento en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ef15a-110">Fires on the background recognition thread.</span></span><br/>                                                                                                                                                               |



 

 

 




