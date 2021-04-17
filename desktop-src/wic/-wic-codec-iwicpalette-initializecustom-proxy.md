---
description: Función de proxy para el método InitializeCustom.
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: IWICPalette_InitializeCustom_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3b64daf458a6b916f0f9e2ba23e135d6c7328a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716787"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a><span data-ttu-id="ae074-103">IWICPalette \_ InitializeCustom \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="ae074-103">IWICPalette\_InitializeCustom\_Proxy function</span></span>

<span data-ttu-id="ae074-104">Función de proxy para el método [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) .</span><span class="sxs-lookup"><span data-stu-id="ae074-104">Proxy function for the [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae074-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae074-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a><span data-ttu-id="ae074-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae074-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae074-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ae074-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae074-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="ae074-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="ae074-109">Puntero a este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="ae074-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="ae074-110">*pColors* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae074-110">*pColors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae074-111">Tipo: \**WICColor \** _</span><span class="sxs-lookup"><span data-stu-id="ae074-111">Type: \**WICColor\** _</span></span>

<span data-ttu-id="ae074-112">Puntero a la matriz de colores.</span><span class="sxs-lookup"><span data-stu-id="ae074-112">Pointer to the color array.</span></span>

</dd> <dt>

<span data-ttu-id="ae074-113">_colorCount \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ae074-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae074-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ae074-114">Type: **UINT**</span></span>

<span data-ttu-id="ae074-115">El número de colores de *pColors*.</span><span class="sxs-lookup"><span data-stu-id="ae074-115">The number of colors in *pColors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae074-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae074-116">Return value</span></span>

<span data-ttu-id="ae074-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ae074-117">Type: **HRESULT**</span></span>

<span data-ttu-id="ae074-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ae074-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ae074-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae074-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae074-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae074-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ae074-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae074-121">Requirements</span></span>



| <span data-ttu-id="ae074-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae074-122">Requirement</span></span> | <span data-ttu-id="ae074-123">Value</span><span class="sxs-lookup"><span data-stu-id="ae074-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae074-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae074-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ae074-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae074-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ae074-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae074-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ae074-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae074-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ae074-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae074-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae074-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae074-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




