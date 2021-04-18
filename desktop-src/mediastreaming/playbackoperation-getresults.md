---
title: PlaybackOperation. GetResults, método
description: Devuelve los resultados de una operación asincrónica iniciada por uno de los métodos de reproducción de MediaRenderer.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- Método GetResults API de streaming de multimedia
- Método GetResults API de streaming multimedia, interfaz PlaybackOperation
- PlaybackOperation interface media streaming API, GetResults (método)
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f146876966cc4e003bd88ad295c9938e5240abfe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419307"
---
# <a name="playbackoperationgetresults-method"></a><span data-ttu-id="2c704-106">PlaybackOperation. GetResults, método</span><span class="sxs-lookup"><span data-stu-id="2c704-106">PlaybackOperation.GetResults method</span></span>

<span data-ttu-id="2c704-107">Devuelve los resultados de una operación asincrónica iniciada por uno de los métodos de reproducción de [**MediaRenderer**](mediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="2c704-107">Returns the results of an asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c704-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c704-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="2c704-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c704-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c704-110">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2c704-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2c704-111">Resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2c704-111">The result of the operation.</span></span> <span data-ttu-id="2c704-112">Un valor de 0 indica que la operación se completó.</span><span class="sxs-lookup"><span data-stu-id="2c704-112">A value of 0 indicates that the operation completed.</span></span> <span data-ttu-id="2c704-113">Otros valores están reservados.</span><span class="sxs-lookup"><span data-stu-id="2c704-113">Other values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c704-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c704-114">Return value</span></span>

<span data-ttu-id="2c704-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2c704-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2c704-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="2c704-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2c704-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2c704-117">Return code</span></span>                                                                          | <span data-ttu-id="2c704-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c704-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2c704-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2c704-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2c704-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="2c704-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c704-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c704-121">Remarks</span></span>

<span data-ttu-id="2c704-122">Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la propiedad [**completed**](playbackoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="2c704-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](playbackoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c704-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c704-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c704-124">**PlaybackOperation**</span><span class="sxs-lookup"><span data-stu-id="2c704-124">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 





