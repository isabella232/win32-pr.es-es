---
description: Se produce cuando la selección de entrada de lápiz dentro del control está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de selección.
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: Evento InkOverlay. SelectionChanging (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e830a9ea97f6722dd8ab9bdb782e4ae4ac5f44fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697560"
---
# <a name="inkoverlayselectionchanging-event"></a><span data-ttu-id="22554-103">Evento InkOverlay. SelectionChanging</span><span class="sxs-lookup"><span data-stu-id="22554-103">InkOverlay.SelectionChanging event</span></span>

<span data-ttu-id="22554-104">Se produce cuando la selección de entrada de lápiz dentro del control está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="22554-104">Occurs when the selection of ink within the control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="22554-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22554-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="22554-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22554-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22554-107">*NewSelection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22554-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22554-108">Nueva colección de [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="22554-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22554-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22554-109">Return value</span></span>

<span data-ttu-id="22554-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="22554-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22554-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22554-111">Remarks</span></span>

<span data-ttu-id="22554-112">Este método de evento se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOESelectionChanging.</span><span class="sxs-lookup"><span data-stu-id="22554-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="22554-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22554-113">Requirements</span></span>



| <span data-ttu-id="22554-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="22554-114">Requirement</span></span> | <span data-ttu-id="22554-115">Value</span><span class="sxs-lookup"><span data-stu-id="22554-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22554-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22554-116">Minimum supported client</span></span><br/> | <span data-ttu-id="22554-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="22554-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="22554-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22554-118">Minimum supported server</span></span><br/> | <span data-ttu-id="22554-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="22554-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="22554-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22554-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="22554-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="22554-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="22554-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22554-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="22554-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22554-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="22554-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="22554-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22554-125">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="22554-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="22554-126">**Selection (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="22554-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

