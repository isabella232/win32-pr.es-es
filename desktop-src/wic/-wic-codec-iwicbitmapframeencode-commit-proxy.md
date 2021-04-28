---
description: 'IWICBitmapFrameEncode_Commit_Proxy función: función de proxy para el método Commit.'
ms.assetid: 605801e5-00f8-4e4f-87d3-ad34d3568ee5
title: IWICBitmapFrameEncode_Commit_Proxy función
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
ms.openlocfilehash: 0f8ab87860c77cf58f73491a1fb5fc1b658ed67f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091123"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="1d567-103">IWICBitmapFrameEncode \_ Commit \_ Proxy function</span><span class="sxs-lookup"><span data-stu-id="1d567-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="1d567-104">Función de proxy para el [**método Commit.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)</span><span class="sxs-lookup"><span data-stu-id="1d567-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d567-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d567-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="1d567-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d567-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d567-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1d567-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d567-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="1d567-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="1d567-109">Puntero a este [**objeto IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="1d567-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d567-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d567-110">Return value</span></span>

<span data-ttu-id="1d567-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1d567-111">Type: **HRESULT**</span></span>

<span data-ttu-id="1d567-112">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1d567-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d567-113">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="1d567-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d567-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d567-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1d567-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d567-115">Requirements</span></span>



| <span data-ttu-id="1d567-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d567-116">Requirement</span></span> | <span data-ttu-id="1d567-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1d567-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d567-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d567-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1d567-119">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1d567-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1d567-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d567-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1d567-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d567-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1d567-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d567-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d567-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d567-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




