---
description: Función de proxy para el método CreateStream (.
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: IWICImagingFactory_CreateStream_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 61670dbe3c1689a3d5b8030585a2b13d281efd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707001"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a><span data-ttu-id="fb707-103">IWICImagingFactory \_ CreateStream ( \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="fb707-103">IWICImagingFactory\_CreateStream\_Proxy function</span></span>

<span data-ttu-id="fb707-104">Función de proxy para el método [**CreateStream (**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) .</span><span class="sxs-lookup"><span data-stu-id="fb707-104">Proxy function for the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb707-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb707-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a><span data-ttu-id="fb707-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb707-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb707-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb707-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb707-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="fb707-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="fb707-109">_ppIWICStream \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb707-109">_ppIWICStream\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb707-110">Tipo: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span><span class="sxs-lookup"><span data-stu-id="fb707-110">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span></span>

<span data-ttu-id="fb707-111">Puntero que recibe un puntero a un nuevo [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span><span class="sxs-lookup"><span data-stu-id="fb707-111">A pointer that receives a pointer to a new [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb707-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb707-112">Return value</span></span>

<span data-ttu-id="fb707-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fb707-113">Type: **HRESULT**</span></span>

<span data-ttu-id="fb707-114">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="fb707-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb707-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fb707-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb707-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb707-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fb707-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb707-117">Requirements</span></span>



| <span data-ttu-id="fb707-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb707-118">Requirement</span></span> | <span data-ttu-id="fb707-119">Value</span><span class="sxs-lookup"><span data-stu-id="fb707-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb707-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb707-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fb707-121">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb707-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="fb707-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb707-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fb707-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb707-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="fb707-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb707-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb707-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb707-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




