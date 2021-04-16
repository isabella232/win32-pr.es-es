---
title: StreamSelectOperation. GetResults, método
description: Devuelve los resultados de la operación asincrónica iniciada por SelectBestStreamAsync.
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- Método GetResults API de streaming de multimedia
- Método GetResults API de streaming multimedia, interfaz StreamSelectOperation
- StreamSelectOperation interface media streaming API, GetResults (método)
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c52479949413d32ca54654f355a06a2dee70866e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714363"
---
# <a name="streamselectoperationgetresults-method"></a><span data-ttu-id="36826-106">StreamSelectOperation. GetResults, método</span><span class="sxs-lookup"><span data-stu-id="36826-106">StreamSelectOperation.GetResults method</span></span>

<span data-ttu-id="36826-107">Devuelve los resultados de la operación asincrónica iniciada por [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="36826-107">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="36826-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36826-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="36826-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36826-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36826-110">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="36826-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="36826-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="36826-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="36826-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36826-112">Return value</span></span>

<span data-ttu-id="36826-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="36826-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="36826-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="36826-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="36826-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="36826-115">Return code</span></span>                                                                          | <span data-ttu-id="36826-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="36826-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="36826-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="36826-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="36826-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="36826-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="36826-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="36826-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36826-120">**StreamSelectOperation**</span><span class="sxs-lookup"><span data-stu-id="36826-120">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

