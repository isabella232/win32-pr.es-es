---
description: Función de proxy para el método Initialize.
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: IWICFormatConverter_Initialize_Proxy función)
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
ms.openlocfilehash: 6450c1a508507db73e44ef8b88b4f94970ac6004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278472"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a><span data-ttu-id="f81fa-103">IWICFormatConverter \_ inicializar \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="f81fa-103">IWICFormatConverter\_Initialize\_Proxy function</span></span>

<span data-ttu-id="f81fa-104">Función de proxy para el método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) .</span><span class="sxs-lookup"><span data-stu-id="f81fa-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f81fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f81fa-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f81fa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f81fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f81fa-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f81fa-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f81fa-108">Tipo: \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) \** _</span><span class="sxs-lookup"><span data-stu-id="f81fa-108">Type: \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\** _</span></span>

<span data-ttu-id="f81fa-109">Puntero a este objeto [_ *IWICFormatConverter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="f81fa-109">Pointer to this [_ *IWICFormatConverter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span>

</dd> <dt>

<span data-ttu-id="f81fa-110">*pISource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f81fa-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f81fa-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="f81fa-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="f81fa-112">Mapa de bits de entrada que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="f81fa-112">The input bitmap to convert</span></span>

</dd> <dt>

<span data-ttu-id="f81fa-113">_dstFormat \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f81fa-113">_dstFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f81fa-114">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="f81fa-114">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="f81fa-115">GUID del formato de píxel de destino.</span><span class="sxs-lookup"><span data-stu-id="f81fa-115">The destination pixel format GUID.</span></span>

</dd> <dt>

<span data-ttu-id="f81fa-116">*interpolación* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f81fa-116">*dither* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f81fa-117">Tipo: **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span><span class="sxs-lookup"><span data-stu-id="f81fa-117">Type: **[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span></span>

<span data-ttu-id="f81fa-118">[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) que se usa para la conversión.</span><span class="sxs-lookup"><span data-stu-id="f81fa-118">The [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) used for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="f81fa-119">*pIPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f81fa-119">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f81fa-120">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="f81fa-120">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="f81fa-121">Paleta que se va a usar para la conversión.</span><span class="sxs-lookup"><span data-stu-id="f81fa-121">The palette to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="f81fa-122">_alphaThresholdPercent \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f81fa-122">_alphaThresholdPercent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f81fa-123">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="f81fa-123">Type: **double**</span></span>

<span data-ttu-id="f81fa-124">Umbral alfa que se va a usar para la conversión.</span><span class="sxs-lookup"><span data-stu-id="f81fa-124">The alpha threshold to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="f81fa-125">*paletteTranslate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f81fa-125">*paletteTranslate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f81fa-126">Tipo: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="f81fa-126">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="f81fa-127">Tipo de traducción de la paleta que se va a usar para la conversión.</span><span class="sxs-lookup"><span data-stu-id="f81fa-127">The palette translation type to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f81fa-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f81fa-128">Return value</span></span>

<span data-ttu-id="f81fa-129">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f81fa-129">Type: **HRESULT**</span></span>

<span data-ttu-id="f81fa-130">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f81fa-130">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f81fa-131">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f81fa-131">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f81fa-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f81fa-132">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f81fa-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f81fa-133">Requirements</span></span>



| <span data-ttu-id="f81fa-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f81fa-134">Requirement</span></span> | <span data-ttu-id="f81fa-135">Value</span><span class="sxs-lookup"><span data-stu-id="f81fa-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f81fa-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f81fa-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f81fa-137">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f81fa-137">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f81fa-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f81fa-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f81fa-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f81fa-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f81fa-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f81fa-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f81fa-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f81fa-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




