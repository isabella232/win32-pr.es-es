---
description: Función de proxy para el método GetThumbnail.
ms.assetid: 377f8aac-3cdc-44dc-8c60-9b6bce915486
title: IWICBitmapFrameDecode_GetThumbnail_Proxy función)
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
ms.openlocfilehash: c29b62b4d3839b7cd3db51574f38ab824b215310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705533"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a><span data-ttu-id="c8642-103">Función de proxy de \_ GetThumbnail de IWICBitmapFrameDecode \_</span><span class="sxs-lookup"><span data-stu-id="c8642-103">IWICBitmapFrameDecode\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="c8642-104">Función de proxy para el método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="c8642-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8642-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8642-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="c8642-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8642-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8642-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c8642-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8642-108">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="c8642-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="c8642-109">Puntero a este objeto [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="c8642-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="c8642-110">*ppIThumbnail* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c8642-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8642-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="c8642-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="c8642-112">Puntero que recibe un puntero al [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="c8642-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8642-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8642-113">Return value</span></span>

<span data-ttu-id="c8642-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c8642-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c8642-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c8642-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8642-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8642-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8642-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8642-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c8642-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8642-118">Requirements</span></span>



| <span data-ttu-id="c8642-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8642-119">Requirement</span></span> | <span data-ttu-id="c8642-120">Value</span><span class="sxs-lookup"><span data-stu-id="c8642-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8642-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8642-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c8642-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8642-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c8642-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8642-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c8642-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8642-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c8642-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8642-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8642-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8642-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




