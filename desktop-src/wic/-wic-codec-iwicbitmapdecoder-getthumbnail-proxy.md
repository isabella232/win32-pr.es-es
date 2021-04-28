---
description: 'IWICBitmapDecoder_GetThumbnail_Proxy función: función de proxy para el método GetThumbnail.'
ms.assetid: 37a6ba78-0d1b-47f6-9b12-8ad123c8ee86
title: IWICBitmapDecoder_GetThumbnail_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3fb4d6ae050772bb6392e1d94c88ef5bfc23d2ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100613"
---
# <a name="iwicbitmapdecoder_getthumbnail_proxy-function"></a><span data-ttu-id="48f92-103">Función IWICBitmapDecoder \_ GetThumbnail \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="48f92-103">IWICBitmapDecoder\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="48f92-104">Función de proxy para [**el método GetThumbnail.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)</span><span class="sxs-lookup"><span data-stu-id="48f92-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f92-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48f92-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetThumbnail_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="48f92-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48f92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48f92-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="48f92-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48f92-108">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="48f92-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="48f92-109">Puntero a este [**objeto IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)</span><span class="sxs-lookup"><span data-stu-id="48f92-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="48f92-110">*ppIThumbnail* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="48f92-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48f92-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="48f92-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="48f92-112">Puntero que recibe un puntero a [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="48f92-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48f92-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48f92-113">Return value</span></span>

<span data-ttu-id="48f92-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="48f92-114">Type: **HRESULT**</span></span>

<span data-ttu-id="48f92-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="48f92-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48f92-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="48f92-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="48f92-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48f92-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="48f92-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48f92-118">Requirements</span></span>



| <span data-ttu-id="48f92-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="48f92-119">Requirement</span></span> | <span data-ttu-id="48f92-120">Valor</span><span class="sxs-lookup"><span data-stu-id="48f92-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f92-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48f92-121">Minimum supported client</span></span><br/> | <span data-ttu-id="48f92-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="48f92-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="48f92-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48f92-123">Minimum supported server</span></span><br/> | <span data-ttu-id="48f92-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="48f92-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="48f92-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48f92-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48f92-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="48f92-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




