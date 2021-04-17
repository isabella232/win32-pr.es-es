---
description: Se produce cuando uno o varios trazos se agregan a la colección InkStrokes.
ms.assetid: d32dcaef-3beb-4ee1-84d6-5944278936f6
title: Evento InkStrokes. StrokesAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a53bf1f511b5809cfb9a6ca0a2f683f0e85540af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716303"
---
# <a name="inkstrokesstrokesadded-event"></a><span data-ttu-id="73985-103">Evento InkStrokes. StrokesAdded</span><span class="sxs-lookup"><span data-stu-id="73985-103">InkStrokes.StrokesAdded event</span></span>

<span data-ttu-id="73985-104">Se produce cuando uno o varios trazos se agregan a la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="73985-104">Occurs when one or more strokes are added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="73985-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73985-105">Syntax</span></span>


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="73985-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73985-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73985-107">*StrokeIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73985-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73985-108">La matriz de enteros de los identificadores de cada objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) agregado cuando se produce este evento.</span><span class="sxs-lookup"><span data-stu-id="73985-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object added when this event occurs.</span></span>

<span data-ttu-id="73985-109">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="73985-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73985-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73985-110">Return value</span></span>

<span data-ttu-id="73985-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="73985-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73985-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73985-112">Remarks</span></span>

<span data-ttu-id="73985-113">Este método de evento se define en la \_ interfaz IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="73985-113">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="73985-114">La \_ interfaz IInkEvents implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ SEStrokesAdded.</span><span class="sxs-lookup"><span data-stu-id="73985-114">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="73985-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73985-115">Requirements</span></span>



| <span data-ttu-id="73985-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="73985-116">Requirement</span></span> | <span data-ttu-id="73985-117">Value</span><span class="sxs-lookup"><span data-stu-id="73985-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73985-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73985-118">Minimum supported client</span></span><br/> | <span data-ttu-id="73985-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="73985-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="73985-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73985-120">Minimum supported server</span></span><br/> | <span data-ttu-id="73985-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="73985-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="73985-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73985-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="73985-123"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="73985-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="73985-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73985-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="73985-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73985-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="73985-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="73985-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="73985-127">[Colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="73985-127">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="73985-128">[**Agregar método \[ InkStrokes colección\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)</span><span class="sxs-lookup"><span data-stu-id="73985-128">[**Add Method \[InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)</span></span>
</dt> <dt>

[<span data-ttu-id="73985-129">**Clase InkDisp**</span><span class="sxs-lookup"><span data-stu-id="73985-129">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> </dl>

 

