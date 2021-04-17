---
description: Función de proxy para el método Initialize.
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: IWICBitmapEncoder_Initialize_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c1a2e684059b75e41c1d89e2d3dd5379cc208b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697506"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a><span data-ttu-id="1bb4b-103">IWICBitmapEncoder \_ inicializar \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="1bb4b-103">IWICBitmapEncoder\_Initialize\_Proxy function</span></span>

<span data-ttu-id="1bb4b-104">Función de proxy para el método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) .</span><span class="sxs-lookup"><span data-stu-id="1bb4b-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bb4b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1bb4b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a><span data-ttu-id="1bb4b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1bb4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bb4b-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1bb4b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb4b-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="1bb4b-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="1bb4b-109">Puntero a este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="1bb4b-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="1bb4b-110">*pIStream* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1bb4b-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb4b-111">Tipo: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="1bb4b-111">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="1bb4b-112">Secuencia de salida.</span><span class="sxs-lookup"><span data-stu-id="1bb4b-112">The output stream.</span></span>

</dd> <dt>

<span data-ttu-id="1bb4b-113">_cacheOption \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1bb4b-113">_cacheOption\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb4b-114">Tipo: **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span><span class="sxs-lookup"><span data-stu-id="1bb4b-114">Type: **[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span></span>

<span data-ttu-id="1bb4b-115">[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) que se usa en la inicialización.</span><span class="sxs-lookup"><span data-stu-id="1bb4b-115">The [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) used on initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bb4b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1bb4b-116">Return value</span></span>

<span data-ttu-id="1bb4b-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1bb4b-117">Type: **HRESULT**</span></span>

<span data-ttu-id="1bb4b-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1bb4b-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1bb4b-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1bb4b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bb4b-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1bb4b-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1bb4b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bb4b-121">Requirements</span></span>



| <span data-ttu-id="1bb4b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bb4b-122">Requirement</span></span> | <span data-ttu-id="1bb4b-123">Value</span><span class="sxs-lookup"><span data-stu-id="1bb4b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bb4b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1bb4b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1bb4b-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1bb4b-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1bb4b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1bb4b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1bb4b-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1bb4b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1bb4b-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1bb4b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bb4b-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bb4b-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

