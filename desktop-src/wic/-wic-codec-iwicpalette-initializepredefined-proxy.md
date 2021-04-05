---
description: Función de proxy para el método InitializePredefined.
ms.assetid: 78137d43-c32f-4d60-b289-2e2154cf4d1e
title: IWICPalette_InitializePredefined_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializePredefined_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d65202d9d7800763e15f52ef0eb03b16bc348e78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816822"
---
# <a name="iwicpalette_initializepredefined_proxy-function"></a><span data-ttu-id="f2dd1-103">IWICPalette \_ InitializePredefined \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="f2dd1-103">IWICPalette\_InitializePredefined\_Proxy function</span></span>

<span data-ttu-id="f2dd1-104">Función de proxy para el método [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) .</span><span class="sxs-lookup"><span data-stu-id="f2dd1-104">Proxy function for the [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2dd1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2dd1-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializePredefined_Proxy(
  _In_ IWICPalette          *THIS_PTR,
  _In_ WICBitmapPaletteType ePaletteType,
  _In_ BOOL                 fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="f2dd1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2dd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2dd1-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f2dd1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dd1-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="f2dd1-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="f2dd1-109">Puntero a este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="f2dd1-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="f2dd1-110">*ePaletteType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2dd1-110">*ePaletteType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dd1-111">Tipo: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="f2dd1-111">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="f2dd1-112">El tipo de paleta predefinida deseado.</span><span class="sxs-lookup"><span data-stu-id="f2dd1-112">The desired pre-defined palette type.</span></span>

</dd> <dt>

<span data-ttu-id="f2dd1-113">*fAddTransparentColor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2dd1-113">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2dd1-114">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="f2dd1-114">Type: **BOOL**</span></span>

<span data-ttu-id="f2dd1-115">Color de Tranparent opcional que se va a agregar a la paleta.</span><span class="sxs-lookup"><span data-stu-id="f2dd1-115">The optional tranparent color to add to the palette.</span></span> <span data-ttu-id="f2dd1-116">Si no se necesita ningún color transparente, use 0.</span><span class="sxs-lookup"><span data-stu-id="f2dd1-116">If no transparent color is needed, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2dd1-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2dd1-117">Return value</span></span>

<span data-ttu-id="f2dd1-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f2dd1-118">Type: **HRESULT**</span></span>

<span data-ttu-id="f2dd1-119">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f2dd1-119">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f2dd1-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2dd1-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2dd1-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2dd1-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f2dd1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2dd1-122">Requirements</span></span>



| <span data-ttu-id="f2dd1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2dd1-123">Requirement</span></span> | <span data-ttu-id="f2dd1-124">Value</span><span class="sxs-lookup"><span data-stu-id="f2dd1-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2dd1-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2dd1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f2dd1-126">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2dd1-126">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f2dd1-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2dd1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f2dd1-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2dd1-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f2dd1-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2dd1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2dd1-130"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2dd1-130"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




