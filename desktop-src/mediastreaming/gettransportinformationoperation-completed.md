---
title: Propiedad GetTransportInformationOperation Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por GetTransportInformationAsync.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- Propiedad completada API de streaming de multimedia
- Propiedad completada API de streaming multimedia, interfaz GetTransportInformationOperation
- Interfaz GetTransportInformationOperation API de streaming de multimedia, propiedad Completed
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2948af2ed84a70c9f37efbc4aae985e9b1ab5804
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704947"
---
# <a name="gettransportinformationoperationcompleted-property"></a><span data-ttu-id="e8012-106">GetTransportInformationOperation:: Completed (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e8012-106">GetTransportInformationOperation::Completed property</span></span>

<span data-ttu-id="e8012-107">Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) .</span><span class="sxs-lookup"><span data-stu-id="e8012-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) is completed.</span></span>

<span data-ttu-id="e8012-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e8012-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8012-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8012-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="e8012-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8012-110">Property value</span></span>

<span data-ttu-id="e8012-111">Controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="e8012-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8012-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8012-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8012-113">**GetTransportInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="e8012-113">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

 