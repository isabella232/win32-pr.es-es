---
description: Función de proxy para el método GetFrameCount.
ms.assetid: 2103af73-60a2-4c1c-8db2-7dfd474440eb
title: IWICBitmapDecoder_GetFrameCount_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrameCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 784f362d711f22f5bfe1728f41309cdd7c22e788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809578"
---
# <a name="iwicbitmapdecoder_getframecount_proxy-function"></a><span data-ttu-id="00442-103">IWICBitmapDecoder \_ GetFrameCount, \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="00442-103">IWICBitmapDecoder\_GetFrameCount\_Proxy function</span></span>

<span data-ttu-id="00442-104">Función de proxy para el método [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .</span><span class="sxs-lookup"><span data-stu-id="00442-104">Proxy function for the [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="00442-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00442-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrameCount_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="00442-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00442-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00442-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="00442-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00442-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="00442-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="00442-109">Puntero a este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="00442-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="00442-110">*pCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="00442-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00442-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="00442-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="00442-112">Puntero que recibe el número total de fotogramas de la imagen.</span><span class="sxs-lookup"><span data-stu-id="00442-112">A pointer that receives the total number of frames in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00442-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00442-113">Return value</span></span>

<span data-ttu-id="00442-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="00442-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="00442-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="00442-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="00442-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="00442-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00442-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00442-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="00442-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00442-118">Requirements</span></span>



| <span data-ttu-id="00442-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="00442-119">Requirement</span></span> | <span data-ttu-id="00442-120">Value</span><span class="sxs-lookup"><span data-stu-id="00442-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00442-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00442-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00442-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00442-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="00442-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00442-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00442-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="00442-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="00442-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="00442-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00442-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00442-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




