---
description: 'IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy función: función proxy para el método GetMetadataQueryWriter.'
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b06bc6fbcdc65c9d1163ccb4a862d6046b455c9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097173"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="3095c-103">Función IWICFastMetadataEncoder \_ GetMetadataQueryWriter \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="3095c-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="3095c-104">Función de proxy para [**el método GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="3095c-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3095c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3095c-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="3095c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3095c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3095c-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="3095c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3095c-108">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="3095c-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="3095c-109">Puntero a este [**objeto IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="3095c-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="3095c-110">*ppIMetadataQueryWriter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3095c-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3095c-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="3095c-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="3095c-112">Puntero que recibe un puntero al escritor de consultas de metadatos del codificador.</span><span class="sxs-lookup"><span data-stu-id="3095c-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3095c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3095c-113">Return value</span></span>

<span data-ttu-id="3095c-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3095c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="3095c-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3095c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3095c-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="3095c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3095c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3095c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3095c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3095c-118">Requirements</span></span>



| <span data-ttu-id="3095c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3095c-119">Requirement</span></span> | <span data-ttu-id="3095c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3095c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3095c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3095c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3095c-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3095c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3095c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3095c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3095c-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3095c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3095c-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3095c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3095c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3095c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




