---
description: Función de proxy para el método GetChannelMask.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: IWICPixelFormatInfo_GetChannelMask_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0db2c14e89aba2b13cb95209b81f6d0da5d9d949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278845"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a><span data-ttu-id="f3683-103">IWICPixelFormatInfo \_ GetChannelMask \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="f3683-103">IWICPixelFormatInfo\_GetChannelMask\_Proxy function</span></span>

<span data-ttu-id="f3683-104">Función de proxy para el método [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) .</span><span class="sxs-lookup"><span data-stu-id="f3683-104">Proxy function for the [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3683-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3683-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a><span data-ttu-id="f3683-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3683-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3683-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f3683-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3683-108">Tipo: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="f3683-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="f3683-109">Puntero a este objeto [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="f3683-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="f3683-110">*uiChannelIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3683-110">*uiChannelIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3683-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f3683-111">Type: **UINT**</span></span>

<span data-ttu-id="f3683-112">Índice de la máscara de canal que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="f3683-112">The index to the channel mask to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f3683-113">*cbMaskBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3683-113">*cbMaskBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3683-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f3683-114">Type: **UINT**</span></span>

<span data-ttu-id="f3683-115">Tamaño del búfer de *pbMaskBuffer* .</span><span class="sxs-lookup"><span data-stu-id="f3683-115">The size of the *pbMaskBuffer* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f3683-116">*pbMaskBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f3683-116">*pbMaskBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3683-117">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="f3683-117">Type: \**BYTE\** _</span></span>

<span data-ttu-id="f3683-118">Puntero al búfer de máscara.</span><span class="sxs-lookup"><span data-stu-id="f3683-118">Pointer to the mask buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f3683-119">_pcbActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f3683-119">_pcbActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3683-120">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="f3683-120">Type: \**UINT\** _</span></span>

<span data-ttu-id="f3683-121">Tamaño real del búfer necesario para obtener la máscara del canal.</span><span class="sxs-lookup"><span data-stu-id="f3683-121">The actual buffer size needed to obtain the channel mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3683-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3683-122">Return value</span></span>

<span data-ttu-id="f3683-123">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f3683-123">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f3683-124">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f3683-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3683-125">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f3683-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3683-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3683-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f3683-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3683-127">Requirements</span></span>



| <span data-ttu-id="f3683-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3683-128">Requirement</span></span> | <span data-ttu-id="f3683-129">Value</span><span class="sxs-lookup"><span data-stu-id="f3683-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3683-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3683-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f3683-131">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3683-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f3683-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3683-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f3683-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3683-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f3683-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3683-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3683-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3683-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




