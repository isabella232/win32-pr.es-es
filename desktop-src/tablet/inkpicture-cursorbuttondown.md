---
description: Se produce cuando la clase InkCollector detecta un botón de cursor que está inactivo.
ms.assetid: 9ee2c19e-8a44-428b-a4c1-3c7250dcdeda
title: Evento InkPicture. CursorButtonDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4531f41ce597d9cbb1fa0b8665a1821a8a32dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278480"
---
# <a name="inkpicturecursorbuttondown-event"></a><span data-ttu-id="443cb-103">Evento InkPicture. CursorButtonDown</span><span class="sxs-lookup"><span data-stu-id="443cb-103">InkPicture.CursorButtonDown event</span></span>

<span data-ttu-id="443cb-104">Se produce cuando la [**clase InkCollector**](inkcollector-class.md) detecta un botón de cursor que está inactivo.</span><span class="sxs-lookup"><span data-stu-id="443cb-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="443cb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="443cb-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="443cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="443cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="443cb-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="443cb-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443cb-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **CursorButtonDown** .</span><span class="sxs-lookup"><span data-stu-id="443cb-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="443cb-109">*Botón* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="443cb-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443cb-110">Botón que se presionó.</span><span class="sxs-lookup"><span data-stu-id="443cb-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="443cb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="443cb-111">Return value</span></span>

<span data-ttu-id="443cb-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="443cb-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="443cb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="443cb-113">Remarks</span></span>

<span data-ttu-id="443cb-114">Un botón de la punta del lápiz está inactivo cuando el usuario baja el lápiz al digitalizador y comienza a trazar un trazo.</span><span class="sxs-lookup"><span data-stu-id="443cb-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="443cb-115">Cuando se presiona el botón, un botón de un barril está inactivo.</span><span class="sxs-lookup"><span data-stu-id="443cb-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="443cb-116">Al presionar el botón secundario del mouse, en realidad recibe dos eventos **CursorButtonDown** : uno para el botón derecho presionado y otro para el botón primario presionado.</span><span class="sxs-lookup"><span data-stu-id="443cb-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="443cb-117">Este método de evento se define en la interfaz de solo envío (dispinterfaces) **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** con el identificador DISPID \_ ICECursorButtonDown.</span><span class="sxs-lookup"><span data-stu-id="443cb-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interface (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="443cb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="443cb-118">Requirements</span></span>



| <span data-ttu-id="443cb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="443cb-119">Requirement</span></span> | <span data-ttu-id="443cb-120">Value</span><span class="sxs-lookup"><span data-stu-id="443cb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="443cb-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="443cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="443cb-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="443cb-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="443cb-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="443cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="443cb-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="443cb-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="443cb-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="443cb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="443cb-126"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="443cb-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="443cb-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="443cb-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="443cb-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="443cb-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="443cb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="443cb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443cb-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="443cb-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="443cb-131">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="443cb-131">**CursorDown Event**</span></span>](inkpicture-cursordown.md)
</dt> <dt>

[<span data-ttu-id="443cb-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="443cb-132">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="443cb-133">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="443cb-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="443cb-134">**Interfaz IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="443cb-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




