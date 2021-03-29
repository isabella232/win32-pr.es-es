---
title: Propiedad CreateMediaRendererOperation. Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por CreateMediaRendererAsync o CreateMediaRendererFromBasicDeviceAsync.
ms.assetid: B62CF929-13D0-4665-89E4-DEC48A38DDF7
keywords:
- Propiedad completada API de streaming de multimedia
- Propiedad completada API de streaming multimedia, interfaz CreateMediaRendererOperation
- Interfaz CreateMediaRendererOperation API de streaming de multimedia, propiedad Completed
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3b4ebafc1441741a352f4573709495228bf13e4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783953"
---
# <a name="createmediarendereroperationcompleted-property"></a><span data-ttu-id="5bb74-106">Propiedad CreateMediaRendererOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="5bb74-106">CreateMediaRendererOperation.Completed property</span></span>

<span data-ttu-id="5bb74-107">Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) o [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) .</span><span class="sxs-lookup"><span data-stu-id="5bb74-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) or [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) is completed.</span></span>

<span data-ttu-id="5bb74-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5bb74-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb74-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bb74-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a><span data-ttu-id="5bb74-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5bb74-110">Property value</span></span>

<span data-ttu-id="5bb74-111">Controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="5bb74-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bb74-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bb74-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb74-113">**CreateMediaRendererOperation**</span><span class="sxs-lookup"><span data-stu-id="5bb74-113">**CreateMediaRendererOperation**</span></span>](createmediarendereroperation.md)
</dt> </dl>

 

 




