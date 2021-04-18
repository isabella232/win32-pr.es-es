---
description: Función de proxy para el método GetDeviceModels.
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: IWICBitmapCodecInfo_GetDeviceModels_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b8fa6d6df6984569aa3fe49fc734f7699aa504d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715065"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a><span data-ttu-id="07c5b-103">IWICBitmapCodecInfo \_ GetDeviceModels \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="07c5b-103">IWICBitmapCodecInfo\_GetDeviceModels\_Proxy function</span></span>

<span data-ttu-id="07c5b-104">Función de proxy para el método [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) .</span><span class="sxs-lookup"><span data-stu-id="07c5b-104">Proxy function for the [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c5b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07c5b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="07c5b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07c5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07c5b-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="07c5b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07c5b-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="07c5b-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="07c5b-109">Puntero a este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="07c5b-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="07c5b-110">*cchDeviceModels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="07c5b-110">*cchDeviceModels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07c5b-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="07c5b-111">Type: **UINT**</span></span>

<span data-ttu-id="07c5b-112">Tamaño del búfer de modelos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07c5b-112">The size of the device models buffer.</span></span>

</dd> <dt>

<span data-ttu-id="07c5b-113">*wzDeviceModels* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="07c5b-113">*wzDeviceModels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07c5b-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="07c5b-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="07c5b-115">Un puntero que recibe una lista delimitada por comas de nombres de modelo de dispositivo asociados al códec.</span><span class="sxs-lookup"><span data-stu-id="07c5b-115">A pointer that receives a comma delimited list of device model names associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="07c5b-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="07c5b-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07c5b-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="07c5b-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="07c5b-118">Tamaño de búfer real necesario para recuperar todos los nombres de modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07c5b-118">The actual buffer size needed to retrieve all of the device model names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07c5b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07c5b-119">Return value</span></span>

<span data-ttu-id="07c5b-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="07c5b-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="07c5b-121">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="07c5b-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="07c5b-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07c5b-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="07c5b-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07c5b-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="07c5b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07c5b-124">Requirements</span></span>



| <span data-ttu-id="07c5b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="07c5b-125">Requirement</span></span> | <span data-ttu-id="07c5b-126">Value</span><span class="sxs-lookup"><span data-stu-id="07c5b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c5b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07c5b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="07c5b-128">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07c5b-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="07c5b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07c5b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="07c5b-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="07c5b-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="07c5b-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="07c5b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07c5b-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07c5b-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




