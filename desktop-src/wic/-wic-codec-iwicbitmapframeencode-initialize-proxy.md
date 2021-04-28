---
description: 'IWICBitmapFrameEncode_Initialize_Proxy función: función de proxy para el método Initialize.'
ms.assetid: af9e204c-7072-47b8-84eb-47a754968d5b
title: IWICBitmapFrameEncode_Initialize_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e8c8a7526343e6dfcda9859fd06259700019a9bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100553"
---
# <a name="iwicbitmapframeencode_initialize_proxy-function"></a><span data-ttu-id="3b411-103">IWICBitmapFrameEncode \_ Initialize \_ Proxy function</span><span class="sxs-lookup"><span data-stu-id="3b411-103">IWICBitmapFrameEncode\_Initialize\_Proxy function</span></span>

<span data-ttu-id="3b411-104">Función de proxy para el [**método Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize)</span><span class="sxs-lookup"><span data-stu-id="3b411-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b411-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b411-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Initialize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IPropertyBag2         *pIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="3b411-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b411-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b411-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="3b411-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b411-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="3b411-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="3b411-109">Puntero a este [**objeto IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="3b411-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="3b411-110">*pIEncoderOptions* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3b411-110">*pIEncoderOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b411-111">Tipo: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="3b411-111">Type: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\***</span></span>

<span data-ttu-id="3b411-112">Conjunto de propiedades que se usarán para [**la inicialización de IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="3b411-112">The set of properties to use for [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b411-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b411-113">Return value</span></span>

<span data-ttu-id="3b411-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3b411-114">Type: **HRESULT**</span></span>

<span data-ttu-id="3b411-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3b411-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b411-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="3b411-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b411-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b411-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3b411-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b411-118">Requirements</span></span>



| <span data-ttu-id="3b411-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b411-119">Requirement</span></span> | <span data-ttu-id="3b411-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3b411-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b411-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b411-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b411-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3b411-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3b411-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b411-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b411-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b411-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3b411-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b411-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b411-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b411-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

