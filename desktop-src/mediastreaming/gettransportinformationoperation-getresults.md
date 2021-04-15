---
title: GetTransportInformationOperation GetResults (método)
description: Devuelve los resultados de la operación asincrónica iniciada por GetTransportInformationAsync.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- Método GetResults API de streaming de multimedia
- Método GetResults API de streaming multimedia, interfaz GetTransportInformationOperation
- GetTransportInformationOperation interface media streaming API, GetResults (método)
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f846a5824ed07bcaf849a540429eaabe46f3d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420657"
---
# <a name="gettransportinformationoperationgetresults-method"></a><span data-ttu-id="3f79a-106">GetTransportInformationOperation:: GetResults (método)</span><span class="sxs-lookup"><span data-stu-id="3f79a-106">GetTransportInformationOperation::GetResults method</span></span>

<span data-ttu-id="3f79a-107">Devuelve los resultados de la operación asincrónica iniciada por [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span><span class="sxs-lookup"><span data-stu-id="3f79a-107">Returns the results of the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="3f79a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f79a-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="3f79a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f79a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f79a-110">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3f79a-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3f79a-111">Referencia a una estructura [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) que contiene los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="3f79a-111">A reference to a [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f79a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f79a-112">Return value</span></span>

<span data-ttu-id="3f79a-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3f79a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3f79a-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="3f79a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3f79a-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3f79a-115">Return code</span></span>                                                                          | <span data-ttu-id="3f79a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f79a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3f79a-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3f79a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3f79a-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="3f79a-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3f79a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f79a-119">Remarks</span></span>

<span data-ttu-id="3f79a-120">Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la propiedad [**completed**](gettransportinformationoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="3f79a-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](gettransportinformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f79a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f79a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f79a-122">**GetTransportInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="3f79a-122">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

