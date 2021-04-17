---
description: Función de proxy para el método CreateNewFrame.
ms.assetid: b23e8689-0fdc-49a7-a004-148b50420127
title: IWICBitmapEncoder_CreateNewFrame_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_CreateNewFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0ddf0141e5b13e370f199e3f211e74c3a0e6e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697550"
---
# <a name="iwicbitmapencoder_createnewframe_proxy-function"></a><span data-ttu-id="92aea-103">IWICBitmapEncoder \_ CreateNewFrame \_ proxy, función</span><span class="sxs-lookup"><span data-stu-id="92aea-103">IWICBitmapEncoder\_CreateNewFrame\_Proxy function</span></span>

<span data-ttu-id="92aea-104">Función de proxy para el método [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) .</span><span class="sxs-lookup"><span data-stu-id="92aea-104">Proxy function for the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="92aea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92aea-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_CreateNewFrame_Proxy(
  _In_    IWICBitmapEncoder     *THIS_PTR,
  _Out_   IWICBitmapFrameEncode **ppIFrameEncode,
  _Inout_ IPropertyBag2         **ppIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="92aea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92aea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92aea-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="92aea-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92aea-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="92aea-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="92aea-109">Puntero a este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="92aea-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="92aea-110">*ppIFrameEncode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="92aea-110">*ppIFrameEncode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92aea-111">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span><span class="sxs-lookup"><span data-stu-id="92aea-111">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span></span>

<span data-ttu-id="92aea-112">Puntero que recibe un puntero a la nueva instancia de [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span><span class="sxs-lookup"><span data-stu-id="92aea-112">A pointer that receives a pointer to the new instance of an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span>

</dd> <dt>

<span data-ttu-id="92aea-113">*ppIEncoderOptions* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="92aea-113">*ppIEncoderOptions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="92aea-114">Tipo: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span><span class="sxs-lookup"><span data-stu-id="92aea-114">Type: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span></span>

<span data-ttu-id="92aea-115">Propiedades con nombre que se van a usar para la inicialización del marco.</span><span class="sxs-lookup"><span data-stu-id="92aea-115">The named properties to use for frame initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92aea-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92aea-116">Return value</span></span>

<span data-ttu-id="92aea-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="92aea-117">Type: **HRESULT**</span></span>

<span data-ttu-id="92aea-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="92aea-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="92aea-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="92aea-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="92aea-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92aea-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="92aea-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92aea-121">Requirements</span></span>



| <span data-ttu-id="92aea-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="92aea-122">Requirement</span></span> | <span data-ttu-id="92aea-123">Value</span><span class="sxs-lookup"><span data-stu-id="92aea-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92aea-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92aea-124">Minimum supported client</span></span><br/> | <span data-ttu-id="92aea-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92aea-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="92aea-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92aea-126">Minimum supported server</span></span><br/> | <span data-ttu-id="92aea-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="92aea-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="92aea-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92aea-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92aea-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92aea-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

