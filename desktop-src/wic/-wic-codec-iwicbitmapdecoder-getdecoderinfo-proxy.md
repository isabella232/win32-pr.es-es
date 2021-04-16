---
description: Función de proxy para el método GetDecoderInfo.
ms.assetid: 4117492e-d652-4c72-9979-cc4e554a6fd8
title: IWICBitmapDecoder_GetDecoderInfo_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetDecoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ca3e234bc6bbff8899b88c89169a59d9838350b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497332"
---
# <a name="iwicbitmapdecoder_getdecoderinfo_proxy-function"></a><span data-ttu-id="facaa-103">IWICBitmapDecoder \_ GetDecoderInfo, \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="facaa-103">IWICBitmapDecoder\_GetDecoderInfo\_Proxy function</span></span>

<span data-ttu-id="facaa-104">Función de proxy para el método [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="facaa-104">Proxy function for the [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="facaa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="facaa-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetDecoderInfo_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _Out_ IWICBitmapDecoderInfo **ppIDecoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="facaa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="facaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="facaa-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="facaa-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="facaa-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="facaa-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="facaa-109">Puntero a este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="facaa-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="facaa-110">*ppIDecoderInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="facaa-110">*ppIDecoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="facaa-111">Tipo: **[ **IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="facaa-111">Type: **[**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span></span>

<span data-ttu-id="facaa-112">Puntero que recibe un puntero a un [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span><span class="sxs-lookup"><span data-stu-id="facaa-112">A pointer that receives a pointer to an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="facaa-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="facaa-113">Return value</span></span>

<span data-ttu-id="facaa-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="facaa-114">Type: **HRESULT**</span></span>

<span data-ttu-id="facaa-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="facaa-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="facaa-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="facaa-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="facaa-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="facaa-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="facaa-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="facaa-118">Requirements</span></span>



| <span data-ttu-id="facaa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="facaa-119">Requirement</span></span> | <span data-ttu-id="facaa-120">Value</span><span class="sxs-lookup"><span data-stu-id="facaa-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="facaa-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="facaa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="facaa-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="facaa-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="facaa-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="facaa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="facaa-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="facaa-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="facaa-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="facaa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="facaa-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="facaa-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




