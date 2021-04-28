---
description: 'IWICBitmapFrameEncode_SetThumbnail_Proxy función: función proxy para el método SetThumbnail.'
ms.assetid: 3ad473ec-9218-4ed1-961d-a2aa0d542119
title: IWICBitmapFrameEncode_SetThumbnail_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9af9dd2d4f8fe71a6dc94420db17383a5da6da28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116603"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="a0ed7-103">IWICBitmapFrameEncode \_ SetThumbnail \_ Proxy function</span><span class="sxs-lookup"><span data-stu-id="a0ed7-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="a0ed7-104">Función de proxy para [**el método SetThumbnail.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)</span><span class="sxs-lookup"><span data-stu-id="a0ed7-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ed7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0ed7-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="a0ed7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0ed7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0ed7-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a0ed7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ed7-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="a0ed7-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="a0ed7-109">Puntero a este [**objeto IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)</span><span class="sxs-lookup"><span data-stu-id="a0ed7-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="a0ed7-110">*pIThumbnail* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a0ed7-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ed7-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="a0ed7-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="a0ed7-112">Origen de mapa de bits que se usará como miniatura.</span><span class="sxs-lookup"><span data-stu-id="a0ed7-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0ed7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0ed7-113">Return value</span></span>

<span data-ttu-id="a0ed7-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a0ed7-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a0ed7-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a0ed7-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a0ed7-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="a0ed7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0ed7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0ed7-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a0ed7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0ed7-118">Requirements</span></span>



| <span data-ttu-id="a0ed7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0ed7-119">Requirement</span></span> | <span data-ttu-id="a0ed7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a0ed7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ed7-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0ed7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a0ed7-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a0ed7-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a0ed7-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0ed7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a0ed7-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0ed7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a0ed7-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a0ed7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0ed7-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0ed7-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




