---
description: Función de proxy para el método GetColorCount.
ms.assetid: 2ad87383-4d30-4df0-b43a-95fdad1d59f9
title: IWICPalette_GetColorCount_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColorCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9518878dd05c6b89152b91863c8996f96b8e6e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911385"
---
# <a name="iwicpalette_getcolorcount_proxy-function"></a><span data-ttu-id="2ca9c-103">IWICPalette \_ GetColorCount \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="2ca9c-103">IWICPalette\_GetColorCount\_Proxy function</span></span>

<span data-ttu-id="2ca9c-104">Función de proxy para el método [**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) .</span><span class="sxs-lookup"><span data-stu-id="2ca9c-104">Proxy function for the [**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca9c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ca9c-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColorCount_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ UINT        *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="2ca9c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ca9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ca9c-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2ca9c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ca9c-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="2ca9c-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="2ca9c-109">Puntero a este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="2ca9c-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="2ca9c-110">*pcCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2ca9c-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ca9c-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="2ca9c-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="2ca9c-112">Puntero que recibe el número de colores de la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="2ca9c-112">Pointer that receives the number of colors in the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ca9c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ca9c-113">Return value</span></span>

<span data-ttu-id="2ca9c-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2ca9c-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2ca9c-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2ca9c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2ca9c-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ca9c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ca9c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ca9c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca9c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ca9c-118">Requirements</span></span>



| <span data-ttu-id="2ca9c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca9c-119">Requirement</span></span> | <span data-ttu-id="2ca9c-120">Value</span><span class="sxs-lookup"><span data-stu-id="2ca9c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca9c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ca9c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca9c-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ca9c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2ca9c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ca9c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca9c-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ca9c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2ca9c-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ca9c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ca9c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ca9c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




