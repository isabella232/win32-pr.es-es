---
description: Función de proxy para el método GetResolution.
ms.assetid: 5e261c2b-534a-4875-a84f-7251d54f15c6
title: IWICBitmapSource_GetResolution_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0bcd63c01bf99e426cdbf5044223a40308fb5e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277200"
---
# <a name="iwicbitmapsource_getresolution_proxy-function"></a><span data-ttu-id="498f8-103">Función de proxy de \_ GetResolution de IWICBitmapSource \_</span><span class="sxs-lookup"><span data-stu-id="498f8-103">IWICBitmapSource\_GetResolution\_Proxy function</span></span>

<span data-ttu-id="498f8-104">Función de proxy para el método [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) .</span><span class="sxs-lookup"><span data-stu-id="498f8-104">Proxy function for the [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="498f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="498f8-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetResolution_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ double           *pDpiX,
  _Out_ double           *pDpiY
);
```



## <a name="parameters"></a><span data-ttu-id="498f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="498f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="498f8-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="498f8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="498f8-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="498f8-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="498f8-109">Puntero a este objeto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="498f8-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="498f8-110">*pDpiX* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="498f8-110">*pDpiX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="498f8-111">Tipo: \**Double \** _</span><span class="sxs-lookup"><span data-stu-id="498f8-111">Type: \**double\** _</span></span>

<span data-ttu-id="498f8-112">Puntero que recibe la resolución de PPP del eje x.</span><span class="sxs-lookup"><span data-stu-id="498f8-112">A pointer that receives the x-axis dpi resolution.</span></span>

</dd> <dt>

<span data-ttu-id="498f8-113">_pDpiY \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="498f8-113">_pDpiY\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="498f8-114">Tipo: \**Double \** _</span><span class="sxs-lookup"><span data-stu-id="498f8-114">Type: \**double\** _</span></span>

<span data-ttu-id="498f8-115">Puntero que recibe la resolución de PPP del eje y.</span><span class="sxs-lookup"><span data-stu-id="498f8-115">A pointer that receives the y-axis dpi resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="498f8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="498f8-116">Return value</span></span>

<span data-ttu-id="498f8-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="498f8-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="498f8-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="498f8-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="498f8-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="498f8-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="498f8-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="498f8-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="498f8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="498f8-121">Requirements</span></span>



| <span data-ttu-id="498f8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="498f8-122">Requirement</span></span> | <span data-ttu-id="498f8-123">Value</span><span class="sxs-lookup"><span data-stu-id="498f8-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="498f8-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="498f8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="498f8-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="498f8-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="498f8-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="498f8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="498f8-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="498f8-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="498f8-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="498f8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="498f8-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="498f8-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




