---
description: Función de proxy para el método GetMimeTypes.
ms.assetid: 9d05624f-da08-4475-933b-faa12bec9012
title: IWICBitmapCodecInfo_GetMimeTypes_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetMimeTypes_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eb00b2ae3cd935171a9333a55a76038ef9ae2ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541270"
---
# <a name="iwicbitmapcodecinfo_getmimetypes_proxy-function"></a><span data-ttu-id="53011-103">IWICBitmapCodecInfo \_ GetMimeTypes \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="53011-103">IWICBitmapCodecInfo\_GetMimeTypes\_Proxy function</span></span>

<span data-ttu-id="53011-104">Función de proxy para el método [**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) .</span><span class="sxs-lookup"><span data-stu-id="53011-104">Proxy function for the [**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="53011-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53011-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetMimeTypes_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _In_  UINT                cchMimeTypes,
  _Out_ WCHAR               *wzMimeTypes,
  _Out_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="53011-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53011-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53011-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="53011-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53011-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="53011-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="53011-109">Puntero a este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="53011-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="53011-110">*cchMimeTypes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="53011-110">*cchMimeTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53011-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="53011-111">Type: **UINT**</span></span>

<span data-ttu-id="53011-112">Tamaño del búfer de tipos MIME.</span><span class="sxs-lookup"><span data-stu-id="53011-112">The size of the mime types buffer.</span></span>

</dd> <dt>

<span data-ttu-id="53011-113">*wzMimeTypes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="53011-113">*wzMimeTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53011-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="53011-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="53011-115">Puntero que recibe los tipos MIME asociados al códec.</span><span class="sxs-lookup"><span data-stu-id="53011-115">A pointer that receives the mime types associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="53011-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="53011-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53011-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="53011-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="53011-118">Tamaño de búfer real necesario para recuperar todos los tipos MIME asociados al códec.</span><span class="sxs-lookup"><span data-stu-id="53011-118">The actual buffer size needed to retrieve all mime types associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53011-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53011-119">Return value</span></span>

<span data-ttu-id="53011-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="53011-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="53011-121">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="53011-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53011-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53011-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="53011-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53011-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="53011-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53011-124">Requirements</span></span>



| <span data-ttu-id="53011-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="53011-125">Requirement</span></span> | <span data-ttu-id="53011-126">Value</span><span class="sxs-lookup"><span data-stu-id="53011-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53011-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53011-127">Minimum supported client</span></span><br/> | <span data-ttu-id="53011-128">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53011-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="53011-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53011-129">Minimum supported server</span></span><br/> | <span data-ttu-id="53011-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="53011-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="53011-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53011-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53011-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53011-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




