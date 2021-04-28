---
description: 'IWICBitmapDecoder_GetColorContexts_Proxy función: función proxy para el método GetColorContexts.'
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: IWICBitmapDecoder_GetColorContexts_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e550ca4ebd863e58a4bd285c48a2a01aad059b03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086263"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a><span data-ttu-id="dcefb-103">Función IWICBitmapDecoder \_ GetColorContexts \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="dcefb-103">IWICBitmapDecoder\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="dcefb-104">Función de proxy para [**el método GetColorContexts.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)</span><span class="sxs-lookup"><span data-stu-id="dcefb-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcefb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcefb-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="dcefb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcefb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcefb-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="dcefb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcefb-108">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="dcefb-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="dcefb-109">Puntero a este [**objeto IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)</span><span class="sxs-lookup"><span data-stu-id="dcefb-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="dcefb-110">*cCount* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="dcefb-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcefb-111">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="dcefb-111">Type: **UINT**</span></span>

<span data-ttu-id="dcefb-112">Número de contextos de color que se recuperarán.</span><span class="sxs-lookup"><span data-stu-id="dcefb-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="dcefb-113">Este valor debe ser el tamaño de o menor que el tamaño disponible para *ppIColorContexts.*</span><span class="sxs-lookup"><span data-stu-id="dcefb-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="dcefb-114">*ppIColorContexts* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dcefb-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcefb-115">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="dcefb-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="dcefb-116">Puntero que recibe un puntero a [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="dcefb-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="dcefb-117">*pcActualCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dcefb-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcefb-118">Tipo: **UINT \***</span><span class="sxs-lookup"><span data-stu-id="dcefb-118">Type: **UINT\***</span></span>

<span data-ttu-id="dcefb-119">Puntero que recibe el número de contextos de color contenidos en la imagen.</span><span class="sxs-lookup"><span data-stu-id="dcefb-119">A pointer that receives the number of color contexts contained in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcefb-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcefb-120">Return value</span></span>

<span data-ttu-id="dcefb-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dcefb-121">Type: **HRESULT**</span></span>

<span data-ttu-id="dcefb-122">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dcefb-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dcefb-123">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="dcefb-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcefb-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcefb-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dcefb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcefb-125">Requirements</span></span>



| <span data-ttu-id="dcefb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcefb-126">Requirement</span></span> | <span data-ttu-id="dcefb-127">Valor</span><span class="sxs-lookup"><span data-stu-id="dcefb-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcefb-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcefb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dcefb-129">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dcefb-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="dcefb-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcefb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dcefb-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcefb-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="dcefb-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dcefb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcefb-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcefb-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




