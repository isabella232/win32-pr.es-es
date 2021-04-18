---
description: 'Función de proxy de Windows Imaging Component (WIC) para IEnumString:: RESET.'
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: IEnumString_Reset_WIC_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 64057e0f49b105232f980ac3d73014156e2da732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715071"
---
# <a name="ienumstring_reset_wic_proxy-function"></a><span data-ttu-id="6e579-103">IEnumString \_ restablecimiento de la \_ función de \_ proxy WIC</span><span class="sxs-lookup"><span data-stu-id="6e579-103">IEnumString\_Reset\_WIC\_Proxy function</span></span>

<span data-ttu-id="6e579-104">Función de proxy de Windows Imaging Component (WIC) para IEnumString:: RESET.</span><span class="sxs-lookup"><span data-stu-id="6e579-104">Windows Imaging Component (WIC) proxy function for IEnumString::Reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e579-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e579-105">Syntax</span></span>


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="6e579-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e579-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e579-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="6e579-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e579-108">Tipo: \**IEnumString \** _</span><span class="sxs-lookup"><span data-stu-id="6e579-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="6e579-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="6e579-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="6e579-110">_celt \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="6e579-110">_celt\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e579-111">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="6e579-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="6e579-112">*rgelt* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6e579-112">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e579-113">Tipo: \**LPOLESTR \** _</span><span class="sxs-lookup"><span data-stu-id="6e579-113">Type: \**LPOLESTR\** _</span></span>

</dd> <dt>

<span data-ttu-id="6e579-114">_pceltFetched \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e579-114">_pceltFetched\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e579-115">Tipo: \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="6e579-115">Type: \**ULONG\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e579-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e579-116">Return value</span></span>

<span data-ttu-id="6e579-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6e579-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6e579-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6e579-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e579-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e579-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e579-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e579-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6e579-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e579-121">Requirements</span></span>



| <span data-ttu-id="6e579-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e579-122">Requirement</span></span> | <span data-ttu-id="6e579-123">Value</span><span class="sxs-lookup"><span data-stu-id="6e579-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e579-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e579-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6e579-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e579-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6e579-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e579-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6e579-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e579-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6e579-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e579-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e579-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e579-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




