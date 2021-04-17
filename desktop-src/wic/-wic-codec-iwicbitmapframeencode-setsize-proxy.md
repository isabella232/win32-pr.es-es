---
description: Función de proxy para el método setSize.
ms.assetid: 28b4967f-4c8a-475c-8f86-c19e5d424a26
title: IWICBitmapFrameEncode_SetSize_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0a8046ede01cdd30d6a30eb81cbc1617531ef1d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697348"
---
# <a name="iwicbitmapframeencode_setsize_proxy-function"></a><span data-ttu-id="f2ebe-103">IWICBitmapFrameEncode \_ establece la \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="f2ebe-103">IWICBitmapFrameEncode\_SetSize\_Proxy function</span></span>

<span data-ttu-id="f2ebe-104">Función de proxy para el método [**setSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) .</span><span class="sxs-lookup"><span data-stu-id="f2ebe-104">Proxy function for the [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ebe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2ebe-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetSize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  uiWidth,
  _In_ UINT                  uiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="f2ebe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2ebe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2ebe-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f2ebe-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2ebe-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="f2ebe-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="f2ebe-109">Puntero a este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="f2ebe-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="f2ebe-110">*uiWidth* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2ebe-110">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2ebe-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f2ebe-111">Type: **UINT**</span></span>

<span data-ttu-id="f2ebe-112">Ancho de la imagen de salida.</span><span class="sxs-lookup"><span data-stu-id="f2ebe-112">The width of the output image.</span></span>

</dd> <dt>

<span data-ttu-id="f2ebe-113">*uiHeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2ebe-113">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2ebe-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f2ebe-114">Type: **UINT**</span></span>

<span data-ttu-id="f2ebe-115">Alto de la imagen de salida.</span><span class="sxs-lookup"><span data-stu-id="f2ebe-115">The height of the output image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2ebe-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2ebe-116">Return value</span></span>

<span data-ttu-id="f2ebe-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f2ebe-117">Type: **HRESULT**</span></span>

<span data-ttu-id="f2ebe-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f2ebe-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f2ebe-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2ebe-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ebe-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2ebe-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ebe-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2ebe-121">Requirements</span></span>



| <span data-ttu-id="f2ebe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2ebe-122">Requirement</span></span> | <span data-ttu-id="f2ebe-123">Value</span><span class="sxs-lookup"><span data-stu-id="f2ebe-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ebe-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2ebe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ebe-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2ebe-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f2ebe-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2ebe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ebe-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2ebe-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f2ebe-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2ebe-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2ebe-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2ebe-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




