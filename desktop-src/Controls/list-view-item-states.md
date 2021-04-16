---
title: List-View Estados de elemento (CommCtrl. h)
description: El valor de estado de un elemento consta del estado del elemento, un índice de máscara de superposición opcional y un índice de máscara de imagen de estado opcional.
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649796"
---
# <a name="list-view-item-states"></a><span data-ttu-id="3ba40-103">List-View Estados de elemento</span><span class="sxs-lookup"><span data-stu-id="3ba40-103">List-View Item States</span></span>

<span data-ttu-id="3ba40-104">El valor de estado de un elemento consta del estado del elemento, un índice de máscara de superposición opcional y un índice de máscara de imagen de estado opcional.</span><span class="sxs-lookup"><span data-stu-id="3ba40-104">An item's state value consists of the item's state, an optional overlay mask index, and an optional state image mask index.</span></span>

<span data-ttu-id="3ba40-105">El estado de un elemento determina su apariencia y funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="3ba40-105">An item's state determines its appearance and functionality.</span></span> <span data-ttu-id="3ba40-106">El estado puede ser cero o uno o varios de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="3ba40-106">The state can be zero or one or more of the following values:</span></span>



| <span data-ttu-id="3ba40-107">Constante</span><span class="sxs-lookup"><span data-stu-id="3ba40-107">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="3ba40-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ba40-108">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <span data-ttu-id="3ba40-109"><dt>**activación de LVIS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3ba40-109"><dt>**LVIS\_ACTIVATING**</dt></span></span> </dl>             | <span data-ttu-id="3ba40-110">No se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="3ba40-110">Not currently supported.</span></span><br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="3ba40-111"><dt>**LVIS \_ cortar**</dt></span><span class="sxs-lookup"><span data-stu-id="3ba40-111"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="3ba40-112">El elemento está marcado para una operación de cortar y pegar.</span><span class="sxs-lookup"><span data-stu-id="3ba40-112">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="3ba40-113"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="3ba40-113"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="3ba40-114">El elemento se resalta como un destino de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="3ba40-114">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="3ba40-115"><dt>**LVIS \_ centrado**</dt></span><span class="sxs-lookup"><span data-stu-id="3ba40-115"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="3ba40-116">El elemento tiene el foco, por lo que está rodeado por un rectángulo de foco estándar.</span><span class="sxs-lookup"><span data-stu-id="3ba40-116">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="3ba40-117">Aunque se puede seleccionar más de un elemento, solo un elemento puede tener el foco.</span><span class="sxs-lookup"><span data-stu-id="3ba40-117">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="3ba40-118"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="3ba40-118"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="3ba40-119">Una máscara recupera el índice de la imagen de superposición del elemento.</span><span class="sxs-lookup"><span data-stu-id="3ba40-119">The item's overlay image index is retrieved by a mask.</span></span><br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="3ba40-120"><dt>**LVIS \_ seleccionado**</dt></span><span class="sxs-lookup"><span data-stu-id="3ba40-120"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="3ba40-121">El elemento está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="3ba40-121">The item is selected.</span></span> <span data-ttu-id="3ba40-122">La apariencia de un elemento seleccionado depende de si tiene el foco y también de los colores del sistema utilizados para la selección.</span><span class="sxs-lookup"><span data-stu-id="3ba40-122">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="3ba40-123"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="3ba40-123"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="3ba40-124">Una máscara recupera el índice de la imagen de estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="3ba40-124">The item's state image index is retrieved by a mask.</span></span><br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="3ba40-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ba40-125">Remarks</span></span>

<span data-ttu-id="3ba40-126">Puede usar la **LVIS \_ OVERLAYMASK** Mask para aislar el índice basado en uno de la imagen de superposición.</span><span class="sxs-lookup"><span data-stu-id="3ba40-126">You can use the **LVIS\_OVERLAYMASK** mask to isolate the one-based index of the overlay image.</span></span> <span data-ttu-id="3ba40-127">Puede usar la máscara **\_ STATEIMAGEMASK de LVIS** para aislar el índice basado en uno de la imagen de estado.</span><span class="sxs-lookup"><span data-stu-id="3ba40-127">You can use the **LVIS\_STATEIMAGEMASK** mask to isolate the one-based index of the state image.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba40-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ba40-128">Requirements</span></span>



| <span data-ttu-id="3ba40-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ba40-129">Requirement</span></span> | <span data-ttu-id="3ba40-130">Value</span><span class="sxs-lookup"><span data-stu-id="3ba40-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba40-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ba40-131">Header</span></span><br/> | <dl> <span data-ttu-id="3ba40-132"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ba40-132"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





