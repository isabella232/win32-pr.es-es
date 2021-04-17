---
description: Función de proxy para el método GetColorContexts.
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: IWICBitmapDecoder_GetColorContexts_Proxy función)
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
ms.openlocfilehash: 737ad4b8bbb0014a04129d3a264cecaed4b5fe8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706496"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a><span data-ttu-id="1b041-103">IWICBitmapDecoder \_ GetColorContexts, \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="1b041-103">IWICBitmapDecoder\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="1b041-104">Función de proxy para el método [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="1b041-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b041-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b041-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="1b041-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b041-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b041-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1b041-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b041-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="1b041-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="1b041-109">Puntero a este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="1b041-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="1b041-110">*enta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1b041-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b041-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1b041-111">Type: **UINT**</span></span>

<span data-ttu-id="1b041-112">El número de contextos de color que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="1b041-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="1b041-113">Este valor debe ser el tamaño de, o menor que, disponible para *ppIColorContexts*.</span><span class="sxs-lookup"><span data-stu-id="1b041-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="1b041-114">*ppIColorContexts* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1b041-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b041-115">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="1b041-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="1b041-116">Puntero que recibe un puntero a la [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="1b041-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="1b041-117">*pcActualCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1b041-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b041-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="1b041-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="1b041-119">Puntero que recibe el número de contextos de color contenidos en la imagen.</span><span class="sxs-lookup"><span data-stu-id="1b041-119">A pointer that receives the number of color contexts contained in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b041-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b041-120">Return value</span></span>

<span data-ttu-id="1b041-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1b041-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1b041-122">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1b041-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b041-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b041-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b041-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b041-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1b041-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b041-125">Requirements</span></span>



| <span data-ttu-id="1b041-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b041-126">Requirement</span></span> | <span data-ttu-id="1b041-127">Value</span><span class="sxs-lookup"><span data-stu-id="1b041-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b041-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b041-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1b041-129">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b041-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1b041-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b041-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1b041-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b041-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1b041-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1b041-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b041-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b041-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




