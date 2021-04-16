---
description: Función de proxy para el método Initialize.
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: IWICBitmapFlipRotator_Initialize_Proxy función)
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
ms.openlocfilehash: 82a1aa5648edd47d0b635a407adc001c25183b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705535"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="f6a35-103">IWICBitmapFlipRotator \_ inicializar \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="f6a35-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="f6a35-104">Función de proxy para el método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) .</span><span class="sxs-lookup"><span data-stu-id="f6a35-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6a35-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6a35-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="f6a35-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6a35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6a35-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f6a35-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6a35-108">Tipo: \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) \** _</span><span class="sxs-lookup"><span data-stu-id="f6a35-108">Type: \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\** _</span></span>

<span data-ttu-id="f6a35-109">Puntero a este objeto [_ *IWICBitmapFlipRotator* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="f6a35-109">Pointer to this [_ *IWICBitmapFlipRotator*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="f6a35-110">*pISource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6a35-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6a35-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="f6a35-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="f6a35-112">Origen del mapa de bits de entrada.</span><span class="sxs-lookup"><span data-stu-id="f6a35-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="f6a35-113">_options \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f6a35-113">_options\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6a35-114">Tipo: **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="f6a35-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="f6a35-115">[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) que se va a voltear o girar la imagen.</span><span class="sxs-lookup"><span data-stu-id="f6a35-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6a35-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6a35-116">Return value</span></span>

<span data-ttu-id="f6a35-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f6a35-117">Type: **HRESULT**</span></span>

<span data-ttu-id="f6a35-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f6a35-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6a35-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6a35-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6a35-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6a35-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f6a35-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6a35-121">Requirements</span></span>



| <span data-ttu-id="f6a35-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6a35-122">Requirement</span></span> | <span data-ttu-id="f6a35-123">Value</span><span class="sxs-lookup"><span data-stu-id="f6a35-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a35-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6a35-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f6a35-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6a35-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f6a35-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6a35-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f6a35-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6a35-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f6a35-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6a35-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6a35-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6a35-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




