---
description: Se produce cuando la selección de tinta dentro del control ha cambiado, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de selección.
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: Evento InkOverlay. SelectionChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997e0c8e9620b0a269ff8cd97ff04aa3abfb1df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707151"
---
# <a name="inkoverlayselectionchanged-event"></a><span data-ttu-id="587f0-103">Evento InkOverlay. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="587f0-103">InkOverlay.SelectionChanged event</span></span>

<span data-ttu-id="587f0-104">Se produce cuando la selección de tinta dentro del control ha cambiado, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="587f0-104">Occurs when the selection of ink within the control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="587f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="587f0-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="587f0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="587f0-106">Parameters</span></span>

<span data-ttu-id="587f0-107">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="587f0-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="587f0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="587f0-108">Return value</span></span>

<span data-ttu-id="587f0-109">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="587f0-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="587f0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="587f0-110">Remarks</span></span>

<span data-ttu-id="587f0-111">No hay datos de evento.</span><span class="sxs-lookup"><span data-stu-id="587f0-111">There are no event data.</span></span>

<span data-ttu-id="587f0-112">Este método de evento se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOESelectionChanged.</span><span class="sxs-lookup"><span data-stu-id="587f0-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="587f0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="587f0-113">Requirements</span></span>



| <span data-ttu-id="587f0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="587f0-114">Requirement</span></span> | <span data-ttu-id="587f0-115">Value</span><span class="sxs-lookup"><span data-stu-id="587f0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="587f0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="587f0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="587f0-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="587f0-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="587f0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="587f0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="587f0-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="587f0-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="587f0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="587f0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="587f0-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="587f0-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="587f0-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="587f0-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="587f0-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="587f0-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="587f0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="587f0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="587f0-125">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="587f0-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="587f0-126">**Selection (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="587f0-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

 




