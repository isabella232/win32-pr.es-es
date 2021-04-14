---
description: Función de proxy para el método CreateBitmapFlipRotator.
ms.assetid: 1dc55744-8ae1-4d8b-9ffd-735ee45ceb47
title: IWICImagingFactory_CreateBitmapFlipRotator_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFlipRotator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dea33ea75ad9d9626b327ee0173abc2f28a3e417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668388"
---
# <a name="iwicimagingfactory_createbitmapfliprotator_proxy-function"></a><span data-ttu-id="30600-103">IWICImagingFactory \_ CreateBitmapFlipRotator \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="30600-103">IWICImagingFactory\_CreateBitmapFlipRotator\_Proxy function</span></span>

<span data-ttu-id="30600-104">Función de proxy para el método [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="30600-104">Proxy function for the [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="30600-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30600-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFlipRotator_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _Out_ IWICBitmapFlipRotator **ppIBitmapFlipRotator
);
```



## <a name="parameters"></a><span data-ttu-id="30600-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30600-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30600-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30600-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30600-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="30600-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="30600-109">_ppIBitmapFlipRotator \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="30600-109">_ppIBitmapFlipRotator\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30600-110">Tipo: **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span><span class="sxs-lookup"><span data-stu-id="30600-110">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span></span>

<span data-ttu-id="30600-111">Puntero que recibe un puntero a un nuevo [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span><span class="sxs-lookup"><span data-stu-id="30600-111">A pointer that receives a pointer to a new [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30600-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30600-112">Return value</span></span>

<span data-ttu-id="30600-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="30600-113">Type: **HRESULT**</span></span>

<span data-ttu-id="30600-114">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="30600-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30600-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30600-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30600-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30600-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="30600-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30600-117">Requirements</span></span>



| <span data-ttu-id="30600-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="30600-118">Requirement</span></span> | <span data-ttu-id="30600-119">Value</span><span class="sxs-lookup"><span data-stu-id="30600-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30600-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30600-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30600-121">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30600-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="30600-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30600-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30600-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="30600-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="30600-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30600-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30600-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30600-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




