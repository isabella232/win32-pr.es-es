---
description: Función de proxy para el método DoesSupportLossless.
ms.assetid: c88d7971-cc93-458c-a31e-19a8b8350d09
title: IWICBitmapCodecInfo_DoesSupportLossless_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportLossless_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f498af72391aa0a7745ed79d06c6e1d55317393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809584"
---
# <a name="iwicbitmapcodecinfo_doessupportlossless_proxy-function"></a><span data-ttu-id="51944-103">IWICBitmapCodecInfo \_ DoesSupportLossless \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="51944-103">IWICBitmapCodecInfo\_DoesSupportLossless\_Proxy function</span></span>

<span data-ttu-id="51944-104">Función de proxy para el método [**DoesSupportLossless**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless) .</span><span class="sxs-lookup"><span data-stu-id="51944-104">Proxy function for the [**DoesSupportLossless**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51944-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51944-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportLossless_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportLossless
);
```



## <a name="parameters"></a><span data-ttu-id="51944-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51944-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51944-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="51944-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51944-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="51944-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="51944-109">Puntero a este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="51944-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="51944-110">*pfSupportLossless* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="51944-110">*pfSupportLossless* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51944-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="51944-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="51944-112">Un puntero que recibe _ *true*\* si el códec admite formatos sin pérdida; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="51944-112">A pointer that receives _ *TRUE*\* if the codec supports lossless formats; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51944-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51944-113">Return value</span></span>

<span data-ttu-id="51944-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="51944-114">Type: **HRESULT**</span></span>

<span data-ttu-id="51944-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="51944-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51944-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51944-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="51944-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51944-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="51944-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51944-118">Requirements</span></span>



| <span data-ttu-id="51944-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="51944-119">Requirement</span></span> | <span data-ttu-id="51944-120">Value</span><span class="sxs-lookup"><span data-stu-id="51944-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51944-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51944-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51944-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51944-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="51944-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51944-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51944-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="51944-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="51944-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="51944-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51944-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51944-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




