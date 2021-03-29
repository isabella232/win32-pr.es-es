---
description: Función de proxy para el método GetFrame.
ms.assetid: 31612afa-5017-4ddb-bdf8-25555db35da5
title: IWICBitmapDecoder_GetFrame_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 996c0f412aafe6063e25a346552f9c257a51eed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360244"
---
# <a name="iwicbitmapdecoder_getframe_proxy-function"></a><span data-ttu-id="9e17d-103">IWICBitmapDecoder \_ GetFrame \_ proxy (función)</span><span class="sxs-lookup"><span data-stu-id="9e17d-103">IWICBitmapDecoder\_GetFrame\_Proxy function</span></span>

<span data-ttu-id="9e17d-104">Función de proxy para el método [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) .</span><span class="sxs-lookup"><span data-stu-id="9e17d-104">Proxy function for the [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e17d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e17d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrame_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _In_  UINT                  index,
  _Out_ IWICBitmapFrameDecode **ppIBitmapFrame
);
```



## <a name="parameters"></a><span data-ttu-id="9e17d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e17d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e17d-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9e17d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e17d-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="9e17d-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="9e17d-109">Puntero a este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="9e17d-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="9e17d-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9e17d-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e17d-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9e17d-111">Type: **UINT**</span></span>

<span data-ttu-id="9e17d-112">Marco concreto que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="9e17d-112">The particular frame to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9e17d-113">*ppIBitmapFrame* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9e17d-113">*ppIBitmapFrame* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e17d-114">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span><span class="sxs-lookup"><span data-stu-id="9e17d-114">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\*\***</span></span>

<span data-ttu-id="9e17d-115">Puntero que recibe un puntero al [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span><span class="sxs-lookup"><span data-stu-id="9e17d-115">A pointer that receives a pointer to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e17d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e17d-116">Return value</span></span>

<span data-ttu-id="9e17d-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9e17d-117">Type: **HRESULT**</span></span>

<span data-ttu-id="9e17d-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9e17d-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e17d-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e17d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e17d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e17d-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9e17d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e17d-121">Requirements</span></span>



| <span data-ttu-id="9e17d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e17d-122">Requirement</span></span> | <span data-ttu-id="9e17d-123">Value</span><span class="sxs-lookup"><span data-stu-id="9e17d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e17d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e17d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9e17d-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e17d-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9e17d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e17d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9e17d-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e17d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9e17d-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e17d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e17d-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e17d-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




