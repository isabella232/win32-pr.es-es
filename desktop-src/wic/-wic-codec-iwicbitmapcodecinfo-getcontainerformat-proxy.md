---
description: Función de proxy para el método GetContainerFormat.
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: IWICBitmapCodecInfo_GetContainerFormat_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 896c2ff88085c0300cffcc56c2877b98cd4ab68a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275354"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="c680c-103">IWICBitmapCodecInfo \_ GetContainerFormat \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="c680c-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="c680c-104">Función de proxy para el método [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="c680c-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c680c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c680c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="c680c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c680c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c680c-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c680c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c680c-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="c680c-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="c680c-109">Puntero a este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="c680c-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="c680c-110">*pguidContainerFormat* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c680c-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c680c-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="c680c-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="c680c-112">Puntero que recibe el GUID del contenedor.</span><span class="sxs-lookup"><span data-stu-id="c680c-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c680c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c680c-113">Return value</span></span>

<span data-ttu-id="c680c-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c680c-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c680c-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c680c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c680c-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c680c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c680c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c680c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c680c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c680c-118">Requirements</span></span>



| <span data-ttu-id="c680c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c680c-119">Requirement</span></span> | <span data-ttu-id="c680c-120">Value</span><span class="sxs-lookup"><span data-stu-id="c680c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c680c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c680c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c680c-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c680c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c680c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c680c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c680c-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c680c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c680c-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c680c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c680c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c680c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




