---
description: Función de proxy para el método CreateBitmapFromHBITMAP.
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688298"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a><span data-ttu-id="bea2c-103">IWICImagingFactory \_ CreateBitmapFromHBITMAP \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="bea2c-103">IWICImagingFactory\_CreateBitmapFromHBITMAP\_Proxy function</span></span>

<span data-ttu-id="bea2c-104">Función de proxy para el método [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) .</span><span class="sxs-lookup"><span data-stu-id="bea2c-104">Proxy function for the [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bea2c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bea2c-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="bea2c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bea2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bea2c-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bea2c-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea2c-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="bea2c-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="bea2c-109">_hBitmap \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="bea2c-109">_hBitmap\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea2c-110">Tipo: **hBitmap**</span><span class="sxs-lookup"><span data-stu-id="bea2c-110">Type: **HBITMAP**</span></span>

<span data-ttu-id="bea2c-111">Identificador de mapa de bits del que se va a crear el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="bea2c-111">A bitmap handle to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="bea2c-112">*hPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bea2c-112">*hPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea2c-113">Tipo: **HPALETTE**</span><span class="sxs-lookup"><span data-stu-id="bea2c-113">Type: **HPALETTE**</span></span>

<span data-ttu-id="bea2c-114">Identificador de la paleta que se usa para crear el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="bea2c-114">A palette handle used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="bea2c-115">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bea2c-115">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea2c-116">Tipo: **[ **WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span><span class="sxs-lookup"><span data-stu-id="bea2c-116">Type: **[**WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span></span>

<span data-ttu-id="bea2c-117">Opciones del canal alfa para crear el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="bea2c-117">The alpha channel options to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="bea2c-118">*ppIBitmap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bea2c-118">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bea2c-119">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="bea2c-119">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="bea2c-120">Puntero que recibe un puntero al nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="bea2c-120">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bea2c-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bea2c-121">Return value</span></span>

<span data-ttu-id="bea2c-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bea2c-122">Type: **HRESULT**</span></span>

<span data-ttu-id="bea2c-123">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bea2c-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bea2c-124">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bea2c-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bea2c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bea2c-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bea2c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bea2c-126">Requirements</span></span>



| <span data-ttu-id="bea2c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bea2c-127">Requirement</span></span> | <span data-ttu-id="bea2c-128">Value</span><span class="sxs-lookup"><span data-stu-id="bea2c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bea2c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea2c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bea2c-130">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bea2c-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bea2c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea2c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bea2c-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bea2c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bea2c-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bea2c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bea2c-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bea2c-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




