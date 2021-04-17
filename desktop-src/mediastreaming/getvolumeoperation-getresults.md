---
title: GetVolumeOperation. GetResults, método
description: Devuelve los resultados de la operación asincrónica iniciada por GetVolumeAsync.
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- Método GetResults API de streaming de multimedia
- Método GetResults API de streaming multimedia, interfaz GetVolumeOperation
- GetVolumeOperation interface media streaming API, GetResults (método)
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 444eaf590e5afc5d4f5185bcd3793698d6fe4535
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704955"
---
# <a name="getvolumeoperationgetresults-method"></a><span data-ttu-id="f13b9-106">GetVolumeOperation. GetResults, método</span><span class="sxs-lookup"><span data-stu-id="f13b9-106">GetVolumeOperation.GetResults method</span></span>

<span data-ttu-id="f13b9-107">Devuelve los resultados de la operación asincrónica iniciada por [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span><span class="sxs-lookup"><span data-stu-id="f13b9-107">Returns the results of the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="f13b9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f13b9-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="f13b9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f13b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f13b9-110">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f13b9-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f13b9-111">Volumen.</span><span class="sxs-lookup"><span data-stu-id="f13b9-111">The volume.</span></span> <span data-ttu-id="f13b9-112">Un valor comprendido entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="f13b9-112">A value between 0 and 100.</span></span> <span data-ttu-id="f13b9-113">0 indica el volumen mínimo y 100 indica el volumen máximo.</span><span class="sxs-lookup"><span data-stu-id="f13b9-113">0 indicates minimum volume, and 100 indicates maximum volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f13b9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f13b9-114">Return value</span></span>

<span data-ttu-id="f13b9-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f13b9-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f13b9-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="f13b9-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f13b9-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f13b9-117">Return code</span></span>                                                                          | <span data-ttu-id="f13b9-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f13b9-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f13b9-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f13b9-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f13b9-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="f13b9-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f13b9-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f13b9-121">Remarks</span></span>

<span data-ttu-id="f13b9-122">Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la propiedad [**completed**](getvolumeoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="f13b9-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getvolumeoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="f13b9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f13b9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f13b9-124">**GetVolumeOperation**</span><span class="sxs-lookup"><span data-stu-id="f13b9-124">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

