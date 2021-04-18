---
description: Se produce cuando la posición de la selección actual está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de selección.
ms.assetid: 7cd7a5b1-4ae6-4038-afd0-6ef9d0700938
title: Evento InkOverlay. SelectionMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afc77198a6a7228e44b3f2bad8015c25a939812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706955"
---
# <a name="inkoverlayselectionmoving-event"></a><span data-ttu-id="bac4d-103">Evento InkOverlay. SelectionMoving</span><span class="sxs-lookup"><span data-stu-id="bac4d-103">InkOverlay.SelectionMoving event</span></span>

<span data-ttu-id="bac4d-104">Se produce cuando la posición de la selección actual está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="bac4d-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="bac4d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bac4d-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="bac4d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bac4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bac4d-107">*CurSelectionRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bac4d-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bac4d-108">Rectángulo al que se mueve la selección después del evento **SelectionMoving** .</span><span class="sxs-lookup"><span data-stu-id="bac4d-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="bac4d-109">Este rectángulo se especifica en coordenadas de la ventana del cliente, lo que permite escenarios como el mantenimiento de la relación de aspecto al cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="bac4d-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bac4d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bac4d-110">Return value</span></span>

<span data-ttu-id="bac4d-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="bac4d-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bac4d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bac4d-112">Remarks</span></span>

<span data-ttu-id="bac4d-113">Este método de evento se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOESelectionMoving.</span><span class="sxs-lookup"><span data-stu-id="bac4d-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID off DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="bac4d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bac4d-114">Requirements</span></span>



| <span data-ttu-id="bac4d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bac4d-115">Requirement</span></span> | <span data-ttu-id="bac4d-116">Value</span><span class="sxs-lookup"><span data-stu-id="bac4d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bac4d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bac4d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bac4d-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bac4d-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bac4d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bac4d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bac4d-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bac4d-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="bac4d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bac4d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bac4d-122"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bac4d-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bac4d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bac4d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bac4d-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bac4d-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="bac4d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bac4d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac4d-126">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="bac4d-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="bac4d-127">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="bac4d-127">**InkOverlay Class**</span></span>
</dt> <dt>

[<span data-ttu-id="bac4d-128">**Selection (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="bac4d-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="bac4d-129">**Clase InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="bac4d-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




