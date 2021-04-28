---
description: 'IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy función : función de proxy para el método GetMetadataQueryWriter.'
ms.assetid: b2c61dee-b72b-408c-8cb9-de2587587f1f
title: IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 89eb7342277d335c78ee2bc6807f2fc4d170bb9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113613"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="ed8db-103">IWICBitmapFrameEncode \_ GetMetadataQueryWriter \_ Proxy function</span><span class="sxs-lookup"><span data-stu-id="ed8db-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="ed8db-104">Función de proxy para [**el método GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="ed8db-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed8db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed8db-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="ed8db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed8db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8db-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ed8db-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8db-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="ed8db-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="ed8db-109">Puntero a este [**objeto IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="ed8db-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="ed8db-110">*ppIMetadataQueryWriter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed8db-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8db-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="ed8db-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="ed8db-112">Puntero que recibe un escritor de consultas de metadatos para el marco.</span><span class="sxs-lookup"><span data-stu-id="ed8db-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed8db-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed8db-113">Return value</span></span>

<span data-ttu-id="ed8db-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ed8db-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ed8db-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ed8db-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ed8db-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="ed8db-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed8db-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed8db-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ed8db-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed8db-118">Requirements</span></span>



| <span data-ttu-id="ed8db-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed8db-119">Requirement</span></span> | <span data-ttu-id="ed8db-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ed8db-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8db-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed8db-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ed8db-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ed8db-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ed8db-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed8db-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ed8db-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed8db-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ed8db-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed8db-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed8db-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed8db-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




