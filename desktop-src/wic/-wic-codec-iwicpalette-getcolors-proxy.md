---
description: Función de proxy para el método GetColors.
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: IWICPalette_GetColors_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277777"
---
# <a name="iwicpalette_getcolors_proxy-function"></a><span data-ttu-id="1b969-103">IWICPalette \_ GetColors \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="1b969-103">IWICPalette\_GetColors\_Proxy function</span></span>

<span data-ttu-id="1b969-104">Función de proxy para el método [**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) .</span><span class="sxs-lookup"><span data-stu-id="1b969-104">Proxy function for the [**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b969-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b969-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a><span data-ttu-id="1b969-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b969-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b969-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1b969-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b969-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="1b969-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="1b969-109">Puntero a este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="1b969-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="1b969-110">*colorCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1b969-110">*colorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b969-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1b969-111">Type: **UINT**</span></span>

<span data-ttu-id="1b969-112">Tamaño de la matriz *pColors* .</span><span class="sxs-lookup"><span data-stu-id="1b969-112">The size of the *pColors* array.</span></span>

</dd> <dt>

<span data-ttu-id="1b969-113">*pColors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1b969-113">*pColors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b969-114">Tipo: \**WICColor \** _</span><span class="sxs-lookup"><span data-stu-id="1b969-114">Type: \**WICColor\** _</span></span>

<span data-ttu-id="1b969-115">Puntero que recibe los colores de la paleta.</span><span class="sxs-lookup"><span data-stu-id="1b969-115">Pointer that receives the colors of the palette.</span></span>

</dd> <dt>

<span data-ttu-id="1b969-116">_pcActualColors \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1b969-116">_pcActualColors\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b969-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="1b969-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="1b969-118">Tamaño real necesario para obtener los colores de la paleta.</span><span class="sxs-lookup"><span data-stu-id="1b969-118">The actual size needed to obtain the palette colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b969-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b969-119">Return value</span></span>

<span data-ttu-id="1b969-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1b969-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1b969-121">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1b969-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b969-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b969-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b969-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b969-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1b969-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b969-124">Requirements</span></span>



| <span data-ttu-id="1b969-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b969-125">Requirement</span></span> | <span data-ttu-id="1b969-126">Value</span><span class="sxs-lookup"><span data-stu-id="1b969-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b969-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b969-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1b969-128">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b969-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1b969-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b969-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1b969-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b969-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1b969-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1b969-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b969-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b969-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




