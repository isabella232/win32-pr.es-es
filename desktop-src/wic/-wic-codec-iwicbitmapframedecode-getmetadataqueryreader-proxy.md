---
description: IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy función proxy para el método GetMetadataQueryReader.
ms.assetid: 2a3e0a59-3524-4da4-993a-607a3727faba
title: IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c6c00cc4463bd8540e5baeb41a10577e9f67e85c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091143"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="5e597-103">Función IWICBitmapFrameDecode \_ GetMetadataQueryReader \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="5e597-103">IWICBitmapFrameDecode\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="5e597-104">Función de proxy para [**el método GetMetadataQueryReader.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)</span><span class="sxs-lookup"><span data-stu-id="5e597-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e597-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e597-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="5e597-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e597-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e597-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="5e597-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e597-108">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="5e597-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="5e597-109">Puntero a este [**objeto IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="5e597-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="5e597-110">*ppIMetadataQueryReader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5e597-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e597-111">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="5e597-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="5e597-112">Puntero que recibe un puntero a [**un objeto IWICMetadataQueryReader.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)</span><span class="sxs-lookup"><span data-stu-id="5e597-112">A pointer that receives a pointer to an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e597-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e597-113">Return value</span></span>

<span data-ttu-id="5e597-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5e597-114">Type: **HRESULT**</span></span>

<span data-ttu-id="5e597-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5e597-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e597-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="5e597-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e597-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e597-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5e597-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e597-118">Requirements</span></span>



| <span data-ttu-id="5e597-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e597-119">Requirement</span></span> | <span data-ttu-id="5e597-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5e597-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e597-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e597-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5e597-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e597-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5e597-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e597-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5e597-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e597-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5e597-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e597-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e597-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e597-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




