---
description: 'Evento InkOverlay.SelectionResized: se produce cuando el tamaño de la selección actual ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad Selection.'
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: Evento InkOverlay.SelectionResized (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f3dd3cf1bdda004733dde99bb66150710044310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116883"
---
# <a name="inkoverlayselectionresized-event"></a><span data-ttu-id="a172a-103">Evento InkOverlay.SelectionResized</span><span class="sxs-lookup"><span data-stu-id="a172a-103">InkOverlay.SelectionResized event</span></span>

<span data-ttu-id="a172a-104">Se produce cuando el tamaño de la selección actual ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)</span><span class="sxs-lookup"><span data-stu-id="a172a-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a172a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a172a-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="a172a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a172a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a172a-107">*OldSelectionRect* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a172a-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a172a-108">Rectángulo delimitador de la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) seleccionada tal como existía antes de que se desencadenase el **evento SelectionResized.**</span><span class="sxs-lookup"><span data-stu-id="a172a-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="a172a-109">Este rectángulo se especifica en coordenadas de espacio de entrada manuscrita, lo que permite escenarios de deshacer.</span><span class="sxs-lookup"><span data-stu-id="a172a-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a172a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a172a-110">Return value</span></span>

<span data-ttu-id="a172a-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a172a-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a172a-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a172a-112">Remarks</span></span>

<span data-ttu-id="a172a-113">Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkOverlayEvents e IInkPictureEvents con un identificador de DISPID \_ IOESelectionResized.</span><span class="sxs-lookup"><span data-stu-id="a172a-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="a172a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a172a-114">Requirements</span></span>



| <span data-ttu-id="a172a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a172a-115">Requirement</span></span> | <span data-ttu-id="a172a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a172a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a172a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a172a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a172a-118">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="a172a-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a172a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a172a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a172a-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a172a-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a172a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a172a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a172a-122"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="a172a-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a172a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a172a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a172a-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a172a-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a172a-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a172a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a172a-126">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="a172a-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="a172a-127">**Propiedad Selection**</span><span class="sxs-lookup"><span data-stu-id="a172a-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="a172a-128">**InkRectangle (clase)**</span><span class="sxs-lookup"><span data-stu-id="a172a-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

