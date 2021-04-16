---
description: Establece el ejemplo para el origen de la secuencia de medios.
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: 'IMFMediaStreamSourceSampleRequest:: SetSample (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: bc3b2693a4690207f0b39d7f1b846e1e63069a8c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670077"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a><span data-ttu-id="9566c-103">IMFMediaStreamSourceSampleRequest:: SetSample (método)</span><span class="sxs-lookup"><span data-stu-id="9566c-103">IMFMediaStreamSourceSampleRequest::SetSample method</span></span>

<span data-ttu-id="9566c-104">Establece el ejemplo para el origen de la secuencia de medios.</span><span class="sxs-lookup"><span data-stu-id="9566c-104">Sets the sample for the media stream source.</span></span>

## <a name="syntax"></a><span data-ttu-id="9566c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9566c-105">Syntax</span></span>


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a><span data-ttu-id="9566c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9566c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9566c-107">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9566c-107">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9566c-108">El ejemplo del origen del flujo de medios.</span><span class="sxs-lookup"><span data-stu-id="9566c-108">The sample for the media stream source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9566c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9566c-109">Return value</span></span>

<span data-ttu-id="9566c-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9566c-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9566c-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9566c-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9566c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9566c-112">Requirements</span></span>



| <span data-ttu-id="9566c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9566c-113">Requirement</span></span> | <span data-ttu-id="9566c-114">Value</span><span class="sxs-lookup"><span data-stu-id="9566c-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9566c-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9566c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9566c-116">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="9566c-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="9566c-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9566c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9566c-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="9566c-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="9566c-119">IDL</span><span class="sxs-lookup"><span data-stu-id="9566c-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9566c-120"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9566c-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9566c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9566c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9566c-122">**IMFMediaStreamSourceSampleRequest**</span><span class="sxs-lookup"><span data-stu-id="9566c-122">**IMFMediaStreamSourceSampleRequest**</span></span>](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 




