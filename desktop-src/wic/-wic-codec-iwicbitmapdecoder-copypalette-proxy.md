---
description: 'IWICBitmapDecoder_CopyPalette_Proxy función: función de proxy para el método CopyPalette.'
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: IWICBitmapDecoder_CopyPalette_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56dbc523fe29ef9cc958b6ffbd80509284b78b88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086363"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="fa06a-103">Función \_ CopyPalette Proxy de IWICBitmapDecoder \_</span><span class="sxs-lookup"><span data-stu-id="fa06a-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="fa06a-104">Función de proxy para [**el método CopyPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)</span><span class="sxs-lookup"><span data-stu-id="fa06a-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa06a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa06a-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="fa06a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa06a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa06a-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="fa06a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa06a-108">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="fa06a-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="fa06a-109">Puntero a este [**objeto IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)</span><span class="sxs-lookup"><span data-stu-id="fa06a-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="fa06a-110">*pIPalette* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fa06a-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa06a-111">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="fa06a-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="fa06a-112">Paleta de imágenes que se copiará.</span><span class="sxs-lookup"><span data-stu-id="fa06a-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa06a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa06a-113">Return value</span></span>

<span data-ttu-id="fa06a-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fa06a-114">Type: **HRESULT**</span></span>

<span data-ttu-id="fa06a-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fa06a-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa06a-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="fa06a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa06a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa06a-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fa06a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa06a-118">Requirements</span></span>



| <span data-ttu-id="fa06a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa06a-119">Requirement</span></span> | <span data-ttu-id="fa06a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fa06a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa06a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa06a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fa06a-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fa06a-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="fa06a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa06a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fa06a-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa06a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="fa06a-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa06a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa06a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa06a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




