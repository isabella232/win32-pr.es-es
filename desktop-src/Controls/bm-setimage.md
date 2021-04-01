---
title: Mensaje de BM_SETIMAGE (Winuser. h)
description: Asocia una nueva imagen (icono o mapa de bits) al botón.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- BM_SETIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d083c4fb509d51eb017bb7d3d38fab07b4c006
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150020"
---
# <a name="bm_setimage-message"></a><span data-ttu-id="118f8-104">Mensaje de el SETIMAGE de BM \_</span><span class="sxs-lookup"><span data-stu-id="118f8-104">BM\_SETIMAGE message</span></span>

<span data-ttu-id="118f8-105">Asocia una nueva imagen (icono o mapa de bits) al botón.</span><span class="sxs-lookup"><span data-stu-id="118f8-105">Associates a new image (icon or bitmap) with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="118f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="118f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="118f8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="118f8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="118f8-108">Tipo de imagen que se va a asociar al botón.</span><span class="sxs-lookup"><span data-stu-id="118f8-108">The type of image to associate with the button.</span></span> <span data-ttu-id="118f8-109">Este parámetro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="118f8-109">This parameter can be one of the following values:</span></span>

-   <span data-ttu-id="118f8-110">mapa de bits de imagen \_</span><span class="sxs-lookup"><span data-stu-id="118f8-110">IMAGE\_BITMAP</span></span>
-   <span data-ttu-id="118f8-111">icono de imagen \_</span><span class="sxs-lookup"><span data-stu-id="118f8-111">IMAGE\_ICON</span></span>

</dd> <dt>

<span data-ttu-id="118f8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="118f8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="118f8-113">Identificador (**HICON** o **hBitmap**) de la imagen que se va a asociar al botón.</span><span class="sxs-lookup"><span data-stu-id="118f8-113">A handle (**HICON** or **HBITMAP**) to the image to associate with the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="118f8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="118f8-114">Return value</span></span>

<span data-ttu-id="118f8-115">El valor devuelto es un identificador de la imagen asociada previamente al botón, si existe; de lo contrario, es **null**.</span><span class="sxs-lookup"><span data-stu-id="118f8-115">The return value is a handle to the image previously associated with the button, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="118f8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="118f8-116">Remarks</span></span>

<span data-ttu-id="118f8-117">La apariencia del texto, un icono o ambos en un control de botón depende del [**\_ icono de BS**](button-styles.md) y de los estilos de [**mapa de \_ bits BS**](button-styles.md) , y de si se llama al mensaje de el **\_ SETIMAGE de BM** .</span><span class="sxs-lookup"><span data-stu-id="118f8-117">The appearance of text, an icon, or both on a button control depends on the [**BS\_ICON**](button-styles.md) and [**BS\_BITMAP**](button-styles.md) styles, and whether the **BM\_SETIMAGE** message is called.</span></span> <span data-ttu-id="118f8-118">Los resultados posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="118f8-118">The possible results are as follows:</span></span>



| <span data-ttu-id="118f8-119">\_¿Icono de BS \_ o conjunto de mapas de bits BS?</span><span class="sxs-lookup"><span data-stu-id="118f8-119">BS\_ICON or BS\_BITMAP Set?</span></span> | <span data-ttu-id="118f8-120">Se \_ llamó a la BM SETIMAGE?</span><span class="sxs-lookup"><span data-stu-id="118f8-120">BM\_SETIMAGE Called?</span></span> | <span data-ttu-id="118f8-121">Resultado</span><span class="sxs-lookup"><span data-stu-id="118f8-121">Result</span></span>              |
|-----------------------------|----------------------|---------------------|
| <span data-ttu-id="118f8-122">Sí</span><span class="sxs-lookup"><span data-stu-id="118f8-122">Yes</span></span>                         | <span data-ttu-id="118f8-123">Sí</span><span class="sxs-lookup"><span data-stu-id="118f8-123">Yes</span></span>                  | <span data-ttu-id="118f8-124">Mostrar solo el icono.</span><span class="sxs-lookup"><span data-stu-id="118f8-124">Show icon only.</span></span>     |
| <span data-ttu-id="118f8-125">No</span><span class="sxs-lookup"><span data-stu-id="118f8-125">No</span></span>                          | <span data-ttu-id="118f8-126">Sí</span><span class="sxs-lookup"><span data-stu-id="118f8-126">Yes</span></span>                  | <span data-ttu-id="118f8-127">Mostrar el icono y el texto.</span><span class="sxs-lookup"><span data-stu-id="118f8-127">Show icon and text.</span></span> |
| <span data-ttu-id="118f8-128">Sí</span><span class="sxs-lookup"><span data-stu-id="118f8-128">Yes</span></span>                         | <span data-ttu-id="118f8-129">No</span><span class="sxs-lookup"><span data-stu-id="118f8-129">No</span></span>                   | <span data-ttu-id="118f8-130">Mostrar solo texto.</span><span class="sxs-lookup"><span data-stu-id="118f8-130">Show text only.</span></span>     |
| <span data-ttu-id="118f8-131">No</span><span class="sxs-lookup"><span data-stu-id="118f8-131">No</span></span>                          | <span data-ttu-id="118f8-132">No</span><span class="sxs-lookup"><span data-stu-id="118f8-132">No</span></span>                   | <span data-ttu-id="118f8-133">Mostrar solo texto</span><span class="sxs-lookup"><span data-stu-id="118f8-133">Show text only</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="118f8-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="118f8-134">Requirements</span></span>



| <span data-ttu-id="118f8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="118f8-135">Requirement</span></span> | <span data-ttu-id="118f8-136">Value</span><span class="sxs-lookup"><span data-stu-id="118f8-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="118f8-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="118f8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="118f8-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="118f8-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="118f8-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="118f8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="118f8-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="118f8-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="118f8-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="118f8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="118f8-142"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="118f8-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="118f8-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="118f8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="118f8-144">**BM \_ de BM**</span><span class="sxs-lookup"><span data-stu-id="118f8-144">**BM\_GETIMAGE**</span></span>](bm-getimage.md)
</dt> </dl>

 

 





