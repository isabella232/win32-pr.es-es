---
description: Función de proxy para el método WriteSource.
ms.assetid: d95ad80f-7a26-45a7-8103-2673989143b7
title: IWICBitmapFrameEncode_WriteSource_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_WriteSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9eb5ab9db9341d138c72d350304407966a6293d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279509"
---
# <a name="iwicbitmapframeencode_writesource_proxy-function"></a><span data-ttu-id="2b71c-103">IWICBitmapFrameEncode \_ WriteSource, \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="2b71c-103">IWICBitmapFrameEncode\_WriteSource\_Proxy function</span></span>

<span data-ttu-id="2b71c-104">Función de proxy para el método [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) .</span><span class="sxs-lookup"><span data-stu-id="2b71c-104">Proxy function for the [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b71c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b71c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_WriteSource_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ WICRect               *prc
);
```



## <a name="parameters"></a><span data-ttu-id="2b71c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b71c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b71c-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2b71c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b71c-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="2b71c-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="2b71c-109">Puntero a este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="2b71c-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="2b71c-110">*pIBitmapSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b71c-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b71c-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="2b71c-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="2b71c-112">Origen del mapa de bits que se va a codificar.</span><span class="sxs-lookup"><span data-stu-id="2b71c-112">The bitmap source to encode.</span></span>

</dd> <dt>

<span data-ttu-id="2b71c-113">_prc \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2b71c-113">_prc\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b71c-114">Tipo: \**[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="2b71c-114">Type: \**[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="2b71c-115">Rectángulo de tamaño del origen del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="2b71c-115">The size rectangle of the bitmap source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b71c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b71c-116">Return value</span></span>

<span data-ttu-id="2b71c-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2b71c-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2b71c-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2b71c-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2b71c-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b71c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b71c-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b71c-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2b71c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b71c-121">Requirements</span></span>



| <span data-ttu-id="2b71c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b71c-122">Requirement</span></span> | <span data-ttu-id="2b71c-123">Value</span><span class="sxs-lookup"><span data-stu-id="2b71c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b71c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b71c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2b71c-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b71c-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2b71c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b71c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2b71c-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b71c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2b71c-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b71c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b71c-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b71c-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




