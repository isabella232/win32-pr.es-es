---
description: Se produce cuando ha cambiado la posición de la selección actual, por ejemplo, a través de las modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad de selección.
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: Evento InkOverlay. SelectionMoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f254b5e3ae3c23f50b12c097608946aad3b3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361332"
---
# <a name="inkoverlayselectionmoved-event"></a><span data-ttu-id="140a7-103">Evento InkOverlay. SelectionMoved</span><span class="sxs-lookup"><span data-stu-id="140a7-103">InkOverlay.SelectionMoved event</span></span>

<span data-ttu-id="140a7-104">Se produce cuando ha cambiado la posición de la selección actual, por ejemplo, a través de las modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="140a7-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="140a7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="140a7-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="140a7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="140a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="140a7-107">*OldSelectionRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="140a7-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="140a7-108">Rectángulo delimitador de la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) seleccionada tal y como existía antes de que se activara el evento **SelectionMoved** .</span><span class="sxs-lookup"><span data-stu-id="140a7-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="140a7-109">Este rectángulo se especifica en coordenadas de espacio de tinta, lo que permite escenarios de deshacer.</span><span class="sxs-lookup"><span data-stu-id="140a7-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="140a7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="140a7-110">Return value</span></span>

<span data-ttu-id="140a7-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="140a7-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="140a7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="140a7-112">Remarks</span></span>

<span data-ttu-id="140a7-113">El método de evento de Basic se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOESelectionMoved.</span><span class="sxs-lookup"><span data-stu-id="140a7-113">TThis event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="140a7-114">Para obtener el nuevo rectángulo delimitador de la colección de trazos que se han pasado, llame al método [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .</span><span class="sxs-lookup"><span data-stu-id="140a7-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="140a7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="140a7-115">Requirements</span></span>



| <span data-ttu-id="140a7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="140a7-116">Requirement</span></span> | <span data-ttu-id="140a7-117">Value</span><span class="sxs-lookup"><span data-stu-id="140a7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="140a7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="140a7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="140a7-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="140a7-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="140a7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="140a7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="140a7-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="140a7-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="140a7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="140a7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="140a7-123"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="140a7-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="140a7-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="140a7-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="140a7-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="140a7-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="140a7-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="140a7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140a7-127">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="140a7-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="140a7-128">**Selection (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="140a7-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="140a7-129">**Clase InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="140a7-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

