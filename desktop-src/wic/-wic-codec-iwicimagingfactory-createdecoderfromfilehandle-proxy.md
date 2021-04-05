---
description: Función de proxy para el método CreateDecoderFromFileHandle.
ms.assetid: bc7f8a07-6d82-4d95-88ef-979d571758f4
title: IWICImagingFactory_CreateDecoderFromFileHandle_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 15c515bb17641e2e7b70b79552fe3bacf1f1c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002158"
---
# <a name="iwicimagingfactory_createdecoderfromfilehandle_proxy-function"></a><span data-ttu-id="29b6d-103">IWICImagingFactory \_ CreateDecoderFromFileHandle \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="29b6d-103">IWICImagingFactory\_CreateDecoderFromFileHandle\_Proxy function</span></span>

<span data-ttu-id="29b6d-104">Función de proxy para el método [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) .</span><span class="sxs-lookup"><span data-stu-id="29b6d-104">Proxy function for the [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="29b6d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29b6d-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFileHandle_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        ULONG_PTR          hFile,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="29b6d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29b6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29b6d-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29b6d-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29b6d-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="29b6d-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="29b6d-109">_hFile \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="29b6d-109">_hFile\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29b6d-110">Tipo: **ULong \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="29b6d-110">Type: **ULONG\_PTR**</span></span>

<span data-ttu-id="29b6d-111">Identificador de archivo del que se va a crear el descodificador.</span><span class="sxs-lookup"><span data-stu-id="29b6d-111">The file handle to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="29b6d-112">*pguidVendor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29b6d-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29b6d-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="29b6d-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="29b6d-114">GUID del proveedor para el descodificador.</span><span class="sxs-lookup"><span data-stu-id="29b6d-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="29b6d-115">_metadataOptions \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="29b6d-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29b6d-116">Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="29b6d-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="29b6d-117">[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) que se va a usar al crear el descodificador.</span><span class="sxs-lookup"><span data-stu-id="29b6d-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="29b6d-118">*ppIDecoder* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="29b6d-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29b6d-119">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="29b6d-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="29b6d-120">Puntero que recibe un puntero a un nuevo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="29b6d-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29b6d-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29b6d-121">Return value</span></span>

<span data-ttu-id="29b6d-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="29b6d-122">Type: **HRESULT**</span></span>

<span data-ttu-id="29b6d-123">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="29b6d-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="29b6d-124">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29b6d-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="29b6d-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29b6d-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="29b6d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29b6d-126">Requirements</span></span>



| <span data-ttu-id="29b6d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="29b6d-127">Requirement</span></span> | <span data-ttu-id="29b6d-128">Value</span><span class="sxs-lookup"><span data-stu-id="29b6d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29b6d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29b6d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="29b6d-130">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29b6d-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="29b6d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29b6d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="29b6d-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="29b6d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="29b6d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="29b6d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29b6d-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29b6d-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




