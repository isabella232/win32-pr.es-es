---
description: Función de proxy para el método CreateEncoder.
ms.assetid: e3ffad7f-eb0e-481d-81ee-caf18e14ba59
title: IWICImagingFactory_CreateEncoder_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateEncoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 38e5dd19ddc07de42f8be9e8c887a4f412a853b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706488"
---
# <a name="iwicimagingfactory_createencoder_proxy-function"></a><span data-ttu-id="68c25-103">IWICImagingFactory \_ CreateEncoder \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="68c25-103">IWICImagingFactory\_CreateEncoder\_Proxy function</span></span>

<span data-ttu-id="68c25-104">Función de proxy para el método [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) .</span><span class="sxs-lookup"><span data-stu-id="68c25-104">Proxy function for the [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="68c25-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68c25-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateEncoder_Proxy(
  _In_           IWICImagingFactory *pFactory,
  _In_           REFGUID            guidContainerFormat,
  _In_opt_ const GUID               *pguidVendor,
  _Out_          IWICBitmapEncoder  **ppIEncoder
);
```



## <a name="parameters"></a><span data-ttu-id="68c25-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68c25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68c25-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68c25-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68c25-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="68c25-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="68c25-109">_guidContainerFormat \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="68c25-109">_guidContainerFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68c25-110">Tipo: **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="68c25-110">Type: **REFGUID**</span></span>

<span data-ttu-id="68c25-111">GUID para el formato de contenedor deseado.</span><span class="sxs-lookup"><span data-stu-id="68c25-111">The GUID for the desired container format.</span></span>

</dd> <dt>

<span data-ttu-id="68c25-112">*pguidVendor* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="68c25-112">*pguidVendor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68c25-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="68c25-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="68c25-114">GUID del proveedor para el codificador.</span><span class="sxs-lookup"><span data-stu-id="68c25-114">The vendor GUID for the encoder.</span></span>

</dd> <dt>

<span data-ttu-id="68c25-115">_ppIEncoder \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="68c25-115">_ppIEncoder\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68c25-116">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="68c25-116">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span></span>

<span data-ttu-id="68c25-117">Puntero que recibe un puntero a un nuevo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="68c25-117">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68c25-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68c25-118">Return value</span></span>

<span data-ttu-id="68c25-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="68c25-119">Type: **HRESULT**</span></span>

<span data-ttu-id="68c25-120">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="68c25-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68c25-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68c25-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="68c25-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68c25-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="68c25-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68c25-123">Requirements</span></span>



| <span data-ttu-id="68c25-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="68c25-124">Requirement</span></span> | <span data-ttu-id="68c25-125">Value</span><span class="sxs-lookup"><span data-stu-id="68c25-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68c25-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68c25-126">Minimum supported client</span></span><br/> | <span data-ttu-id="68c25-127">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68c25-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="68c25-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68c25-128">Minimum supported server</span></span><br/> | <span data-ttu-id="68c25-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="68c25-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="68c25-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68c25-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68c25-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68c25-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




