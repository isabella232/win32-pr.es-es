---
title: Estados del botón de la barra de herramientas (CommCtrl. h)
description: En esta sección se enumeran los Estados que puede tener un botón de la barra de herramientas.
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649769"
---
# <a name="toolbar-button-states"></a><span data-ttu-id="bd571-103">Estados del botón de la barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="bd571-103">Toolbar Button States</span></span>

<span data-ttu-id="bd571-104">En esta sección se enumeran los Estados que puede tener un botón de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bd571-104">This section lists the states a toolbar button can have.</span></span>



| <span data-ttu-id="bd571-105">Constante</span><span class="sxs-lookup"><span data-stu-id="bd571-105">Constant</span></span>                                                                                                                                                                              | <span data-ttu-id="bd571-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd571-106">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <span data-ttu-id="bd571-107"><dt>**TBSTATE \_ activado**</dt></span><span class="sxs-lookup"><span data-stu-id="bd571-107"><dt>**TBSTATE\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="bd571-108">El botón tiene el estilo de [**\_ comprobación TBSTYLE**](toolbar-control-and-button-styles.md) y se está haciendo clic en él.</span><span class="sxs-lookup"><span data-stu-id="bd571-108">The button has the [**TBSTYLE\_CHECK**](toolbar-control-and-button-styles.md) style and is being clicked.</span></span><br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <span data-ttu-id="bd571-109"><dt>**TBSTATE \_ puntos suspensivos**</dt></span><span class="sxs-lookup"><span data-stu-id="bd571-109"><dt>**TBSTATE\_ELLIPSES**</dt></span></span> </dl>                | <span data-ttu-id="bd571-110">[Versión 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="bd571-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="bd571-111">El texto del botón se corta y se muestran puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="bd571-111">The button's text is cut off and an ellipsis is displayed.</span></span><br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <span data-ttu-id="bd571-112"><dt>**TBSTATE \_ habilitado**</dt></span><span class="sxs-lookup"><span data-stu-id="bd571-112"><dt>**TBSTATE\_ENABLED**</dt></span></span> </dl>                   | <span data-ttu-id="bd571-113">El botón acepta los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="bd571-113">The button accepts user input.</span></span> <span data-ttu-id="bd571-114">Un botón que no tiene este estado está atenuado.</span><span class="sxs-lookup"><span data-stu-id="bd571-114">A button that does not have this state is grayed.</span></span><br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <span data-ttu-id="bd571-115"><dt>**TBSTATE \_ oculto**</dt></span><span class="sxs-lookup"><span data-stu-id="bd571-115"><dt>**TBSTATE\_HIDDEN**</dt></span></span> </dl>                      | <span data-ttu-id="bd571-116">El botón no está visible y no puede recibir datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="bd571-116">The button is not visible and cannot receive user input.</span></span><br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <span data-ttu-id="bd571-117"><dt>**TBSTATE \_ indeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="bd571-117"><dt>**TBSTATE\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="bd571-118">El botón está atenuado.</span><span class="sxs-lookup"><span data-stu-id="bd571-118">The button is grayed.</span></span><br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <span data-ttu-id="bd571-119"><dt>**TBSTATE \_ marcados**</dt></span><span class="sxs-lookup"><span data-stu-id="bd571-119"><dt>**TBSTATE\_MARKED**</dt></span></span> </dl>                      | <span data-ttu-id="bd571-120">[Versión 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="bd571-120">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="bd571-121">El botón está marcado como.</span><span class="sxs-lookup"><span data-stu-id="bd571-121">The button is marked.</span></span> <span data-ttu-id="bd571-122">La interpretación de un elemento marcado depende de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bd571-122">The interpretation of a marked item is dependent upon the application.</span></span> <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <span data-ttu-id="bd571-123"><dt>**TBSTATE \_ presionado**</dt></span><span class="sxs-lookup"><span data-stu-id="bd571-123"><dt>**TBSTATE\_PRESSED**</dt></span></span> </dl>                   | <span data-ttu-id="bd571-124">Se está haciendo clic en el botón.</span><span class="sxs-lookup"><span data-stu-id="bd571-124">The button is being clicked.</span></span><br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <span data-ttu-id="bd571-125"><dt>**TBSTATE \_ Wrap**</dt></span><span class="sxs-lookup"><span data-stu-id="bd571-125"><dt>**TBSTATE\_WRAP**</dt></span></span> </dl>                            | <span data-ttu-id="bd571-126">El botón va seguido de un salto de línea.</span><span class="sxs-lookup"><span data-stu-id="bd571-126">The button is followed by a line break.</span></span> <span data-ttu-id="bd571-127">El botón también debe tener el \_ estado habilitado de TBSTATE.</span><span class="sxs-lookup"><span data-stu-id="bd571-127">The button must also have the TBSTATE\_ENABLED state.</span></span><br/>                                              |



## <a name="remarks"></a><span data-ttu-id="bd571-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd571-128">Remarks</span></span>

<span data-ttu-id="bd571-129">Una barra de herramientas puede tener una combinación de Estados.</span><span class="sxs-lookup"><span data-stu-id="bd571-129">A toolbar may have a combination of states.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd571-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd571-130">Requirements</span></span>



| <span data-ttu-id="bd571-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd571-131">Requirement</span></span> | <span data-ttu-id="bd571-132">Value</span><span class="sxs-lookup"><span data-stu-id="bd571-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd571-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd571-133">Header</span></span><br/> | <dl> <span data-ttu-id="bd571-134"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd571-134"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





