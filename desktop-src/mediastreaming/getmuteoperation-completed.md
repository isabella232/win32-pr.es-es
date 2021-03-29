---
title: Propiedad GetMuteOperation. Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por GetMuteAsync.
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- Propiedad completada API de streaming de multimedia
- Propiedad completada API de streaming multimedia, interfaz GetMuteOperation
- Interfaz GetMuteOperation API de streaming de multimedia, propiedad Completed
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40c360dc3597d8cf04d1a8c505e479a38136f592
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791085"
---
# <a name="getmuteoperationcompleted-property"></a><span data-ttu-id="501e6-106">Propiedad GetMuteOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="501e6-106">GetMuteOperation.Completed property</span></span>

<span data-ttu-id="501e6-107">Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) .</span><span class="sxs-lookup"><span data-stu-id="501e6-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) is completed.</span></span>

<span data-ttu-id="501e6-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="501e6-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="501e6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="501e6-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="501e6-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="501e6-110">Property value</span></span>

<span data-ttu-id="501e6-111">Controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="501e6-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="501e6-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="501e6-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="501e6-113">**GetMuteOperation**</span><span class="sxs-lookup"><span data-stu-id="501e6-113">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

 