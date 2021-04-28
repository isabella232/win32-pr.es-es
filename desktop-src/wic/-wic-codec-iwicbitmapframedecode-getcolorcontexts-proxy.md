---
description: 'IWICBitmapFrameDecode_GetColorContexts_Proxy función: función proxy para el método GetColorContexts.'
ms.assetid: 1925a64e-558d-4931-a3c3-b35d2b92a292
title: IWICBitmapFrameDecode_GetColorContexts_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 99fb6caa9b9e654be0adc1235cad0e79a7fa1ef3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100583"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a><span data-ttu-id="c6b92-103">IWICBitmapFrameDecode \_ GetColorContexts \_ Proxy function</span><span class="sxs-lookup"><span data-stu-id="c6b92-103">IWICBitmapFrameDecode\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="c6b92-104">Función de proxy para [**el método GetColorContexts.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)</span><span class="sxs-lookup"><span data-stu-id="c6b92-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6b92-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6b92-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="c6b92-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6b92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6b92-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c6b92-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6b92-108">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="c6b92-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="c6b92-109">Puntero a este [**objeto IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)</span><span class="sxs-lookup"><span data-stu-id="c6b92-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="c6b92-110">*cCount* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c6b92-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6b92-111">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="c6b92-111">Type: **UINT**</span></span>

<span data-ttu-id="c6b92-112">Número de contextos de color que se recuperarán.</span><span class="sxs-lookup"><span data-stu-id="c6b92-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="c6b92-113">Este valor debe ser el tamaño de o menor que el tamaño disponible para *ppIColorContexts.*</span><span class="sxs-lookup"><span data-stu-id="c6b92-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="c6b92-114">*ppIColorContexts* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c6b92-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6b92-115">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="c6b92-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="c6b92-116">Puntero que recibe un puntero a los [**objetos IWICColorContext.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)</span><span class="sxs-lookup"><span data-stu-id="c6b92-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects.</span></span>

</dd> <dt>

<span data-ttu-id="c6b92-117">*pcActualCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c6b92-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6b92-118">Tipo: **UINT \***</span><span class="sxs-lookup"><span data-stu-id="c6b92-118">Type: **UINT\***</span></span>

<span data-ttu-id="c6b92-119">Puntero que recibe el número de contextos de color contenidos en el marco de imagen.</span><span class="sxs-lookup"><span data-stu-id="c6b92-119">A pointer that receives the number of color contexts contained in the image frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6b92-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6b92-120">Return value</span></span>

<span data-ttu-id="c6b92-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c6b92-121">Type: **HRESULT**</span></span>

<span data-ttu-id="c6b92-122">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c6b92-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6b92-123">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c6b92-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6b92-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6b92-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b92-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6b92-125">Requirements</span></span>



| <span data-ttu-id="c6b92-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6b92-126">Requirement</span></span> | <span data-ttu-id="c6b92-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c6b92-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b92-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6b92-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b92-129">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c6b92-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c6b92-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6b92-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b92-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6b92-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c6b92-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6b92-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6b92-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6b92-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




