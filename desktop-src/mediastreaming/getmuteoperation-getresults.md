---
title: GetMuteOperation. GetResults, método
description: Devuelve los resultados de la operación asincrónica iniciada por GetMuteAsync.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- Método GetResults API de streaming de multimedia
- Método GetResults API de streaming multimedia, interfaz GetMuteOperation
- GetMuteOperation interface media streaming API, GetResults (método)
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149210"
---
# <a name="getmuteoperationgetresults-method"></a><span data-ttu-id="60ca4-106">GetMuteOperation. GetResults, método</span><span class="sxs-lookup"><span data-stu-id="60ca4-106">GetMuteOperation.GetResults method</span></span>

<span data-ttu-id="60ca4-107">Devuelve los resultados de la operación asincrónica iniciada por [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span><span class="sxs-lookup"><span data-stu-id="60ca4-107">Returns the results of the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="60ca4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60ca4-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="60ca4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60ca4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ca4-110">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="60ca4-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="60ca4-111">Valor de silencio.</span><span class="sxs-lookup"><span data-stu-id="60ca4-111">The mute value.</span></span> <span data-ttu-id="60ca4-112">Un valor de True indica que el audio está silenciado actualmente.</span><span class="sxs-lookup"><span data-stu-id="60ca4-112">A value of true indicates that audio is currently muted.</span></span> <span data-ttu-id="60ca4-113">Un valor de False indica que el audio no está silenciado.</span><span class="sxs-lookup"><span data-stu-id="60ca4-113">A value of false indicates that audio is not muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ca4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60ca4-114">Return value</span></span>

<span data-ttu-id="60ca4-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="60ca4-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="60ca4-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="60ca4-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="60ca4-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="60ca4-117">Return code</span></span>                                                                          | <span data-ttu-id="60ca4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="60ca4-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="60ca4-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="60ca4-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="60ca4-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="60ca4-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60ca4-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60ca4-121">Remarks</span></span>

<span data-ttu-id="60ca4-122">Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la propiedad [**completed**](getmuteoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="60ca4-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getmuteoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="60ca4-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="60ca4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ca4-124">**GetMuteOperation**</span><span class="sxs-lookup"><span data-stu-id="60ca4-124">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

