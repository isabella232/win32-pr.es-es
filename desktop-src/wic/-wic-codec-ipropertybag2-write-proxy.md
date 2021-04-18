---
description: 'Función de proxy de Windows Imaging Component (WIC) para IPropertyBag2:: Write.'
ms.assetid: b97caba6-298a-4b36-9f39-9b5440b866c3
title: IPropertyBag2_Write_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertyBag2_Write_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c868ee748c3c2894daa63850284ae121f85975fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360249"
---
# <a name="ipropertybag2_write_proxy-function"></a><span data-ttu-id="866f0-103">IPropertyBag2 \_ escribir \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="866f0-103">IPropertyBag2\_Write\_Proxy function</span></span>

<span data-ttu-id="866f0-104">Función de proxy de Windows Imaging Component (WIC) para IPropertyBag2:: Write.</span><span class="sxs-lookup"><span data-stu-id="866f0-104">Windows Imaging Component (WIC) proxy function for IPropertyBag2::Write.</span></span>

## <a name="syntax"></a><span data-ttu-id="866f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="866f0-105">Syntax</span></span>


```C++
HRESULT IPropertyBag2_Write_Proxy(
  _In_ IPropertyBag2 *THIS_PTR,
  _In_ ULONG         cProperties,
  _In_ PROPBAG2      *ppropBag,
  _In_ VARIANT       *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="866f0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="866f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="866f0-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="866f0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="866f0-108">Tipo: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="866f0-108">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="866f0-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="866f0-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="866f0-110">_cProperties \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="866f0-110">_cProperties\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="866f0-111">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="866f0-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="866f0-112">*ppropBag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="866f0-112">*ppropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="866f0-113">Tipo: \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="866f0-113">Type: \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85))\** _</span></span>

</dd> <dt>

<span data-ttu-id="866f0-114">_pvarValue \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="866f0-114">_pvarValue\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="866f0-115">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="866f0-115">Type: \**VARIANT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="866f0-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="866f0-116">Return value</span></span>

<span data-ttu-id="866f0-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="866f0-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="866f0-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="866f0-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="866f0-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="866f0-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="866f0-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="866f0-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="866f0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="866f0-121">Requirements</span></span>



| <span data-ttu-id="866f0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="866f0-122">Requirement</span></span> | <span data-ttu-id="866f0-123">Value</span><span class="sxs-lookup"><span data-stu-id="866f0-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="866f0-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="866f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="866f0-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="866f0-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="866f0-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="866f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="866f0-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="866f0-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="866f0-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="866f0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="866f0-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="866f0-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

