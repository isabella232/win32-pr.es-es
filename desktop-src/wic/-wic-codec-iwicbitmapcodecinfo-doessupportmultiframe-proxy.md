---
description: Función de proxy para el método DoesSupportMultiframe.
ms.assetid: ceee0090-ff23-4eb4-b0ea-de1d12bceef8
title: IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d148127345e77da027191114f7e411bdae564deb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154170"
---
# <a name="iwicbitmapcodecinfo_doessupportmultiframe_proxy-function"></a><span data-ttu-id="9ba32-103">IWICBitmapCodecInfo \_ DoesSupportMultiframe \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="9ba32-103">IWICBitmapCodecInfo\_DoesSupportMultiframe\_Proxy function</span></span>

<span data-ttu-id="9ba32-104">Función de proxy para el método [**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) .</span><span class="sxs-lookup"><span data-stu-id="9ba32-104">Proxy function for the [**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba32-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ba32-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportMultiframe
);
```



## <a name="parameters"></a><span data-ttu-id="9ba32-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ba32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ba32-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9ba32-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ba32-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="9ba32-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="9ba32-109">Puntero a este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="9ba32-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="9ba32-110">*pfSupportMultiframe* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9ba32-110">*pfSupportMultiframe* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ba32-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="9ba32-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="9ba32-112">Un puntero que recibe _ *true*\* si el códec admite imágenes de varios fotogramas; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9ba32-112">A pointer that receives _ *TRUE*\* if the codec supports multi frame images; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ba32-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ba32-113">Return value</span></span>

<span data-ttu-id="9ba32-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9ba32-114">Type: **HRESULT**</span></span>

<span data-ttu-id="9ba32-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9ba32-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ba32-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ba32-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ba32-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ba32-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba32-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ba32-118">Requirements</span></span>



| <span data-ttu-id="9ba32-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ba32-119">Requirement</span></span> | <span data-ttu-id="9ba32-120">Value</span><span class="sxs-lookup"><span data-stu-id="9ba32-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba32-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ba32-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba32-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ba32-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9ba32-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ba32-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba32-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ba32-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9ba32-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ba32-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ba32-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ba32-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




