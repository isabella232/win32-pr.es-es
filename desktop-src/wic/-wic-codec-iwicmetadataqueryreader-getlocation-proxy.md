---
description: Función de proxy para el método GetLocation.
ms.assetid: 2dc4767b-9992-4e5a-a171-2de19178d912
title: IWICMetadataQueryReader_GetLocation_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetLocation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 40dd23df0e1004687a945889d2598d41ca0e2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678483"
---
# <a name="iwicmetadataqueryreader_getlocation_proxy-function"></a><span data-ttu-id="8664f-103">IWICMetadataQueryReader \_ la \_ función proxy GetLocation</span><span class="sxs-lookup"><span data-stu-id="8664f-103">IWICMetadataQueryReader\_GetLocation\_Proxy function</span></span>

<span data-ttu-id="8664f-104">Función de proxy para el método [**GetLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) .</span><span class="sxs-lookup"><span data-stu-id="8664f-104">Proxy function for the [**GetLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8664f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8664f-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetLocation_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    UINT                    cchMaxLength,
  _Inout_ WCHAR                   *wzNamespace,
  _Out_   UINT                    *pcchActualLength
);
```



## <a name="parameters"></a><span data-ttu-id="8664f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8664f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8664f-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8664f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8664f-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="8664f-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="8664f-109">Puntero a este objeto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="8664f-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="8664f-110">*cchMaxLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8664f-110">*cchMaxLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8664f-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8664f-111">Type: **UINT**</span></span>

<span data-ttu-id="8664f-112">Longitud del búfer de *wzNamespace* .</span><span class="sxs-lookup"><span data-stu-id="8664f-112">The length of the *wzNamespace* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8664f-113">*wzNamespace* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8664f-113">*wzNamespace* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8664f-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="8664f-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="8664f-115">Puntero que recibe la ubicación del espacio de nombres actual.</span><span class="sxs-lookup"><span data-stu-id="8664f-115">Pointer that receives the current namespace location.</span></span>

</dd> <dt>

<span data-ttu-id="8664f-116">_pcchActualLength \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8664f-116">_pcchActualLength\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8664f-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="8664f-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="8664f-118">La longitud de búfer real necesaria para recuperar la ubicación del espacio de nombres actual.</span><span class="sxs-lookup"><span data-stu-id="8664f-118">The actual buffer length needed to retrieve the current namespace location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8664f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8664f-119">Return value</span></span>

<span data-ttu-id="8664f-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8664f-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8664f-121">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8664f-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8664f-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8664f-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8664f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8664f-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8664f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8664f-124">Requirements</span></span>



| <span data-ttu-id="8664f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8664f-125">Requirement</span></span> | <span data-ttu-id="8664f-126">Value</span><span class="sxs-lookup"><span data-stu-id="8664f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8664f-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8664f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8664f-128">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8664f-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8664f-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8664f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8664f-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8664f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8664f-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8664f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8664f-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8664f-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




