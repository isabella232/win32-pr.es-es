---
description: Función de proxy para el método commit.
ms.assetid: 605801e5-00f8-4e4f-87d3-ad34d3568ee5
title: IWICBitmapFrameEncode_Commit_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0da0cb95a13148082d8263f622bb4089a7c9bd30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360240"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="20d6c-103">IWICBitmapFrameEncode (función de proxy de \_ confirmación) \_</span><span class="sxs-lookup"><span data-stu-id="20d6c-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="20d6c-104">Función de proxy para el método [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) .</span><span class="sxs-lookup"><span data-stu-id="20d6c-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="20d6c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20d6c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="20d6c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20d6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20d6c-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="20d6c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20d6c-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="20d6c-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="20d6c-109">Puntero a este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="20d6c-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20d6c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20d6c-110">Return value</span></span>

<span data-ttu-id="20d6c-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="20d6c-111">Type: **HRESULT**</span></span>

<span data-ttu-id="20d6c-112">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="20d6c-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="20d6c-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="20d6c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="20d6c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20d6c-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="20d6c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20d6c-115">Requirements</span></span>



| <span data-ttu-id="20d6c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="20d6c-116">Requirement</span></span> | <span data-ttu-id="20d6c-117">Value</span><span class="sxs-lookup"><span data-stu-id="20d6c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d6c-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20d6c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="20d6c-119">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20d6c-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="20d6c-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20d6c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="20d6c-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="20d6c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="20d6c-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="20d6c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20d6c-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20d6c-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




