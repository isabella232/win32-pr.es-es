---
description: Función de proxy para el método GetFileExtensions.
ms.assetid: 1c9232c5-54f3-4186-a1c8-4531e8357d06
title: IWICBitmapCodecInfo_GetFileExtensions_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetFileExtensions_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7dc44622bb7d576bfe4dc8a70e69779a72c1c07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360245"
---
# <a name="iwicbitmapcodecinfo_getfileextensions_proxy-function"></a><span data-ttu-id="39a7b-103">IWICBitmapCodecInfo \_ GetFileExtensions \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="39a7b-103">IWICBitmapCodecInfo\_GetFileExtensions\_Proxy function</span></span>

<span data-ttu-id="39a7b-104">Función de proxy para el método [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) .</span><span class="sxs-lookup"><span data-stu-id="39a7b-104">Proxy function for the [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="39a7b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39a7b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetFileExtensions_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchFileExtensions,
  _Inout_ WCHAR               *wzFileExtensions,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="39a7b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39a7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a7b-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="39a7b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a7b-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="39a7b-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="39a7b-109">Puntero a este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="39a7b-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="39a7b-110">*cchFileExtensions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39a7b-110">*cchFileExtensions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a7b-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="39a7b-111">Type: **UINT**</span></span>

<span data-ttu-id="39a7b-112">Tamaño del búfer de extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="39a7b-112">The size of the file name extension buffer.</span></span>

</dd> <dt>

<span data-ttu-id="39a7b-113">*wzFileExtensions* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="39a7b-113">*wzFileExtensions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="39a7b-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="39a7b-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="39a7b-115">Puntero que recibe las extensiones de nombre de archivo asociadas al códec.</span><span class="sxs-lookup"><span data-stu-id="39a7b-115">A pointer that receives the file name extensions associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="39a7b-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="39a7b-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="39a7b-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="39a7b-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="39a7b-118">El tamaño de búfer real necesario para recuperar todas las extensiones de nombre de archivo asociadas al códec.</span><span class="sxs-lookup"><span data-stu-id="39a7b-118">The actual buffer size needed to retrieve all file name extensions associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a7b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39a7b-119">Return value</span></span>

<span data-ttu-id="39a7b-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="39a7b-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="39a7b-121">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="39a7b-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="39a7b-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39a7b-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="39a7b-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39a7b-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="39a7b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39a7b-124">Requirements</span></span>



| <span data-ttu-id="39a7b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="39a7b-125">Requirement</span></span> | <span data-ttu-id="39a7b-126">Value</span><span class="sxs-lookup"><span data-stu-id="39a7b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a7b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39a7b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="39a7b-128">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39a7b-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="39a7b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39a7b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="39a7b-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="39a7b-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="39a7b-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39a7b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39a7b-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39a7b-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




