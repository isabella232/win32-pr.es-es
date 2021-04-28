---
description: 'IWICBitmapFrameDecode_GetThumbnail_Proxy función: función proxy para el método GetThumbnail.'
ms.assetid: 377f8aac-3cdc-44dc-8c60-9b6bce915486
title: IWICBitmapFrameDecode_GetThumbnail_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7f3c94461ac13aa39d14b97f13fe5e9e8d7569a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113643"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a><span data-ttu-id="7f848-103">IWICBitmapFrameDecode \_ GetThumbnail \_ Proxy function</span><span class="sxs-lookup"><span data-stu-id="7f848-103">IWICBitmapFrameDecode\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="7f848-104">Función de proxy para [**el método GetThumbnail.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)</span><span class="sxs-lookup"><span data-stu-id="7f848-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f848-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f848-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="7f848-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f848-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f848-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7f848-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f848-108">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="7f848-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="7f848-109">Puntero a este [**objeto IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="7f848-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="7f848-110">*ppIThumbnail* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7f848-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f848-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="7f848-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="7f848-112">Puntero que recibe un puntero a [**IWICBitmapSource de**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) la miniatura.</span><span class="sxs-lookup"><span data-stu-id="7f848-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f848-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f848-113">Return value</span></span>

<span data-ttu-id="7f848-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7f848-114">Type: **HRESULT**</span></span>

<span data-ttu-id="7f848-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7f848-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f848-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="7f848-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f848-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f848-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7f848-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f848-118">Requirements</span></span>



| <span data-ttu-id="7f848-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f848-119">Requirement</span></span> | <span data-ttu-id="7f848-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7f848-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f848-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f848-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7f848-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7f848-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7f848-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f848-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7f848-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f848-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7f848-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7f848-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f848-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f848-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




