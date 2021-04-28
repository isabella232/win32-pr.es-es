---
description: 'IWICBitmapFlipRotator_Initialize_Proxy función: función proxy para el método Initialize.'
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: IWICBitmapFlipRotator_Initialize_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4a260d6e60c0ffdeb05aa064ae8abbb38818ac8c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091163"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="e70a1-103">IWICBitmapFlipRotator \_ Initialize \_ Proxy function</span><span class="sxs-lookup"><span data-stu-id="e70a1-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="e70a1-104">Función de proxy para el [**método Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize)</span><span class="sxs-lookup"><span data-stu-id="e70a1-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70a1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e70a1-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="e70a1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e70a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e70a1-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e70a1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70a1-108">Tipo: **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span><span class="sxs-lookup"><span data-stu-id="e70a1-108">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span></span>

<span data-ttu-id="e70a1-109">Puntero a este [**objeto IWICBitmapFlipRotator.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)</span><span class="sxs-lookup"><span data-stu-id="e70a1-109">Pointer to this [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="e70a1-110">*pISource* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e70a1-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70a1-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="e70a1-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="e70a1-112">Origen del mapa de bits de entrada.</span><span class="sxs-lookup"><span data-stu-id="e70a1-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="e70a1-113">*opciones* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e70a1-113">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70a1-114">Tipo: **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="e70a1-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="e70a1-115">[**WICBitmapTransformOptions para**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) voltear o girar la imagen.</span><span class="sxs-lookup"><span data-stu-id="e70a1-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e70a1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e70a1-116">Return value</span></span>

<span data-ttu-id="e70a1-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e70a1-117">Type: **HRESULT**</span></span>

<span data-ttu-id="e70a1-118">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e70a1-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e70a1-119">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="e70a1-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e70a1-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e70a1-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e70a1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e70a1-121">Requirements</span></span>



| <span data-ttu-id="e70a1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e70a1-122">Requirement</span></span> | <span data-ttu-id="e70a1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e70a1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e70a1-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e70a1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e70a1-125">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e70a1-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e70a1-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e70a1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e70a1-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e70a1-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e70a1-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e70a1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e70a1-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e70a1-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




