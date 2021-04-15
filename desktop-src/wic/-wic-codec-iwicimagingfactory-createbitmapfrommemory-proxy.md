---
description: Función de proxy para el método CreateBitmapFromMemory.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: IWICImagingFactory_CreateBitmapFromMemory_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 79893952bb6dcdbab6c4a1cea4f57355831d31c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668387"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a><span data-ttu-id="d08fb-103">IWICImagingFactory \_ CreateBitmapFromMemory \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="d08fb-103">IWICImagingFactory\_CreateBitmapFromMemory\_Proxy function</span></span>

<span data-ttu-id="d08fb-104">Función de proxy para el método [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) .</span><span class="sxs-lookup"><span data-stu-id="d08fb-104">Proxy function for the [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08fb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d08fb-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="d08fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d08fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d08fb-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d08fb-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08fb-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="d08fb-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="d08fb-109">_uiWidth \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d08fb-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08fb-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d08fb-110">Type: **UINT**</span></span>

<span data-ttu-id="d08fb-111">Ancho del nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="d08fb-111">The width of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="d08fb-112">*uiHeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d08fb-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08fb-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d08fb-113">Type: **UINT**</span></span>

<span data-ttu-id="d08fb-114">Alto del nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="d08fb-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="d08fb-115">*PixelFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d08fb-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08fb-116">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="d08fb-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="d08fb-117">Formato de píxel del nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="d08fb-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="d08fb-118">*cbStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d08fb-118">*cbStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08fb-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d08fb-119">Type: **UINT**</span></span>

<span data-ttu-id="d08fb-120">El [*paso*](/windows) de los datos de píxel especificados.</span><span class="sxs-lookup"><span data-stu-id="d08fb-120">The [*stride*](/windows) of the given pixel data.</span></span>

</dd> <dt>

<span data-ttu-id="d08fb-121">*cbBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d08fb-121">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08fb-122">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d08fb-122">Type: **UINT**</span></span>

<span data-ttu-id="d08fb-123">Tamaño de *pbBuffer*.</span><span class="sxs-lookup"><span data-stu-id="d08fb-123">The size of *pbBuffer*.</span></span>

</dd> <dt>

<span data-ttu-id="d08fb-124">*pbBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d08fb-124">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08fb-125">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="d08fb-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="d08fb-126">Búfer utilizado para crear el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="d08fb-126">The buffer used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="d08fb-127">_ppIBitmap \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d08fb-127">_ppIBitmap\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d08fb-128">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="d08fb-128">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="d08fb-129">Puntero que recibe un puntero al nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="d08fb-129">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d08fb-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d08fb-130">Return value</span></span>

<span data-ttu-id="d08fb-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d08fb-131">Type: **HRESULT**</span></span>

<span data-ttu-id="d08fb-132">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d08fb-132">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d08fb-133">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d08fb-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d08fb-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d08fb-134">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d08fb-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d08fb-135">Requirements</span></span>



| <span data-ttu-id="d08fb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d08fb-136">Requirement</span></span> | <span data-ttu-id="d08fb-137">Value</span><span class="sxs-lookup"><span data-stu-id="d08fb-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d08fb-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d08fb-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d08fb-139">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d08fb-139">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d08fb-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d08fb-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d08fb-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d08fb-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d08fb-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d08fb-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d08fb-143"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d08fb-143"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

