---
description: Se produce cuando la posición de la selección actual está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de selección.
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: Evento InkPicture. SelectionMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2dbc0064e22f21faf80d67f51ca1eeb58b6433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083315"
---
# <a name="inkpictureselectionmoving-event"></a><span data-ttu-id="87ac8-103">Evento InkPicture. SelectionMoving</span><span class="sxs-lookup"><span data-stu-id="87ac8-103">InkPicture.SelectionMoving event</span></span>

<span data-ttu-id="87ac8-104">Se produce cuando la posición de la selección actual está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="87ac8-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ac8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87ac8-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="87ac8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87ac8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ac8-107">*CurSelectionRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87ac8-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87ac8-108">Rectángulo al que se mueve la selección después del evento **SelectionMoving** .</span><span class="sxs-lookup"><span data-stu-id="87ac8-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="87ac8-109">Este rectángulo se especifica en coordenadas de la ventana del cliente, lo que permite escenarios como el mantenimiento de la relación de aspecto al cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="87ac8-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ac8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87ac8-110">Return value</span></span>

<span data-ttu-id="87ac8-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="87ac8-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87ac8-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87ac8-112">Remarks</span></span>

<span data-ttu-id="87ac8-113">Este método de evento se define en las interfaces de solo envío **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** (dispinterfaces) con un identificador de DISPID \_ IOESelectionMoving.</span><span class="sxs-lookup"><span data-stu-id="87ac8-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ac8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87ac8-114">Requirements</span></span>



| <span data-ttu-id="87ac8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ac8-115">Requirement</span></span> | <span data-ttu-id="87ac8-116">Value</span><span class="sxs-lookup"><span data-stu-id="87ac8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ac8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87ac8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="87ac8-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="87ac8-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="87ac8-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87ac8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="87ac8-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="87ac8-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="87ac8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87ac8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="87ac8-122"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="87ac8-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="87ac8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87ac8-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="87ac8-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87ac8-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="87ac8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="87ac8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ac8-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="87ac8-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="87ac8-127">[**Propiedad de selección \[ InkPicture (control)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="87ac8-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="87ac8-128">**Clase InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="87ac8-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




