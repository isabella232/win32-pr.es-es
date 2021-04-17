---
description: Función de proxy para el método CreateFastMetadataEncoderFromDecoder.
ms.assetid: eae7ed9c-9205-4e41-91b2-461fd1f5d093
title: IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cdeb682139feb03c19cd66e999b6e3b8b7b366d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697228"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromdecoder_proxy-function"></a><span data-ttu-id="417e9-103">IWICImagingFactory \_ CreateFastMetadataEncoderFromDecoder \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="417e9-103">IWICImagingFactory\_CreateFastMetadataEncoderFromDecoder\_Proxy function</span></span>

<span data-ttu-id="417e9-104">Función de proxy para el método [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) .</span><span class="sxs-lookup"><span data-stu-id="417e9-104">Proxy function for the [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="417e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="417e9-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapDecoder       *pIDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="417e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="417e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="417e9-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="417e9-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="417e9-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="417e9-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="417e9-109">_pIDecoder \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="417e9-109">_pIDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="417e9-110">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="417e9-110">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="417e9-111">El descodificador del que se va a crear [_ *IWICFastMetadataEncoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) .</span><span class="sxs-lookup"><span data-stu-id="417e9-111">The decoder to create the [_ *IWICFastMetadataEncoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="417e9-112">*ppIFME* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="417e9-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="417e9-113">Tipo: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="417e9-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="417e9-114">Puntero que recibe un puntero al nuevo [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span><span class="sxs-lookup"><span data-stu-id="417e9-114">A pointer that receives a pointer to the new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="417e9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="417e9-115">Return value</span></span>

<span data-ttu-id="417e9-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="417e9-116">Type: **HRESULT**</span></span>

<span data-ttu-id="417e9-117">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="417e9-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="417e9-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="417e9-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="417e9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="417e9-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="417e9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="417e9-120">Requirements</span></span>



| <span data-ttu-id="417e9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="417e9-121">Requirement</span></span> | <span data-ttu-id="417e9-122">Value</span><span class="sxs-lookup"><span data-stu-id="417e9-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="417e9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="417e9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="417e9-124">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="417e9-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="417e9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="417e9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="417e9-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="417e9-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="417e9-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="417e9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="417e9-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="417e9-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




