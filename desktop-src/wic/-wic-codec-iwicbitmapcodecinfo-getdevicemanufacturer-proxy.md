---
description: Función de proxy para el método GetDeviceManufacturer.
ms.assetid: f4dbf67a-eb67-4138-a77a-7386567b95e6
title: IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3dc10df32325fd0ffc5bb24d1a4c7927b1adc7e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715066"
---
# <a name="iwicbitmapcodecinfo_getdevicemanufacturer_proxy-function"></a><span data-ttu-id="4caf3-103">IWICBitmapCodecInfo \_ GetDeviceManufacturer \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="4caf3-103">IWICBitmapCodecInfo\_GetDeviceManufacturer\_Proxy function</span></span>

<span data-ttu-id="4caf3-104">Función de proxy para el método [**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) .</span><span class="sxs-lookup"><span data-stu-id="4caf3-104">Proxy function for the [**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4caf3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4caf3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceManufacturer,
  _Inout_ WCHAR               *wzDeviceManufacturer,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="4caf3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4caf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4caf3-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4caf3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4caf3-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="4caf3-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="4caf3-109">Puntero a este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="4caf3-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="4caf3-110">*cchDeviceManufacturer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4caf3-110">*cchDeviceManufacturer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4caf3-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4caf3-111">Type: **UINT**</span></span>

<span data-ttu-id="4caf3-112">Tamaño del nombre del fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4caf3-112">The size of the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="4caf3-113">*wzDeviceManufacturer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4caf3-113">*wzDeviceManufacturer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4caf3-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="4caf3-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="4caf3-115">Puntero que recibe el nombre del fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4caf3-115">A pointer that receives the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="4caf3-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4caf3-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4caf3-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="4caf3-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="4caf3-118">Tamaño de búfer real necesario para recuperar el nombre del fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4caf3-118">The actual buffer size needed to retrieve the device manufacture's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4caf3-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4caf3-119">Return value</span></span>

<span data-ttu-id="4caf3-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4caf3-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4caf3-121">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4caf3-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4caf3-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4caf3-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4caf3-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4caf3-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4caf3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4caf3-124">Requirements</span></span>



| <span data-ttu-id="4caf3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4caf3-125">Requirement</span></span> | <span data-ttu-id="4caf3-126">Value</span><span class="sxs-lookup"><span data-stu-id="4caf3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4caf3-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4caf3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4caf3-128">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4caf3-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4caf3-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4caf3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4caf3-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4caf3-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4caf3-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4caf3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4caf3-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4caf3-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




