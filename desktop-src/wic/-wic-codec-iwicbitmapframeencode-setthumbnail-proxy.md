---
description: Función de proxy para el método SetThumbnail.
ms.assetid: 3ad473ec-9218-4ed1-961d-a2aa0d542119
title: IWICBitmapFrameEncode_SetThumbnail_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 052e73911178ef0db957c5dd8edcf6e9d6892ace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911386"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="8bfc2-103">IWICBitmapFrameEncode \_ SetThumbnail, \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="8bfc2-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="8bfc2-104">Función de proxy para el método [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="8bfc2-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bfc2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bfc2-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="8bfc2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bfc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bfc2-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8bfc2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bfc2-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="8bfc2-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="8bfc2-109">Puntero a este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="8bfc2-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="8bfc2-110">*pIThumbnail* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8bfc2-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bfc2-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="8bfc2-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="8bfc2-112">Origen del mapa de bits que se va a usar como miniatura.</span><span class="sxs-lookup"><span data-stu-id="8bfc2-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bfc2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bfc2-113">Return value</span></span>

<span data-ttu-id="8bfc2-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8bfc2-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8bfc2-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8bfc2-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8bfc2-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8bfc2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bfc2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bfc2-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8bfc2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bfc2-118">Requirements</span></span>



| <span data-ttu-id="8bfc2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bfc2-119">Requirement</span></span> | <span data-ttu-id="8bfc2-120">Value</span><span class="sxs-lookup"><span data-stu-id="8bfc2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bfc2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bfc2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8bfc2-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8bfc2-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8bfc2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bfc2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8bfc2-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8bfc2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8bfc2-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8bfc2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bfc2-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bfc2-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




