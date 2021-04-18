---
description: Función de proxy para el método SetColorContexts.
ms.assetid: 985ae179-df59-42a0-9987-5dd863512e57
title: IWICBitmapFrameEncode_SetColorContexts_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8a960873340c15772113a3f1553a9b6e16c44338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705531"
---
# <a name="iwicbitmapframeencode_setcolorcontexts_proxy-function"></a><span data-ttu-id="01ed0-103">IWICBitmapFrameEncode \_ SetColorContexts, \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="01ed0-103">IWICBitmapFrameEncode\_SetColorContexts\_Proxy function</span></span>

<span data-ttu-id="01ed0-104">Función de proxy para el método [**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) .</span><span class="sxs-lookup"><span data-stu-id="01ed0-104">Proxy function for the [**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="01ed0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01ed0-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetColorContexts_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  cCount,
  _In_ IWICColorContext      **ppIColorContext
);
```



## <a name="parameters"></a><span data-ttu-id="01ed0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01ed0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01ed0-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="01ed0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01ed0-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="01ed0-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="01ed0-109">Puntero a este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="01ed0-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="01ed0-110">*enta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01ed0-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01ed0-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="01ed0-111">Type: **UINT**</span></span>

<span data-ttu-id="01ed0-112">El número de perfiles de [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="01ed0-112">The number of [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) profiles to set.</span></span>

</dd> <dt>

<span data-ttu-id="01ed0-113">*ppIColorContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01ed0-113">*ppIColorContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01ed0-114">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="01ed0-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="01ed0-115">Un puntero a un puntero [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) que contiene los perfiles de los contextos de color que se van a establecer en el marco.</span><span class="sxs-lookup"><span data-stu-id="01ed0-115">A pointer to an [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) pointer containing the color contexts profiles to set to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01ed0-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01ed0-116">Return value</span></span>

<span data-ttu-id="01ed0-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="01ed0-117">Type: **HRESULT**</span></span>

<span data-ttu-id="01ed0-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="01ed0-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01ed0-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01ed0-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="01ed0-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01ed0-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="01ed0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01ed0-121">Requirements</span></span>



| <span data-ttu-id="01ed0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="01ed0-122">Requirement</span></span> | <span data-ttu-id="01ed0-123">Value</span><span class="sxs-lookup"><span data-stu-id="01ed0-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01ed0-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01ed0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="01ed0-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01ed0-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="01ed0-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01ed0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="01ed0-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="01ed0-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="01ed0-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01ed0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01ed0-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01ed0-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




