---
description: Función de proxy para el método CreateBitmapClipper.
ms.assetid: 163a8d7b-f22b-4ab5-9dba-00b0cdaab440
title: IWICImagingFactory_CreateBitmapClipper_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapClipper_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fb722622ce9a8b3ad3144bcf9ea53942c8e611aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002710"
---
# <a name="iwicimagingfactory_createbitmapclipper_proxy-function"></a><span data-ttu-id="5a14a-103">IWICImagingFactory \_ CreateBitmapClipper \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="5a14a-103">IWICImagingFactory\_CreateBitmapClipper\_Proxy function</span></span>

<span data-ttu-id="5a14a-104">Función de proxy para el método [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="5a14a-104">Proxy function for the [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a14a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a14a-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapClipper_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapClipper  **ppIBitmapClipper
);
```



## <a name="parameters"></a><span data-ttu-id="5a14a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a14a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a14a-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5a14a-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a14a-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="5a14a-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="5a14a-109">_ppIBitmapClipper \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5a14a-109">_ppIBitmapClipper\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a14a-110">Tipo: **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span><span class="sxs-lookup"><span data-stu-id="5a14a-110">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span></span>

<span data-ttu-id="5a14a-111">Puntero que recibe un puntero a un nuevo [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span><span class="sxs-lookup"><span data-stu-id="5a14a-111">A pointer that receives a pointer to a new [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a14a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a14a-112">Return value</span></span>

<span data-ttu-id="5a14a-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5a14a-113">Type: **HRESULT**</span></span>

<span data-ttu-id="5a14a-114">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5a14a-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a14a-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a14a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a14a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a14a-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5a14a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a14a-117">Requirements</span></span>



| <span data-ttu-id="5a14a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a14a-118">Requirement</span></span> | <span data-ttu-id="5a14a-119">Value</span><span class="sxs-lookup"><span data-stu-id="5a14a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a14a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a14a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a14a-121">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a14a-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5a14a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a14a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a14a-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a14a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5a14a-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a14a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a14a-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a14a-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




