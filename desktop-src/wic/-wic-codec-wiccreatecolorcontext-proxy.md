---
description: Función de proxy para crear un IWICColorContext.
ms.assetid: 66348ef2-3056-4ec7-84ad-6e022e320a33
title: WICCreateColorContext_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorContext_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e4861bb1ccb275edc38163335e0da5d26441a334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706486"
---
# <a name="wiccreatecolorcontext_proxy-function"></a><span data-ttu-id="408c1-103">\_Función de proxy WICCreateColorContext</span><span class="sxs-lookup"><span data-stu-id="408c1-103">WICCreateColorContext\_Proxy function</span></span>

<span data-ttu-id="408c1-104">Función de proxy para crear un [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="408c1-104">Proxy function for creating an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

## <a name="syntax"></a><span data-ttu-id="408c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="408c1-105">Syntax</span></span>


```C++
HRESULT WICCreateColorContext_Proxy(
  _In_ IWICImagingFactory *THIS_PTR,
       IWICColorContext   ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="408c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="408c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="408c1-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="408c1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="408c1-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="408c1-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

<span data-ttu-id="408c1-109">Puntero a este objeto [_ *IWICImagingFactory* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) .</span><span class="sxs-lookup"><span data-stu-id="408c1-109">Pointer to this [_ *IWICImagingFactory*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="408c1-110">*ppIColorContext*</span><span class="sxs-lookup"><span data-stu-id="408c1-110">*ppIColorContext*</span></span> 
</dt> <dd>

<span data-ttu-id="408c1-111">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span><span class="sxs-lookup"><span data-stu-id="408c1-111">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="408c1-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="408c1-112">Return value</span></span>

<span data-ttu-id="408c1-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="408c1-113">Type: **HRESULT**</span></span>

<span data-ttu-id="408c1-114">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="408c1-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="408c1-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="408c1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="408c1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="408c1-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="408c1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="408c1-117">Requirements</span></span>



| <span data-ttu-id="408c1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="408c1-118">Requirement</span></span> | <span data-ttu-id="408c1-119">Value</span><span class="sxs-lookup"><span data-stu-id="408c1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="408c1-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="408c1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="408c1-121">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="408c1-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="408c1-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="408c1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="408c1-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="408c1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="408c1-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="408c1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="408c1-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="408c1-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




