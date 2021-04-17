---
description: Función de proxy para el método CreateDecoderFromFilename.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: IWICImagingFactory_CreateDecoderFromFilename_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3497d71475198d035a496909e65c47df6c5f8b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697812"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a><span data-ttu-id="238e8-103">IWICImagingFactory \_ CreateDecoderFromFilename \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="238e8-103">IWICImagingFactory\_CreateDecoderFromFilename\_Proxy function</span></span>

<span data-ttu-id="238e8-104">Función de proxy para el método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .</span><span class="sxs-lookup"><span data-stu-id="238e8-104">Proxy function for the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="238e8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="238e8-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="238e8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="238e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="238e8-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="238e8-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238e8-108">Tipo: \**IWICImagingFactory \** _</span><span class="sxs-lookup"><span data-stu-id="238e8-108">Type: \**IWICImagingFactory \** _</span></span>

</dd> <dt>

<span data-ttu-id="238e8-109">_wzFilename \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="238e8-109">_wzFilename\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238e8-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="238e8-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="238e8-111">Puntero a una cadena terminada en null que especifica el nombre de un objeto que se va a crear o abrir.</span><span class="sxs-lookup"><span data-stu-id="238e8-111">A pointer to a null-terminated string that specifies the name of an object to create or open.</span></span>

</dd> <dt>

<span data-ttu-id="238e8-112">*pguidVendor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="238e8-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238e8-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="238e8-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="238e8-114">GUID del proveedor para el descodificador.</span><span class="sxs-lookup"><span data-stu-id="238e8-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="238e8-115">_dwDesiredAccess \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="238e8-115">_dwDesiredAccess\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238e8-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="238e8-116">Type: **DWORD**</span></span>

<span data-ttu-id="238e8-117">El acceso al objeto, que puede ser de lectura, escritura o ambos.</span><span class="sxs-lookup"><span data-stu-id="238e8-117">The access to the object, which can be read, write, or both.</span></span>

<span data-ttu-id="238e8-118">Para obtener más información, consulte [File Security and Access \[ Rights \] files](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="238e8-118">For more information, see [File Security and Access Rights \[Files\]](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="238e8-119">*metadataOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="238e8-119">*metadataOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238e8-120">Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="238e8-120">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="238e8-121">[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) que se va a usar al crear el descodificador.</span><span class="sxs-lookup"><span data-stu-id="238e8-121">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="238e8-122">*ppIDecoder* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="238e8-122">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="238e8-123">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="238e8-123">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="238e8-124">Puntero que recibe un puntero al nuevo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="238e8-124">A pointer that receives a pointer to the new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="238e8-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="238e8-125">Return value</span></span>

<span data-ttu-id="238e8-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="238e8-126">Type: **HRESULT**</span></span>

<span data-ttu-id="238e8-127">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="238e8-127">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="238e8-128">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="238e8-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="238e8-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="238e8-129">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="238e8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="238e8-130">Requirements</span></span>



| <span data-ttu-id="238e8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="238e8-131">Requirement</span></span> | <span data-ttu-id="238e8-132">Value</span><span class="sxs-lookup"><span data-stu-id="238e8-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="238e8-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="238e8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="238e8-134">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="238e8-134">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="238e8-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="238e8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="238e8-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="238e8-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="238e8-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="238e8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="238e8-138"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="238e8-138"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

