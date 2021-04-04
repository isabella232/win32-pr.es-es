---
description: Función de proxy para el método GetMetadataQueryWriter.
ms.assetid: b2c61dee-b72b-408c-8cb9-de2587587f1f
title: IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy función)
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
ms.openlocfilehash: b6668ffc4261310bfa76424afcae92e14c4ed921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809566"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="e51fe-103">IWICBitmapFrameEncode \_ GetMetadataQueryWriter, \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="e51fe-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="e51fe-104">Función de proxy para el método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="e51fe-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e51fe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e51fe-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="e51fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e51fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e51fe-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e51fe-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e51fe-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="e51fe-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="e51fe-109">Puntero a este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="e51fe-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="e51fe-110">*ppIMetadataQueryWriter* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e51fe-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e51fe-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="e51fe-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="e51fe-112">Puntero que recibe un escritor de consultas de metadatos para el marco.</span><span class="sxs-lookup"><span data-stu-id="e51fe-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e51fe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e51fe-113">Return value</span></span>

<span data-ttu-id="e51fe-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e51fe-114">Type: **HRESULT**</span></span>

<span data-ttu-id="e51fe-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e51fe-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e51fe-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e51fe-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e51fe-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e51fe-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e51fe-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e51fe-118">Requirements</span></span>



| <span data-ttu-id="e51fe-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e51fe-119">Requirement</span></span> | <span data-ttu-id="e51fe-120">Value</span><span class="sxs-lookup"><span data-stu-id="e51fe-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51fe-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e51fe-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e51fe-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e51fe-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e51fe-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e51fe-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e51fe-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e51fe-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e51fe-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e51fe-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e51fe-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e51fe-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




