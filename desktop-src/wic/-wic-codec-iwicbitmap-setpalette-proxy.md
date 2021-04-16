---
description: Función de proxy para el método SetPalette.
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: IWICBitmap_SetPalette_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d683dda81d52818bfc7d878d044af9b4e09869b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541278"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="cc485-103">IWICBitmap \_ SetPalette \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="cc485-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="cc485-104">Función de proxy para el método [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="cc485-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc485-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc485-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="cc485-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc485-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc485-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="cc485-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc485-108">Tipo: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="cc485-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="cc485-109">Puntero a este objeto [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="cc485-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="cc485-110">*pIPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc485-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc485-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="cc485-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="cc485-112">Paleta que se va a usar para la conversión.</span><span class="sxs-lookup"><span data-stu-id="cc485-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc485-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc485-113">Return value</span></span>

<span data-ttu-id="cc485-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="cc485-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="cc485-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="cc485-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc485-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc485-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc485-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc485-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cc485-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc485-118">Requirements</span></span>



| <span data-ttu-id="cc485-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc485-119">Requirement</span></span> | <span data-ttu-id="cc485-120">Value</span><span class="sxs-lookup"><span data-stu-id="cc485-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc485-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc485-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cc485-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc485-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cc485-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc485-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cc485-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc485-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cc485-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc485-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc485-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc485-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




