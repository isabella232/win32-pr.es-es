---
description: Función de proxy para el método SetThumbnail.
ms.assetid: 6c062eaf-27a4-4d48-8315-be9bf168f999
title: IWICBitmapEncoder_SetThumbnail_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d2670dae0d8ba9eeda7ca1d6dce5d3957dc59b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497326"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="8c3b2-103">IWICBitmapEncoder \_ SetThumbnail \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="8c3b2-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="8c3b2-104">Función de proxy para el método [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="8c3b2-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c3b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c3b2-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="8c3b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c3b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c3b2-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8c3b2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3b2-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="8c3b2-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="8c3b2-109">Puntero a este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="8c3b2-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="8c3b2-110">*pIThumbnail* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c3b2-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3b2-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="8c3b2-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="8c3b2-112">[_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que se va a establecer como la miniatura global.</span><span class="sxs-lookup"><span data-stu-id="8c3b2-112">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c3b2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c3b2-113">Return value</span></span>

<span data-ttu-id="8c3b2-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8c3b2-114">Type: **HRESULT**</span></span>

<span data-ttu-id="8c3b2-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8c3b2-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8c3b2-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8c3b2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c3b2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c3b2-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8c3b2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c3b2-118">Requirements</span></span>



| <span data-ttu-id="8c3b2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c3b2-119">Requirement</span></span> | <span data-ttu-id="8c3b2-120">Value</span><span class="sxs-lookup"><span data-stu-id="8c3b2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c3b2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c3b2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8c3b2-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c3b2-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8c3b2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c3b2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8c3b2-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c3b2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8c3b2-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c3b2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c3b2-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c3b2-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




