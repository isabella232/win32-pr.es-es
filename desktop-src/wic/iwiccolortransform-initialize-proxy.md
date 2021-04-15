---
description: Inicializa un IWICColorTransform con IWICBitmapSource y lo transforma de un IWICColorContext a otro.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: IWICColorTransform_Initialize_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708787"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a><span data-ttu-id="c5b49-103">IWICColorTransform \_ inicializar \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="c5b49-103">IWICColorTransform\_Initialize\_Proxy function</span></span>

<span data-ttu-id="c5b49-104">Inicializa un [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) con [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) y lo transforma de un [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) a otro.</span><span class="sxs-lookup"><span data-stu-id="c5b49-104">Initializes an [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) with a [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) and transforms it from one [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b49-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5b49-105">Syntax</span></span>


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a><span data-ttu-id="c5b49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5b49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b49-107">*pIColorTransform* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5b49-107">*pIColorTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b49-108">Tipo: **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span><span class="sxs-lookup"><span data-stu-id="c5b49-108">Type: **[**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span></span>

<span data-ttu-id="c5b49-109">Transformación de color que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="c5b49-109">The color transform to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="c5b49-110">*pIBitmapSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5b49-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b49-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="c5b49-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="c5b49-112">Origen de mapa de bits utilizado para inicializar la transformación de color.</span><span class="sxs-lookup"><span data-stu-id="c5b49-112">The bitmap source used to initialize the color transform.</span></span>

</dd> <dt>

<span data-ttu-id="c5b49-113">*pIContextSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5b49-113">*pIContextSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b49-114">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="c5b49-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="c5b49-115">Origen del contexto de color.</span><span class="sxs-lookup"><span data-stu-id="c5b49-115">The color context source.</span></span>

</dd> <dt>

<span data-ttu-id="c5b49-116">*pIContextDest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5b49-116">*pIContextDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b49-117">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="c5b49-117">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="c5b49-118">El destino del contexto de color.</span><span class="sxs-lookup"><span data-stu-id="c5b49-118">The color context destination.</span></span>

</dd> <dt>

<span data-ttu-id="c5b49-119">*pixelFmtDest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5b49-119">*pixelFmtDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b49-120">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="c5b49-120">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="c5b49-121">GUID del formato de píxel deseado.</span><span class="sxs-lookup"><span data-stu-id="c5b49-121">The GUID of the desired pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b49-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5b49-122">Return value</span></span>

<span data-ttu-id="c5b49-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c5b49-123">Type: **HRESULT**</span></span>

<span data-ttu-id="c5b49-124">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c5b49-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c5b49-125">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5b49-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b49-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5b49-126">Requirements</span></span>



| <span data-ttu-id="c5b49-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5b49-127">Requirement</span></span> | <span data-ttu-id="c5b49-128">Value</span><span class="sxs-lookup"><span data-stu-id="c5b49-128">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b49-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5b49-129">DLL</span></span><br/> | <dl> <span data-ttu-id="c5b49-130"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5b49-130"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 




