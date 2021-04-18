---
description: Se produce cuando ha cambiado la posición de la selección actual, por ejemplo, a través de las modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad de selección.
ms.assetid: 669dc6c2-1620-40f3-b4b5-7ab8967e739a
title: Evento InkPicture. SelectionMoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25810b87d5a0a3554c46b1a3869bb9b6c88d2fb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360974"
---
# <a name="inkpictureselectionmoved-event"></a><span data-ttu-id="25cd2-103">Evento InkPicture. SelectionMoved</span><span class="sxs-lookup"><span data-stu-id="25cd2-103">InkPicture.SelectionMoved event</span></span>

<span data-ttu-id="25cd2-104">Se produce cuando ha cambiado la posición de la selección actual, por ejemplo, a través de las modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="25cd2-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="25cd2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25cd2-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="25cd2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25cd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25cd2-107">*OldSelectionRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25cd2-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25cd2-108">Rectángulo delimitador de la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) seleccionada tal y como existía antes de que se activara el evento **SelectionMoved** .</span><span class="sxs-lookup"><span data-stu-id="25cd2-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="25cd2-109">Este rectángulo se especifica en coordenadas de espacio de tinta, lo que permite escenarios de deshacer.</span><span class="sxs-lookup"><span data-stu-id="25cd2-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25cd2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25cd2-110">Return value</span></span>

<span data-ttu-id="25cd2-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="25cd2-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25cd2-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25cd2-112">Remarks</span></span>

<span data-ttu-id="25cd2-113">Este método de evento se define en las interfaces de solo envío **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** (dispinterfaces) con un identificador de DISPID \_ IOESelectionMoved.</span><span class="sxs-lookup"><span data-stu-id="25cd2-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="25cd2-114">Para obtener el nuevo rectángulo delimitador de la colección de trazos que se han pasado, llame al método [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .</span><span class="sxs-lookup"><span data-stu-id="25cd2-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="25cd2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25cd2-115">Requirements</span></span>



| <span data-ttu-id="25cd2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="25cd2-116">Requirement</span></span> | <span data-ttu-id="25cd2-117">Value</span><span class="sxs-lookup"><span data-stu-id="25cd2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25cd2-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25cd2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25cd2-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="25cd2-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="25cd2-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25cd2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25cd2-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="25cd2-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="25cd2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25cd2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25cd2-123"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="25cd2-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="25cd2-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25cd2-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="25cd2-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25cd2-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="25cd2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="25cd2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25cd2-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="25cd2-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="25cd2-128">[**Propiedad de selección \[ InkPicture (control)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="25cd2-128">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="25cd2-129">**Clase InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="25cd2-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

