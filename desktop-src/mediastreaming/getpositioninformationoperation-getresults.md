---
title: GetPositionInformationOperation. GetResults, método
description: Devuelve los resultados de la operación asincrónica iniciada por GetPositionInformationAsync.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- Método GetResults API de streaming de multimedia
- Método GetResults API de streaming multimedia, interfaz GetPositionInformationOperation
- GetPositionInformationOperation interface media streaming API, GetResults (método)
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a0b4311c3be814a73ddb1e2a9b18d8e19aea9ee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791218"
---
# <a name="getpositioninformationoperationgetresults-method"></a><span data-ttu-id="dc7fe-106">GetPositionInformationOperation. GetResults, método</span><span class="sxs-lookup"><span data-stu-id="dc7fe-106">GetPositionInformationOperation.GetResults method</span></span>

<span data-ttu-id="dc7fe-107">Devuelve los resultados de la operación asincrónica iniciada por [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span><span class="sxs-lookup"><span data-stu-id="dc7fe-107">Returns the results of the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc7fe-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc7fe-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="dc7fe-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc7fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc7fe-110">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="dc7fe-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7fe-111">Referencia a una estructura [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) que contiene los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="dc7fe-111">A reference to a [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc7fe-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc7fe-112">Return value</span></span>

<span data-ttu-id="dc7fe-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dc7fe-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dc7fe-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="dc7fe-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dc7fe-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dc7fe-115">Return code</span></span>                                                                          | <span data-ttu-id="dc7fe-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc7fe-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="dc7fe-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="dc7fe-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dc7fe-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="dc7fe-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc7fe-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc7fe-119">Remarks</span></span>

<span data-ttu-id="dc7fe-120">Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la propiedad [**completed**](getpositioninformationoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="dc7fe-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getpositioninformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc7fe-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc7fe-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc7fe-122">**GetPositionInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="dc7fe-122">**GetPositionInformationOperation**</span></span>](getpositioninformationoperation.md)
</dt> </dl>

 

