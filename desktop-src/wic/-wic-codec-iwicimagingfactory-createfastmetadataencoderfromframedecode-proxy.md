---
description: Función de proxy para el método CreateFastMetadataEncoderFromFrameDecode.
ms.assetid: 0edc3387-47e9-401c-9153-76c8c32b52de
title: IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 101bb6aca30f3511a8eb370afa8eb8fd6dda1c21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716901"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromframedecode_proxy-function"></a><span data-ttu-id="79ecf-103">IWICImagingFactory \_ CreateFastMetadataEncoderFromFrameDecode \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="79ecf-103">IWICImagingFactory\_CreateFastMetadataEncoderFromFrameDecode\_Proxy function</span></span>

<span data-ttu-id="79ecf-104">Función de proxy para el método [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) .</span><span class="sxs-lookup"><span data-stu-id="79ecf-104">Proxy function for the [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="79ecf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79ecf-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapFrameDecode   *pIFrameDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="79ecf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79ecf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79ecf-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79ecf-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79ecf-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="79ecf-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="79ecf-109">_pIFrameDecoder \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="79ecf-109">_pIFrameDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79ecf-110">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="79ecf-110">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="79ecf-111">[_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) en la que se va a crear el [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) .</span><span class="sxs-lookup"><span data-stu-id="79ecf-111">The [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) to create the [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="79ecf-112">*ppIFME* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79ecf-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79ecf-113">Tipo: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="79ecf-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="79ecf-114">Puntero que recibe un puntero a un nuevo [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span><span class="sxs-lookup"><span data-stu-id="79ecf-114">A pointer that receives a pointer to a new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79ecf-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79ecf-115">Return value</span></span>

<span data-ttu-id="79ecf-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="79ecf-116">Type: **HRESULT**</span></span>

<span data-ttu-id="79ecf-117">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="79ecf-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="79ecf-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="79ecf-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="79ecf-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79ecf-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="79ecf-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79ecf-120">Requirements</span></span>



| <span data-ttu-id="79ecf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="79ecf-121">Requirement</span></span> | <span data-ttu-id="79ecf-122">Value</span><span class="sxs-lookup"><span data-stu-id="79ecf-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79ecf-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79ecf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="79ecf-124">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79ecf-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="79ecf-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79ecf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="79ecf-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="79ecf-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="79ecf-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79ecf-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79ecf-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79ecf-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




