---
description: Se produce cuando se eliminan uno o varios trazos de la colección InkStrokes.
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: Evento InkStrokes. StrokesRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86448f9676e07a11effe683ecd883874791ff3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361577"
---
# <a name="inkstrokesstrokesremoved-event"></a><span data-ttu-id="75b14-103">Evento InkStrokes. StrokesRemoved</span><span class="sxs-lookup"><span data-stu-id="75b14-103">InkStrokes.StrokesRemoved event</span></span>

<span data-ttu-id="75b14-104">Se produce cuando se eliminan uno o varios trazos de la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="75b14-104">Occurs when one or more strokes are deleted from the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b14-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75b14-105">Syntax</span></span>


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="75b14-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75b14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b14-107">*StrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="75b14-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b14-108">La matriz de enteros de los identificadores de todos los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) eliminados cuando se produce este evento.</span><span class="sxs-lookup"><span data-stu-id="75b14-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object deleted when this event occurs.</span></span>

<span data-ttu-id="75b14-109">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="75b14-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b14-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75b14-110">Return value</span></span>

<span data-ttu-id="75b14-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="75b14-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75b14-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75b14-112">Remarks</span></span>

<span data-ttu-id="75b14-113">Este método de evento se define en la \_ interfaz IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="75b14-113">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="75b14-114">La \_ interfaz IInkEvents implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ SEStrokesRemoved.</span><span class="sxs-lookup"><span data-stu-id="75b14-114">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b14-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75b14-115">Requirements</span></span>



| <span data-ttu-id="75b14-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="75b14-116">Requirement</span></span> | <span data-ttu-id="75b14-117">Value</span><span class="sxs-lookup"><span data-stu-id="75b14-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75b14-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75b14-118">Minimum supported client</span></span><br/> | <span data-ttu-id="75b14-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="75b14-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="75b14-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75b14-120">Minimum supported server</span></span><br/> | <span data-ttu-id="75b14-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="75b14-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="75b14-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75b14-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="75b14-123"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="75b14-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="75b14-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75b14-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="75b14-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75b14-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="75b14-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="75b14-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="75b14-127">[Colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="75b14-127">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="75b14-128">[**Quitar método \[ InkStrokes colección\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span><span class="sxs-lookup"><span data-stu-id="75b14-128">[**Remove Method \[InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span></span>
</dt> <dt>

[<span data-ttu-id="75b14-129">**Clase InkDisp**</span><span class="sxs-lookup"><span data-stu-id="75b14-129">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> </dl>

 

