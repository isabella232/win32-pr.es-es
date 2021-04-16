---
description: Función de proxy para el método CopyPalette.
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: IWICBitmapDecoder_CopyPalette_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee6902668a9c4feffdcc696ce0d5f6214a707bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705539"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="a2466-103">IWICBitmapDecoder \_ CopyPalette, \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="a2466-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="a2466-104">Función de proxy para el método [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="a2466-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2466-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2466-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="a2466-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2466-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2466-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a2466-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2466-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="a2466-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="a2466-109">Puntero a este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="a2466-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="a2466-110">*pIPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a2466-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2466-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="a2466-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="a2466-112">Paleta de imágenes que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="a2466-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2466-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2466-113">Return value</span></span>

<span data-ttu-id="a2466-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a2466-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a2466-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a2466-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a2466-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a2466-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2466-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2466-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a2466-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2466-118">Requirements</span></span>



| <span data-ttu-id="a2466-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2466-119">Requirement</span></span> | <span data-ttu-id="a2466-120">Value</span><span class="sxs-lookup"><span data-stu-id="a2466-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2466-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2466-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2466-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2466-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a2466-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2466-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2466-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2466-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a2466-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2466-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2466-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2466-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




