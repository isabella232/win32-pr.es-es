---
title: Mensaje EM_SETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Establece el estado actual de las opciones tipográficas de un control Rich Edit.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- EM_SETTYPOGRAPHYOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996557"
---
# <a name="em_settypographyoptions-message"></a><span data-ttu-id="6708b-104">\_Mensaje SETTYPOGRAPHYOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="6708b-104">EM\_SETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="6708b-105">Establece el estado actual de las opciones tipográficas de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="6708b-105">Sets the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6708b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6708b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6708b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6708b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6708b-108">Especifica uno o ambos de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6708b-108">Specifies one or both of the following values.</span></span>



| <span data-ttu-id="6708b-109">Value</span><span class="sxs-lookup"><span data-stu-id="6708b-109">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="6708b-110">Significado</span><span class="sxs-lookup"><span data-stu-id="6708b-110">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <span data-ttu-id="6708b-111"><dt>**A \_ ADVANCEDTYPOGRAPHY**</dt></span><span class="sxs-lookup"><span data-stu-id="6708b-111"><dt>**TO\_ADVANCEDTYPOGRAPHY** </dt></span></span> </dl> | <span data-ttu-id="6708b-112">El salto de línea y el formato de línea avanzados están activados.</span><span class="sxs-lookup"><span data-stu-id="6708b-112">Advanced line breaking and line formatting is turned on.</span></span> <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <span data-ttu-id="6708b-113"><dt>**a \_ SIMPLELINEBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="6708b-113"><dt>**TO\_SIMPLELINEBREAK**</dt></span></span> </dl>             | <span data-ttu-id="6708b-114">Salto de línea más rápido para texto simple (requiere **\_ ADVANCEDTYPOGRAPHY**).</span><span class="sxs-lookup"><span data-stu-id="6708b-114">Faster line breaking for simple text (requires **TO\_ADVANCEDTYPOGRAPHY**).</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="6708b-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6708b-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6708b-116">Máscara formada por una o varias de las marcas de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="6708b-116">A mask consisting of one or more of the flags in *wParam*.</span></span> <span data-ttu-id="6708b-117">Solo se establecerán o se borrarán las marcas que se establezcan en esta máscara.</span><span class="sxs-lookup"><span data-stu-id="6708b-117">Only the flags that are set in this mask will be set or cleared.</span></span> <span data-ttu-id="6708b-118">Esto permite establecer o borrar una sola marca sin leer los Estados actuales de la marca.</span><span class="sxs-lookup"><span data-stu-id="6708b-118">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6708b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6708b-119">Return value</span></span>

<span data-ttu-id="6708b-120">Devuelve **true** si *wParam* es válido; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6708b-120">Returns **TRUE** if *wParam* is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6708b-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6708b-121">Remarks</span></span>

<span data-ttu-id="6708b-122">El control Rich Edit activa automáticamente el salto de línea avanzado cuando sea necesario, por ejemplo, para administrar scripts complejos como el árabe y el hebreo, y para las matemáticas.</span><span class="sxs-lookup"><span data-stu-id="6708b-122">Advanced line breaking is turned on automatically by the rich edit control when needed, such as for handling complex scripts like Arabic and Hebrew, and for mathematics.</span></span> <span data-ttu-id="6708b-123">También es necesario para párrafos justificados, guiones y otras características tipográficas.</span><span class="sxs-lookup"><span data-stu-id="6708b-123">It s also needed for justified paragraphs, hyphenation, and other typographic features.</span></span>

## <a name="requirements"></a><span data-ttu-id="6708b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6708b-124">Requirements</span></span>



| <span data-ttu-id="6708b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6708b-125">Requirement</span></span> | <span data-ttu-id="6708b-126">Value</span><span class="sxs-lookup"><span data-stu-id="6708b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6708b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6708b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6708b-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6708b-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6708b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6708b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6708b-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6708b-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6708b-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="6708b-131">Redistributable</span></span><br/>          | <span data-ttu-id="6708b-132">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="6708b-132">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="6708b-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6708b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6708b-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6708b-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6708b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="6708b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6708b-136">**\_GETTYPOGRAPHYOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="6708b-136">**EM\_GETTYPOGRAPHYOPTIONS**</span></span>](em-gettypographyoptions.md)
</dt> </dl>

 

 





