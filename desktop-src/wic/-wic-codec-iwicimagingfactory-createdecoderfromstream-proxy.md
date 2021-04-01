---
description: Función de proxy para el método CreateDecoderFromStream.
ms.assetid: 8395d647-c8c9-4715-b15d-a30755ae0a98
title: IWICImagingFactory_CreateDecoderFromStream_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1f6f84c9c29d10243f1b3bcb2cad43967547eeae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818611"
---
# <a name="iwicimagingfactory_createdecoderfromstream_proxy-function"></a><span data-ttu-id="3bbd6-103">IWICImagingFactory \_ CreateDecoderFromStream \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="3bbd6-103">IWICImagingFactory\_CreateDecoderFromStream\_Proxy function</span></span>

<span data-ttu-id="3bbd6-104">Función de proxy para el método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="3bbd6-104">Proxy function for the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbd6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bbd6-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromStream_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        IStream            *pIStream,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="3bbd6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bbd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bbd6-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3bbd6-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbd6-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="3bbd6-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="3bbd6-109">_pIStream \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="3bbd6-109">_pIStream\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbd6-110">Tipo: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="3bbd6-110">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="3bbd6-111">Secuencia de la que se va a crear el descodificador.</span><span class="sxs-lookup"><span data-stu-id="3bbd6-111">The stream to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="3bbd6-112">_pguidVendor \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="3bbd6-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbd6-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="3bbd6-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="3bbd6-114">GUID del proveedor para el descodificador.</span><span class="sxs-lookup"><span data-stu-id="3bbd6-114">The vendor GUID for the decoder .</span></span>

</dd> <dt>

<span data-ttu-id="3bbd6-115">_metadataOptions \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="3bbd6-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbd6-116">Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="3bbd6-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="3bbd6-117">[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) que se va a usar al crear el descodificador.</span><span class="sxs-lookup"><span data-stu-id="3bbd6-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="3bbd6-118">*ppIDecoder* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3bbd6-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbd6-119">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="3bbd6-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="3bbd6-120">Puntero que recibe un puntero a un nuevo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="3bbd6-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bbd6-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bbd6-121">Return value</span></span>

<span data-ttu-id="3bbd6-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3bbd6-122">Type: **HRESULT**</span></span>

<span data-ttu-id="3bbd6-123">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3bbd6-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3bbd6-124">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3bbd6-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bbd6-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3bbd6-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3bbd6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bbd6-126">Requirements</span></span>



| <span data-ttu-id="3bbd6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bbd6-127">Requirement</span></span> | <span data-ttu-id="3bbd6-128">Value</span><span class="sxs-lookup"><span data-stu-id="3bbd6-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bbd6-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bbd6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3bbd6-130">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3bbd6-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3bbd6-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bbd6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3bbd6-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3bbd6-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3bbd6-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3bbd6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bbd6-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bbd6-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

