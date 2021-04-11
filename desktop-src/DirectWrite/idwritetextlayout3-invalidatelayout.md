---
title: IDWriteTextLayout3 InvalidateLayout, método
description: Invalida el diseño, forzando el diseño para que se remedie antes de llamar a las métricas o funciones de dibujo. Esto resulta útil si el emplazamiento de una fuente cambia y el diseño debe volver a dibujarse, o si el tamaño de un cliente implementa IDWriteInlineObject cambios.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Método InvalidateLayout de escritura directa
- Método InvalidateLayout de escritura directa, interfaz IDWriteTextLayout3
- Interfaz IDWriteTextLayout3 Direct Write, método InvalidateLayout
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5df97d4590f62f586a570d52428b6560a7d88df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150527"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a><span data-ttu-id="c8c7c-107">IDWriteTextLayout3:: InvalidateLayout (método)</span><span class="sxs-lookup"><span data-stu-id="c8c7c-107">IDWriteTextLayout3::InvalidateLayout method</span></span>

<span data-ttu-id="c8c7c-108">Invalida el diseño, forzando el diseño para que se remedie antes de llamar a las métricas o funciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c8c7c-108">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="c8c7c-109">Esto resulta útil si el emplazamiento de una fuente cambia y el diseño debe volver a dibujarse, o si el tamaño de un cliente implementa IDWriteInlineObject cambios.</span><span class="sxs-lookup"><span data-stu-id="c8c7c-109">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c7c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8c7c-110">Syntax</span></span>


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a><span data-ttu-id="c8c7c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8c7c-111">Parameters</span></span>

<span data-ttu-id="c8c7c-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c8c7c-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8c7c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8c7c-113">Return value</span></span>

<span data-ttu-id="c8c7c-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c8c7c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8c7c-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8c7c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8c7c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8c7c-116">Requirements</span></span>



| <span data-ttu-id="c8c7c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8c7c-117">Requirement</span></span> | <span data-ttu-id="c8c7c-118">Value</span><span class="sxs-lookup"><span data-stu-id="c8c7c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c7c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8c7c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c8c7c-120">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="c8c7c-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c8c7c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8c7c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c8c7c-122">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8c7c-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c8c7c-123">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8c7c-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="c8c7c-124">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="c8c7c-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="c8c7c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8c7c-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c8c7c-126"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8c7c-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c8c7c-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8c7c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8c7c-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8c7c-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8c7c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8c7c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8c7c-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="c8c7c-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





