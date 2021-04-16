---
title: Propiedad PlaybackOperation. Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por uno de los métodos de reproducción de MediaRenderer.
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- Propiedad completada API de streaming de multimedia
- Propiedad completada API de streaming multimedia, interfaz PlaybackOperation
- Interfaz PlaybackOperation API de streaming de multimedia, propiedad Completed
topic_type:
- apiref
api_name:
- PlaybackOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf305b4028e223c36df0c8a59c5246228c5b8d40
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105714285"
---
# <a name="playbackoperationcompleted-property"></a><span data-ttu-id="96be9-106">Propiedad PlaybackOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="96be9-106">PlaybackOperation.Completed property</span></span>

<span data-ttu-id="96be9-107">Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por uno de los métodos de reproducción de [**MediaRenderer**](mediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="96be9-107">Gets or sets an event handler that is invoked when the asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods is completed.</span></span>

<span data-ttu-id="96be9-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="96be9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="96be9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96be9-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="96be9-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="96be9-110">Property value</span></span>

<span data-ttu-id="96be9-111">Controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="96be9-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="96be9-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="96be9-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96be9-113">**PlaybackOperation**</span><span class="sxs-lookup"><span data-stu-id="96be9-113">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 




