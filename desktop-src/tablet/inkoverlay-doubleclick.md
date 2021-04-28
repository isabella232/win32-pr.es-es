---
description: 'Evento InkOverlay.DoubleClick: se produce cuando se hace doble clic en el objeto InkCollector o InkOverlay.'
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: Evento InkOverlay.DoubleClick (Msclickut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c358a6c44ccda9be9dc4d0dd1d3e81e4a983ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086833"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="8277c-103">Evento InkOverlay.DoubleClick</span><span class="sxs-lookup"><span data-stu-id="8277c-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="8277c-104">Se produce cuando se hace doble clic en el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay.**](inkoverlay-class.md)</span><span class="sxs-lookup"><span data-stu-id="8277c-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="8277c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8277c-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="8277c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8277c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8277c-107">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8277c-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8277c-108">Si el evento se debe cancelar para el control primario.</span><span class="sxs-lookup"><span data-stu-id="8277c-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8277c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8277c-109">Return value</span></span>

<span data-ttu-id="8277c-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="8277c-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8277c-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8277c-111">Remarks</span></span>

<span data-ttu-id="8277c-112">Este método de evento se define en las interfaces de solo distribución \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador de \_ \_ DISPID IPEDblClick.</span><span class="sxs-lookup"><span data-stu-id="8277c-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="8277c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8277c-113">Requirements</span></span>



| <span data-ttu-id="8277c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8277c-114">Requirement</span></span> | <span data-ttu-id="8277c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8277c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8277c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8277c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8277c-117">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="8277c-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8277c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8277c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8277c-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8277c-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8277c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8277c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8277c-121"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="8277c-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8277c-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8277c-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="8277c-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8277c-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8277c-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8277c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8277c-125">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="8277c-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




