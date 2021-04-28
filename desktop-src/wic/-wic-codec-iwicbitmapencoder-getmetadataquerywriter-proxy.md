---
description: 'IWICBitmapEncoder_GetMetadataQueryWriter_Proxy función: función proxy para el método GetMetadataQueryWriter.'
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: IWICBitmapEncoder_GetMetadataQueryWriter_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 798a9b5bafb2f5011e42e603b8b2c98b0ba79b37
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091173"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="cc7be-103">Función IWICBitmapEncoder \_ GetMetadataQueryWriter \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="cc7be-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="cc7be-104">Función de proxy para [**el método GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="cc7be-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc7be-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc7be-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="cc7be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc7be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc7be-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="cc7be-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc7be-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="cc7be-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="cc7be-109">Puntero a este [**objeto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="cc7be-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="cc7be-110">*ppIMetadataQueryWriter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cc7be-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc7be-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="cc7be-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="cc7be-112">Puntero que recibe un puntero a [**un objeto IWICMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="cc7be-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc7be-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc7be-113">Return value</span></span>

<span data-ttu-id="cc7be-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cc7be-114">Type: **HRESULT**</span></span>

<span data-ttu-id="cc7be-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cc7be-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc7be-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="cc7be-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc7be-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc7be-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cc7be-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc7be-118">Requirements</span></span>



| <span data-ttu-id="cc7be-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc7be-119">Requirement</span></span> | <span data-ttu-id="cc7be-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cc7be-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc7be-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc7be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cc7be-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cc7be-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cc7be-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc7be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cc7be-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc7be-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cc7be-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc7be-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc7be-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc7be-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




