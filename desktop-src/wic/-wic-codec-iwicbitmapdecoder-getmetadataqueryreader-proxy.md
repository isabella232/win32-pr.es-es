---
description: 'IWICBitmapDecoder_GetMetadataQueryReader_Proxy función : función de proxy para el método GetMetadataQueryReader.'
ms.assetid: cc32bdf1-d807-46ac-87b7-77bf2d498e72
title: IWICBitmapDecoder_GetMetadataQueryReader_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ebda8edb5c2007b1dfb39ca9f406855da05c456a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100653"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="81a38-103">Función IWICBitmapDecoder \_ GetMetadataQueryReader \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="81a38-103">IWICBitmapDecoder\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="81a38-104">Función de proxy para [**el método GetMetadataQueryReader.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)</span><span class="sxs-lookup"><span data-stu-id="81a38-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a38-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81a38-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="81a38-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81a38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a38-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="81a38-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a38-108">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="81a38-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="81a38-109">Puntero a este [**objeto IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)</span><span class="sxs-lookup"><span data-stu-id="81a38-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="81a38-110">*ppIMetadataQueryReader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="81a38-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81a38-111">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="81a38-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="81a38-112">Puntero que recibe un puntero a los metadatos.</span><span class="sxs-lookup"><span data-stu-id="81a38-112">A pointer that receives a pointer to the metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a38-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81a38-113">Return value</span></span>

<span data-ttu-id="81a38-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="81a38-114">Type: **HRESULT**</span></span>

<span data-ttu-id="81a38-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="81a38-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="81a38-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="81a38-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="81a38-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81a38-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="81a38-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81a38-118">Requirements</span></span>



| <span data-ttu-id="81a38-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="81a38-119">Requirement</span></span> | <span data-ttu-id="81a38-120">Valor</span><span class="sxs-lookup"><span data-stu-id="81a38-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81a38-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81a38-121">Minimum supported client</span></span><br/> | <span data-ttu-id="81a38-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="81a38-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="81a38-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81a38-123">Minimum supported server</span></span><br/> | <span data-ttu-id="81a38-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="81a38-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="81a38-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81a38-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81a38-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="81a38-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




