---
description: 'Evento InkOverlay.SelectionResizing: se produce cuando el tamaño de la selección actual está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad Selection.'
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: Evento InkOverlay.SelectionResizing (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b5577f83c14ccc2e998fb4257344729e2219a2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086683"
---
# <a name="inkoverlayselectionresizing-event"></a><span data-ttu-id="9adc1-103">Evento InkOverlay.SelectionResizing</span><span class="sxs-lookup"><span data-stu-id="9adc1-103">InkOverlay.SelectionResizing event</span></span>

<span data-ttu-id="9adc1-104">Se produce cuando el tamaño de la selección actual está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)</span><span class="sxs-lookup"><span data-stu-id="9adc1-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9adc1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9adc1-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="9adc1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9adc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9adc1-107">*CurSelectionRect* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9adc1-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9adc1-108">Rectángulo delimitador de la selección después del **evento SelectionResizing.**</span><span class="sxs-lookup"><span data-stu-id="9adc1-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="9adc1-109">Este rectángulo se especifica en coordenadas de ventana de cliente, lo que permite escenarios como mantener la relación de aspecto al cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="9adc1-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9adc1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9adc1-110">Return value</span></span>

<span data-ttu-id="9adc1-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="9adc1-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9adc1-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9adc1-112">Remarks</span></span>

<span data-ttu-id="9adc1-113">Este método de evento se define en las interfaces de solo distribución \_ (dispinterfaces) de IInkOverlayEvents e IInkPictureEvents con un identificador \_ de DISPID \_ IOESelectionResizing.</span><span class="sxs-lookup"><span data-stu-id="9adc1-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="9adc1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9adc1-114">Requirements</span></span>



| <span data-ttu-id="9adc1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9adc1-115">Requirement</span></span> | <span data-ttu-id="9adc1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9adc1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9adc1-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9adc1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9adc1-118">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="9adc1-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9adc1-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9adc1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9adc1-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9adc1-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9adc1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9adc1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9adc1-122"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="9adc1-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9adc1-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9adc1-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9adc1-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9adc1-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9adc1-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9adc1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9adc1-126">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="9adc1-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="9adc1-127">**Propiedad Selection**</span><span class="sxs-lookup"><span data-stu-id="9adc1-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="9adc1-128">**InkRectangle (clase)**</span><span class="sxs-lookup"><span data-stu-id="9adc1-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




