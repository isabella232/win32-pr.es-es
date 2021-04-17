---
description: Función de proxy para el método GetBitsPerPixel.
ms.assetid: bb98daeb-3886-473b-9c8e-5c606602249a
title: IWICPixelFormatInfo_GetBitsPerPixel_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetBitsPerPixel_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f8d3469ca7c1eacf1f6755cbf5b6243527639d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716711"
---
# <a name="iwicpixelformatinfo_getbitsperpixel_proxy-function"></a><span data-ttu-id="1b99b-103">IWICPixelFormatInfo \_ GetBitsPerPixel \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="1b99b-103">IWICPixelFormatInfo\_GetBitsPerPixel\_Proxy function</span></span>

<span data-ttu-id="1b99b-104">Función de proxy para el método [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) .</span><span class="sxs-lookup"><span data-stu-id="1b99b-104">Proxy function for the [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b99b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b99b-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetBitsPerPixel_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiBitsPerPixel
);
```



## <a name="parameters"></a><span data-ttu-id="1b99b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b99b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b99b-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1b99b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99b-108">Tipo: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="1b99b-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="1b99b-109">Puntero a este objeto [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="1b99b-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="1b99b-110">*puiBitsPerPixel* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1b99b-110">*puiBitsPerPixel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b99b-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="1b99b-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="1b99b-112">Puntero que recibe el BPP del formato de píxel.</span><span class="sxs-lookup"><span data-stu-id="1b99b-112">Pointer that receives the BPP of the pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b99b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b99b-113">Return value</span></span>

<span data-ttu-id="1b99b-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1b99b-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1b99b-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1b99b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b99b-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b99b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b99b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b99b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1b99b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b99b-118">Requirements</span></span>



| <span data-ttu-id="1b99b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b99b-119">Requirement</span></span> | <span data-ttu-id="1b99b-120">Value</span><span class="sxs-lookup"><span data-stu-id="1b99b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b99b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b99b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1b99b-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b99b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1b99b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b99b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1b99b-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b99b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1b99b-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1b99b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b99b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b99b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




