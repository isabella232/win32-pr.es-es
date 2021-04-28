---
description: 'IWICFormatConverter_Initialize_Proxy función: función proxy para el método Initialize.'
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: IWICFormatConverter_Initialize_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d70d852adc8f810438ce46dc30345e68fa27e0fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097163"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a><span data-ttu-id="576e3-103">Función IWICFormatConverter \_ Initialize \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="576e3-103">IWICFormatConverter\_Initialize\_Proxy function</span></span>

<span data-ttu-id="576e3-104">Función de proxy para el [**método Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize)</span><span class="sxs-lookup"><span data-stu-id="576e3-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="576e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="576e3-105">Syntax</span></span>


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a><span data-ttu-id="576e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="576e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="576e3-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="576e3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576e3-108">Tipo: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***</span><span class="sxs-lookup"><span data-stu-id="576e3-108">Type: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***</span></span>

<span data-ttu-id="576e3-109">Puntero a este [**objeto IWICFormatConverter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)</span><span class="sxs-lookup"><span data-stu-id="576e3-109">Pointer to this [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span>

</dd> <dt>

<span data-ttu-id="576e3-110">*pISource* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="576e3-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576e3-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="576e3-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="576e3-112">Mapa de bits de entrada que se convertirá</span><span class="sxs-lookup"><span data-stu-id="576e3-112">The input bitmap to convert</span></span>

</dd> <dt>

<span data-ttu-id="576e3-113">*dstFormat* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="576e3-113">*dstFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576e3-114">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="576e3-114">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="576e3-115">GUID del formato de píxel de destino.</span><span class="sxs-lookup"><span data-stu-id="576e3-115">The destination pixel format GUID.</span></span>

</dd> <dt>

<span data-ttu-id="576e3-116">*dither* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="576e3-116">*dither* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576e3-117">Tipo: **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span><span class="sxs-lookup"><span data-stu-id="576e3-117">Type: **[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span></span>

<span data-ttu-id="576e3-118">[**WICBitmapDitherType usado**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) para la conversión.</span><span class="sxs-lookup"><span data-stu-id="576e3-118">The [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) used for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="576e3-119">*pIPalette* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="576e3-119">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576e3-120">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="576e3-120">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="576e3-121">Paleta que se usará para la conversión.</span><span class="sxs-lookup"><span data-stu-id="576e3-121">The palette to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="576e3-122">*alphaThresholdPercent* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="576e3-122">*alphaThresholdPercent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576e3-123">Tipo: **double**</span><span class="sxs-lookup"><span data-stu-id="576e3-123">Type: **double**</span></span>

<span data-ttu-id="576e3-124">Umbral alfa que se usará para la conversión.</span><span class="sxs-lookup"><span data-stu-id="576e3-124">The alpha threshold to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="576e3-125">*paletteTranslate* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="576e3-125">*paletteTranslate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576e3-126">Tipo: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="576e3-126">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="576e3-127">Tipo de traducción de paleta que se usará para la conversión.</span><span class="sxs-lookup"><span data-stu-id="576e3-127">The palette translation type to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="576e3-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="576e3-128">Return value</span></span>

<span data-ttu-id="576e3-129">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="576e3-129">Type: **HRESULT**</span></span>

<span data-ttu-id="576e3-130">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="576e3-130">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="576e3-131">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="576e3-131">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="576e3-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="576e3-132">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="576e3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="576e3-133">Requirements</span></span>



| <span data-ttu-id="576e3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="576e3-134">Requirement</span></span> | <span data-ttu-id="576e3-135">Valor</span><span class="sxs-lookup"><span data-stu-id="576e3-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="576e3-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="576e3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="576e3-137">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="576e3-137">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="576e3-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="576e3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="576e3-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="576e3-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="576e3-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="576e3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="576e3-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="576e3-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




