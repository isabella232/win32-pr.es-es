---
description: 'IWICBitmapEncoder_Initialize_Proxy función: función de proxy para el método Initialize.'
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: IWICBitmapEncoder_Initialize_Proxy función
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
ms.openlocfilehash: d346d1379ae92f19a530c65daff07cb98b2e0e50
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100623"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a><span data-ttu-id="36a19-103">IWICBitmapEncoder \_ Initialize \_ Proxy function</span><span class="sxs-lookup"><span data-stu-id="36a19-103">IWICBitmapEncoder\_Initialize\_Proxy function</span></span>

<span data-ttu-id="36a19-104">Función de proxy para el [**método Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)</span><span class="sxs-lookup"><span data-stu-id="36a19-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="36a19-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36a19-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a><span data-ttu-id="36a19-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36a19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36a19-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="36a19-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36a19-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="36a19-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="36a19-109">Puntero a este [**objeto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="36a19-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="36a19-110">*pIStream* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="36a19-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36a19-111">Tipo: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***</span><span class="sxs-lookup"><span data-stu-id="36a19-111">Type: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***</span></span>

<span data-ttu-id="36a19-112">Secuencia de salida.</span><span class="sxs-lookup"><span data-stu-id="36a19-112">The output stream.</span></span>

</dd> <dt>

<span data-ttu-id="36a19-113">*cacheOption* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="36a19-113">*cacheOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36a19-114">Tipo: **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span><span class="sxs-lookup"><span data-stu-id="36a19-114">Type: **[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span></span>

<span data-ttu-id="36a19-115">[**WICBitmapEncoderCacheOption usado**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) en la inicialización.</span><span class="sxs-lookup"><span data-stu-id="36a19-115">The [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) used on initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36a19-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36a19-116">Return value</span></span>

<span data-ttu-id="36a19-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="36a19-117">Type: **HRESULT**</span></span>

<span data-ttu-id="36a19-118">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="36a19-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="36a19-119">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="36a19-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="36a19-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36a19-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="36a19-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36a19-121">Requirements</span></span>



| <span data-ttu-id="36a19-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="36a19-122">Requirement</span></span> | <span data-ttu-id="36a19-123">Valor</span><span class="sxs-lookup"><span data-stu-id="36a19-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36a19-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36a19-124">Minimum supported client</span></span><br/> | <span data-ttu-id="36a19-125">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="36a19-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="36a19-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36a19-126">Minimum supported server</span></span><br/> | <span data-ttu-id="36a19-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="36a19-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="36a19-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="36a19-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36a19-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="36a19-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

