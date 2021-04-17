---
description: Función de proxy para el método SetPalette.
ms.assetid: d8e2c36e-6886-4959-b2a2-469bebfe1cdc
title: IWICBitmapEncoder_SetPalette_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 128953cd56c3bea17ec9761a2acf2b8bc89cacfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541262"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a><span data-ttu-id="bfb73-103">IWICBitmapEncoder \_ SetPalette \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="bfb73-103">IWICBitmapEncoder\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="bfb73-104">Función de proxy para el método [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="bfb73-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfb73-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfb73-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="bfb73-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfb73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfb73-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="bfb73-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfb73-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="bfb73-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="bfb73-109">Puntero a este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="bfb73-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="bfb73-110">*pIPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bfb73-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfb73-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="bfb73-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="bfb73-112">[_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) que se va a usar como paleta global.</span><span class="sxs-lookup"><span data-stu-id="bfb73-112">The [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) to use as the global palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfb73-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfb73-113">Return value</span></span>

<span data-ttu-id="bfb73-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bfb73-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bfb73-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bfb73-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bfb73-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bfb73-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfb73-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfb73-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bfb73-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfb73-118">Requirements</span></span>



| <span data-ttu-id="bfb73-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfb73-119">Requirement</span></span> | <span data-ttu-id="bfb73-120">Value</span><span class="sxs-lookup"><span data-stu-id="bfb73-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb73-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfb73-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bfb73-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bfb73-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bfb73-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfb73-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bfb73-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bfb73-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bfb73-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bfb73-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfb73-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfb73-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




