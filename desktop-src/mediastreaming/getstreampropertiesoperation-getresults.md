---
title: GetStreamPropertiesOperation. GetResults, método
description: Devuelve los resultados de la operación asincrónica iniciada por GetStreamPropertiesAsync.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- Método GetResults API de streaming de multimedia
- Método GetResults API de streaming multimedia, interfaz GetStreamPropertiesOperation
- GetStreamPropertiesOperation interface media streaming API, GetResults (método)
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 312703c28f5cdbb888b46d6ccd312dd358aa6b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420632"
---
# <a name="getstreampropertiesoperationgetresults-method"></a><span data-ttu-id="1db0f-106">GetStreamPropertiesOperation. GetResults, método</span><span class="sxs-lookup"><span data-stu-id="1db0f-106">GetStreamPropertiesOperation.GetResults method</span></span>

<span data-ttu-id="1db0f-107">Devuelve los resultados de la operación asincrónica iniciada por [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1db0f-107">Returns the results of the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="1db0f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1db0f-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="1db0f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1db0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1db0f-110">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1db0f-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="1db0f-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1db0f-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="1db0f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1db0f-112">Return value</span></span>

<span data-ttu-id="1db0f-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1db0f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1db0f-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="1db0f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1db0f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1db0f-115">Return code</span></span>                                                                          | <span data-ttu-id="1db0f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1db0f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1db0f-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1db0f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1db0f-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="1db0f-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1db0f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="1db0f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1db0f-120">**GetStreamPropertiesOperation**</span><span class="sxs-lookup"><span data-stu-id="1db0f-120">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

