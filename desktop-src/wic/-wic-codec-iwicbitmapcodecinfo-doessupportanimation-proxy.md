---
description: Función de proxy para el método DoesSupportAnimation.
ms.assetid: dd7ed856-14b5-4215-96da-8f5db19a7796
title: IWICBitmapCodecInfo_DoesSupportAnimation_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportAnimation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 443a8ec7871af6161de2efbb6d4f21d65e5ae9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715069"
---
# <a name="iwicbitmapcodecinfo_doessupportanimation_proxy-function"></a><span data-ttu-id="8a6b1-103">IWICBitmapCodecInfo \_ DoesSupportAnimation \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="8a6b1-103">IWICBitmapCodecInfo\_DoesSupportAnimation\_Proxy function</span></span>

<span data-ttu-id="8a6b1-104">Función de proxy para el método [**DoesSupportAnimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) .</span><span class="sxs-lookup"><span data-stu-id="8a6b1-104">Proxy function for the [**DoesSupportAnimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a6b1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a6b1-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportAnimation_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportAnimation
);
```



## <a name="parameters"></a><span data-ttu-id="8a6b1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a6b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a6b1-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8a6b1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6b1-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="8a6b1-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="8a6b1-109">Puntero a este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="8a6b1-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="8a6b1-110">*pfSupportAnimation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8a6b1-110">*pfSupportAnimation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6b1-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="8a6b1-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="8a6b1-112">Un puntero que recibe _ *true*\* si el códec admite imágenes con información de tiempo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-112">A pointer that receives _ *TRUE*\* if the codec supports images with timing information; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a6b1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a6b1-113">Return value</span></span>

<span data-ttu-id="8a6b1-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8a6b1-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8a6b1-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8a6b1-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a6b1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a6b1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a6b1-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8a6b1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a6b1-118">Requirements</span></span>



| <span data-ttu-id="8a6b1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a6b1-119">Requirement</span></span> | <span data-ttu-id="8a6b1-120">Value</span><span class="sxs-lookup"><span data-stu-id="8a6b1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6b1-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a6b1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8a6b1-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a6b1-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8a6b1-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a6b1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8a6b1-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a6b1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8a6b1-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a6b1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a6b1-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a6b1-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




