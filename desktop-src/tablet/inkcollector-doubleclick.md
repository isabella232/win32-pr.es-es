---
description: 'Evento InkCollector.DoubleClick: se produce cuando se hace doble clic en el objeto InkCollector o InkOverlay.'
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: Evento InkCollector.DoubleClick (Msclickut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51c3fef9ee999bbe2701da64e09a360f07db345
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110213"
---
# <a name="inkcollectordoubleclick-event"></a><span data-ttu-id="d9e63-103">Evento InkCollector.DoubleClick</span><span class="sxs-lookup"><span data-stu-id="d9e63-103">InkCollector.DoubleClick event</span></span>

<span data-ttu-id="d9e63-104">Se produce cuando se hace doble clic en el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay.**](inkoverlay-class.md)</span><span class="sxs-lookup"><span data-stu-id="d9e63-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e63-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9e63-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="d9e63-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9e63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9e63-107">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d9e63-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e63-108">**VARIANT \_ TRUE** para cancelar el evento del control primario; en caso contrario, **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d9e63-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9e63-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9e63-109">Return value</span></span>

<span data-ttu-id="d9e63-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="d9e63-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9e63-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9e63-111">Remarks</span></span>

<span data-ttu-id="d9e63-112">Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IPEDblClick.</span><span class="sxs-lookup"><span data-stu-id="d9e63-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9e63-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9e63-113">Requirements</span></span>



| <span data-ttu-id="d9e63-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9e63-114">Requirement</span></span> | <span data-ttu-id="d9e63-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e63-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9e63-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9e63-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d9e63-117">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="d9e63-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d9e63-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9e63-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d9e63-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d9e63-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d9e63-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9e63-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9e63-121"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="d9e63-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d9e63-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9e63-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9e63-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9e63-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d9e63-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d9e63-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9e63-125">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="d9e63-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> </dl>

 

 




