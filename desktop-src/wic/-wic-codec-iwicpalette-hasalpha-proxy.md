---
description: Función de proxy para el método HasAlpha.
ms.assetid: 8af9f588-ac22-40c4-8973-9636951cc9e6
title: IWICPalette_HasAlpha_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_HasAlpha_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f9398b2d570efb41048d88ddeeeb76d62f4ca37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002387"
---
# <a name="iwicpalette_hasalpha_proxy-function"></a><span data-ttu-id="03281-103">IWICPalette \_ HasAlpha \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="03281-103">IWICPalette\_HasAlpha\_Proxy function</span></span>

<span data-ttu-id="03281-104">Función de proxy para el método [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) .</span><span class="sxs-lookup"><span data-stu-id="03281-104">Proxy function for the [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="03281-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03281-105">Syntax</span></span>


```C++
HRESULT IWICPalette_HasAlpha_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ BOOL        *pfHasAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="03281-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03281-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03281-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="03281-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03281-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="03281-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="03281-109">Puntero a este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="03281-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="03281-110">*pfHasAlpha* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="03281-110">*pfHasAlpha* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03281-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="03281-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="03281-112">Puntero que recibe `TRUE` si la paleta contiene un color transparente; de lo contrario, `FALSE` .</span><span class="sxs-lookup"><span data-stu-id="03281-112">Pointer that receives `TRUE` if the palette contains a transparent color; otherwise, `FALSE`.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03281-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03281-113">Return value</span></span>

<span data-ttu-id="03281-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="03281-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="03281-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="03281-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="03281-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03281-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="03281-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03281-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="03281-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03281-118">Requirements</span></span>



| <span data-ttu-id="03281-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="03281-119">Requirement</span></span> | <span data-ttu-id="03281-120">Value</span><span class="sxs-lookup"><span data-stu-id="03281-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03281-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03281-121">Minimum supported client</span></span><br/> | <span data-ttu-id="03281-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03281-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="03281-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03281-123">Minimum supported server</span></span><br/> | <span data-ttu-id="03281-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="03281-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="03281-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03281-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03281-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03281-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




