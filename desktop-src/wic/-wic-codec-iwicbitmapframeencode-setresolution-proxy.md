---
description: 'IWICBitmapFrameEncode_SetResolution_Proxy función: función proxy para el método SetResolution.'
ms.assetid: dc8df5bb-c38b-4be3-a4c6-60e7d5e1cd1b
title: IWICBitmapFrameEncode_SetResolution_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 632d6e797d499c4c5468505a4cee49e088ab025a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116613"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a><span data-ttu-id="a3a97-103">IWICBitmapFrameEncode \_ SetResolution \_ Proxy function</span><span class="sxs-lookup"><span data-stu-id="a3a97-103">IWICBitmapFrameEncode\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="a3a97-104">Función de proxy para [**el método SetResolution.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)</span><span class="sxs-lookup"><span data-stu-id="a3a97-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a97-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3a97-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="a3a97-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3a97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3a97-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a3a97-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3a97-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="a3a97-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="a3a97-109">Puntero a este [**objeto IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="a3a97-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="a3a97-110">*pppX* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a3a97-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3a97-111">Tipo: **double**</span><span class="sxs-lookup"><span data-stu-id="a3a97-111">Type: **double**</span></span>

<span data-ttu-id="a3a97-112">Valor de resolución horizontal.</span><span class="sxs-lookup"><span data-stu-id="a3a97-112">The horizontal resolution value.</span></span>

</dd> <dt>

<span data-ttu-id="a3a97-113">*pppY* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a3a97-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3a97-114">Tipo: **double**</span><span class="sxs-lookup"><span data-stu-id="a3a97-114">Type: **double**</span></span>

<span data-ttu-id="a3a97-115">Valor de resolución vertical.</span><span class="sxs-lookup"><span data-stu-id="a3a97-115">The vertical resolution value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3a97-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3a97-116">Return value</span></span>

<span data-ttu-id="a3a97-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a3a97-117">Type: **HRESULT**</span></span>

<span data-ttu-id="a3a97-118">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a3a97-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a3a97-119">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="a3a97-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3a97-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3a97-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a3a97-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3a97-121">Requirements</span></span>



| <span data-ttu-id="a3a97-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3a97-122">Requirement</span></span> | <span data-ttu-id="a3a97-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a3a97-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a97-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3a97-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a3a97-125">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a3a97-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a3a97-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3a97-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a3a97-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a3a97-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a3a97-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a3a97-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3a97-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3a97-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




