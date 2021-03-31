---
description: Función de proxy para el método Initialize.
ms.assetid: af9e204c-7072-47b8-84eb-47a754968d5b
title: IWICBitmapFrameEncode_Initialize_Proxy función)
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
ms.openlocfilehash: da9192409636de96dbd9d35d9614df2c926c9032
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809565"
---
# <a name="iwicbitmapframeencode_initialize_proxy-function"></a><span data-ttu-id="7886f-103">IWICBitmapFrameEncode \_ inicializar \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="7886f-103">IWICBitmapFrameEncode\_Initialize\_Proxy function</span></span>

<span data-ttu-id="7886f-104">Función de proxy para el método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .</span><span class="sxs-lookup"><span data-stu-id="7886f-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7886f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7886f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Initialize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IPropertyBag2         *pIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="7886f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7886f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7886f-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7886f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7886f-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="7886f-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="7886f-109">Puntero a este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="7886f-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="7886f-110">*pIEncoderOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7886f-110">*pIEncoderOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7886f-111">Tipo: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="7886f-111">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="7886f-112">Conjunto de propiedades que se va a utilizar para la inicialización [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="7886f-112">The set of properties to use for [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7886f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7886f-113">Return value</span></span>

<span data-ttu-id="7886f-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7886f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="7886f-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7886f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7886f-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7886f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7886f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7886f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7886f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7886f-118">Requirements</span></span>



| <span data-ttu-id="7886f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7886f-119">Requirement</span></span> | <span data-ttu-id="7886f-120">Value</span><span class="sxs-lookup"><span data-stu-id="7886f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7886f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7886f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7886f-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7886f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7886f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7886f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7886f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7886f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7886f-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7886f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7886f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7886f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

