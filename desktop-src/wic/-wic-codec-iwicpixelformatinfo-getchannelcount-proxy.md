---
description: Función de proxy para el método GetChannelCount.
ms.assetid: f74916d9-d4b5-4b1b-adba-489d46c8d81c
title: IWICPixelFormatInfo_GetChannelCount_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6bf3f0d8aaf6cf95633fa4cce771bd7c7e8db85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697854"
---
# <a name="iwicpixelformatinfo_getchannelcount_proxy-function"></a><span data-ttu-id="cbee1-103">IWICPixelFormatInfo \_ GetChannelCount \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="cbee1-103">IWICPixelFormatInfo\_GetChannelCount\_Proxy function</span></span>

<span data-ttu-id="cbee1-104">Función de proxy para el método [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) .</span><span class="sxs-lookup"><span data-stu-id="cbee1-104">Proxy function for the [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbee1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbee1-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelCount_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiChannelCount
);
```



## <a name="parameters"></a><span data-ttu-id="cbee1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbee1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbee1-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="cbee1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbee1-108">Tipo: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="cbee1-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="cbee1-109">Puntero a este objeto [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="cbee1-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="cbee1-110">*puiChannelCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cbee1-110">*puiChannelCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbee1-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="cbee1-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="cbee1-112">Puntero que recibe el recuento de canales.</span><span class="sxs-lookup"><span data-stu-id="cbee1-112">Pointer that receives the channel count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbee1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbee1-113">Return value</span></span>

<span data-ttu-id="cbee1-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="cbee1-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="cbee1-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="cbee1-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cbee1-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cbee1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbee1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbee1-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cbee1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbee1-118">Requirements</span></span>



| <span data-ttu-id="cbee1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbee1-119">Requirement</span></span> | <span data-ttu-id="cbee1-120">Value</span><span class="sxs-lookup"><span data-stu-id="cbee1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbee1-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbee1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cbee1-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbee1-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cbee1-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbee1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cbee1-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cbee1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cbee1-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cbee1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbee1-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbee1-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




