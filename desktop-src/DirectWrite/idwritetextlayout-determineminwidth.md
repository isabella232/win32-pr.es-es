---
title: IDWriteTextLayout DetermineMinWidth, método
description: Determina el ancho mínimo posible con el que se puede establecer el diseño sin interrumpir la emergencia entre los caracteres de palabras completas que se están produciendo.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Método DetermineMinWidth de escritura directa
- Método DetermineMinWidth de escritura directa, interfaz IDWriteTextLayout
- Interfaz IDWriteTextLayout Direct Write, método DetermineMinWidth
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690602"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a><span data-ttu-id="7eae7-106">IDWriteTextLayout::D método etermineMinWidth</span><span class="sxs-lookup"><span data-stu-id="7eae7-106">IDWriteTextLayout::DetermineMinWidth method</span></span>

<span data-ttu-id="7eae7-107">Determina el ancho mínimo posible con el que se puede establecer el diseño sin interrumpir la emergencia entre los caracteres de palabras completas que se están produciendo.</span><span class="sxs-lookup"><span data-stu-id="7eae7-107">Determines the minimum possible width the layout can be set to without emergency breaking between the characters of whole words occurring.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eae7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7eae7-108">Syntax</span></span>


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="7eae7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7eae7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eae7-110">*minWidth* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7eae7-110">*minWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7eae7-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="7eae7-111">Type: **FLOAT\***</span></span>

<span data-ttu-id="7eae7-112">Ancho mínimo.</span><span class="sxs-lookup"><span data-stu-id="7eae7-112">Minimum width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eae7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7eae7-113">Return value</span></span>

<span data-ttu-id="7eae7-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7eae7-114">Type: **HRESULT**</span></span>

<span data-ttu-id="7eae7-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7eae7-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7eae7-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7eae7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eae7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eae7-117">Requirements</span></span>



| <span data-ttu-id="7eae7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eae7-118">Requirement</span></span> | <span data-ttu-id="7eae7-119">Value</span><span class="sxs-lookup"><span data-stu-id="7eae7-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7eae7-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7eae7-120">Library</span></span><br/> | <dl> <span data-ttu-id="7eae7-121"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7eae7-121"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="7eae7-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7eae7-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7eae7-123"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eae7-123"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eae7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7eae7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eae7-125">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="7eae7-125">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="7eae7-126">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="7eae7-126">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

