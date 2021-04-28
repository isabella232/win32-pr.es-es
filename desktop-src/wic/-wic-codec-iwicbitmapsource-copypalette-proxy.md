---
description: 'IWICBitmapSource_CopyPalette_Proxy función: función proxy para el método CopyPalette.'
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: IWICBitmapSource_CopyPalette_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ad9f5096aff7770a0b1624495c5c717440b6bd39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100503"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="9badd-103">Función IWICBitmapSource \_ CopyPalette \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="9badd-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="9badd-104">Función de proxy para [**el método CopyPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)</span><span class="sxs-lookup"><span data-stu-id="9badd-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9badd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9badd-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="9badd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9badd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9badd-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9badd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9badd-108">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="9badd-108">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="9badd-109">Puntero a este [**objeto IWICBitmapSource.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)</span><span class="sxs-lookup"><span data-stu-id="9badd-109">Pointer to this [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="9badd-110">*pIPalette* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9badd-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9badd-111">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="9badd-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="9badd-112">Paleta.</span><span class="sxs-lookup"><span data-stu-id="9badd-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9badd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9badd-113">Return value</span></span>

<span data-ttu-id="9badd-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9badd-114">Type: **HRESULT**</span></span>

<span data-ttu-id="9badd-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9badd-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9badd-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9badd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9badd-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9badd-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9badd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9badd-118">Requirements</span></span>



| <span data-ttu-id="9badd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9badd-119">Requirement</span></span> | <span data-ttu-id="9badd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9badd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9badd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9badd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9badd-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9badd-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9badd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9badd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9badd-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9badd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9badd-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9badd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9badd-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9badd-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




