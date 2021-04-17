---
description: Función de proxy para el método GetThumbnail.
ms.assetid: 37a6ba78-0d1b-47f6-9b12-8ad123c8ee86
title: IWICBitmapDecoder_GetThumbnail_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7412999b1a685c0188e0f277e073791d753a245b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697857"
---
# <a name="iwicbitmapdecoder_getthumbnail_proxy-function"></a><span data-ttu-id="65f88-103">IWICBitmapDecoder \_ GetThumbnail, \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="65f88-103">IWICBitmapDecoder\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="65f88-104">Función de proxy para el método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="65f88-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f88-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65f88-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetThumbnail_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="65f88-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65f88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65f88-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="65f88-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f88-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="65f88-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="65f88-109">Puntero a este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="65f88-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="65f88-110">*ppIThumbnail* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="65f88-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65f88-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="65f88-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="65f88-112">Puntero que recibe un puntero al [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="65f88-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65f88-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65f88-113">Return value</span></span>

<span data-ttu-id="65f88-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="65f88-114">Type: **HRESULT**</span></span>

<span data-ttu-id="65f88-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="65f88-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65f88-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65f88-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65f88-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65f88-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="65f88-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65f88-118">Requirements</span></span>



| <span data-ttu-id="65f88-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="65f88-119">Requirement</span></span> | <span data-ttu-id="65f88-120">Value</span><span class="sxs-lookup"><span data-stu-id="65f88-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f88-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65f88-121">Minimum supported client</span></span><br/> | <span data-ttu-id="65f88-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65f88-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="65f88-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65f88-123">Minimum supported server</span></span><br/> | <span data-ttu-id="65f88-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="65f88-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="65f88-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65f88-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65f88-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65f88-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




