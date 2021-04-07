---
description: Función de proxy para el método CreateBitmapFromSource.
ms.assetid: 7d000377-1855-4971-b782-4c0bf7968c5f
title: IWICImagingFactory_CreateBitmapFromSource_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7f7be9ca9eaa8aa14dcaf3617face2dff2f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003156"
---
# <a name="iwicimagingfactory_createbitmapfromsource_proxy-function"></a><span data-ttu-id="c86da-103">IWICImagingFactory \_ CreateBitmapFromSource \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="c86da-103">IWICImagingFactory\_CreateBitmapFromSource\_Proxy function</span></span>

<span data-ttu-id="c86da-104">Función de proxy para el método [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) .</span><span class="sxs-lookup"><span data-stu-id="c86da-104">Proxy function for the [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c86da-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c86da-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromSource_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  IWICBitmapSource           *pIBitmapSource,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="c86da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c86da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c86da-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c86da-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c86da-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="c86da-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="c86da-109">_pIBitmapSource \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c86da-109">_pIBitmapSource\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c86da-110">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="c86da-110">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="c86da-111">[_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) del que se va a crear el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="c86da-111">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="c86da-112">*opción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c86da-112">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c86da-113">Tipo: **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="c86da-113">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="c86da-114">Opciones de caché del nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="c86da-114">The cache options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="c86da-115">*ppIBitmap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c86da-115">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c86da-116">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="c86da-116">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="c86da-117">Puntero que recibe un puntero al nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="c86da-117">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c86da-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c86da-118">Return value</span></span>

<span data-ttu-id="c86da-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c86da-119">Type: **HRESULT**</span></span>

<span data-ttu-id="c86da-120">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c86da-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c86da-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c86da-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c86da-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c86da-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c86da-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c86da-123">Requirements</span></span>



| <span data-ttu-id="c86da-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c86da-124">Requirement</span></span> | <span data-ttu-id="c86da-125">Value</span><span class="sxs-lookup"><span data-stu-id="c86da-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c86da-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c86da-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c86da-127">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c86da-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c86da-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c86da-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c86da-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c86da-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c86da-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c86da-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c86da-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c86da-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




