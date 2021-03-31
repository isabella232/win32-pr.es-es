---
description: Se produce cuando se hace doble clic en el objeto InkCollector o InkOverlay.
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: InkCollector. DoubleClick (evento) (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17faa459e207cd8891a13cf90f587b277d404772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907713"
---
# <a name="inkcollectordoubleclick-event"></a><span data-ttu-id="c707f-103">InkCollector. DoubleClick (evento)</span><span class="sxs-lookup"><span data-stu-id="c707f-103">InkCollector.DoubleClick event</span></span>

<span data-ttu-id="c707f-104">Se produce cuando se hace doble clic en el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c707f-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="c707f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c707f-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="c707f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c707f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c707f-107">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c707f-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c707f-108">**Variante \_ TRUE** para cancelar el evento para el control primario; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="c707f-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c707f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c707f-109">Return value</span></span>

<span data-ttu-id="c707f-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="c707f-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c707f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c707f-111">Remarks</span></span>

<span data-ttu-id="c707f-112">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ IPEDblClick.</span><span class="sxs-lookup"><span data-stu-id="c707f-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="c707f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c707f-113">Requirements</span></span>



| <span data-ttu-id="c707f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c707f-114">Requirement</span></span> | <span data-ttu-id="c707f-115">Value</span><span class="sxs-lookup"><span data-stu-id="c707f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c707f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c707f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c707f-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c707f-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c707f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c707f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c707f-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c707f-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c707f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c707f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c707f-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c707f-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c707f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c707f-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="c707f-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c707f-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c707f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c707f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c707f-125">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="c707f-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> </dl>

 

 




