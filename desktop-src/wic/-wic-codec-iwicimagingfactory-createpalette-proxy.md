---
description: Función de proxy para el método CreatePalette.
ms.assetid: c83b4239-ce6b-4a4c-ab70-df31dfcdd26c
title: IWICImagingFactory_CreatePalette_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreatePalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 626c05ec5e4e365cf61304c4b33e621967cea5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717151"
---
# <a name="iwicimagingfactory_createpalette_proxy-function"></a><span data-ttu-id="ab53c-103">IWICImagingFactory \_ CreatePalette \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="ab53c-103">IWICImagingFactory\_CreatePalette\_Proxy function</span></span>

<span data-ttu-id="ab53c-104">Función de proxy para el método [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) .</span><span class="sxs-lookup"><span data-stu-id="ab53c-104">Proxy function for the [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab53c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab53c-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreatePalette_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICPalette        **ppIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="ab53c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab53c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab53c-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab53c-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab53c-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="ab53c-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="ab53c-109">_ppIPalette \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ab53c-109">_ppIPalette\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab53c-110">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span><span class="sxs-lookup"><span data-stu-id="ab53c-110">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span></span>

<span data-ttu-id="ab53c-111">Puntero que recibe un puntero a un nuevo [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span><span class="sxs-lookup"><span data-stu-id="ab53c-111">A pointer that receives a pointer to a new [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab53c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab53c-112">Return value</span></span>

<span data-ttu-id="ab53c-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ab53c-113">Type: **HRESULT**</span></span>

<span data-ttu-id="ab53c-114">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ab53c-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab53c-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab53c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab53c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab53c-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ab53c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab53c-117">Requirements</span></span>



| <span data-ttu-id="ab53c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab53c-118">Requirement</span></span> | <span data-ttu-id="ab53c-119">Value</span><span class="sxs-lookup"><span data-stu-id="ab53c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab53c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab53c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab53c-121">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab53c-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ab53c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab53c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab53c-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab53c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ab53c-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab53c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab53c-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab53c-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




