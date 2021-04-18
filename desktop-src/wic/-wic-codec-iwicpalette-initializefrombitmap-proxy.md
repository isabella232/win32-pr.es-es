---
description: Función de proxy para el método InitializeFromBitmap.
ms.assetid: 9559a56d-7201-4b39-a3cd-9c0e4eac611a
title: IWICPalette_InitializeFromBitmap_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf5e119acf1efca948281a02f61d8954f4e08818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707365"
---
# <a name="iwicpalette_initializefrombitmap_proxy-function"></a><span data-ttu-id="2e5bc-103">IWICPalette \_ InitializeFromBitmap \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="2e5bc-103">IWICPalette\_InitializeFromBitmap\_Proxy function</span></span>

<span data-ttu-id="2e5bc-104">Función de proxy para el método [**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) .</span><span class="sxs-lookup"><span data-stu-id="2e5bc-104">Proxy function for the [**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e5bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e5bc-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromBitmap_Proxy(
  _In_ IWICPalette      *THIS_PTR,
  _In_ IWICBitmapSource *pISurface,
  _In_ UINT             colorCount,
  _In_ BOOL             fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="2e5bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e5bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e5bc-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2e5bc-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e5bc-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="2e5bc-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="2e5bc-109">Puntero a este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="2e5bc-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="2e5bc-110">*pISurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e5bc-110">*pISurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e5bc-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="2e5bc-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="2e5bc-112">Puntero al mapa de bits de origen.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-112">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2e5bc-113">_colorCount \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2e5bc-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e5bc-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2e5bc-114">Type: **UINT**</span></span>

<span data-ttu-id="2e5bc-115">El número de colores con los que inicializar la paleta.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-115">The number of colors to initialize the palette with.</span></span>

</dd> <dt>

<span data-ttu-id="2e5bc-116">*fAddTransparentColor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e5bc-116">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e5bc-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="2e5bc-117">Type: **BOOL**</span></span>

<span data-ttu-id="2e5bc-118">Valor que indica si se va a agregar un color transparente.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-118">A value to indicate whether to add a transparent color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e5bc-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e5bc-119">Return value</span></span>

<span data-ttu-id="2e5bc-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2e5bc-120">Type: **HRESULT**</span></span>

<span data-ttu-id="2e5bc-121">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2e5bc-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e5bc-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e5bc-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e5bc-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e5bc-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2e5bc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e5bc-124">Requirements</span></span>



| <span data-ttu-id="2e5bc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e5bc-125">Requirement</span></span> | <span data-ttu-id="2e5bc-126">Value</span><span class="sxs-lookup"><span data-stu-id="2e5bc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e5bc-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e5bc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e5bc-128">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e5bc-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2e5bc-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e5bc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e5bc-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e5bc-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2e5bc-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e5bc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e5bc-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e5bc-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




