---
description: Se produce cuando se hace doble clic en el objeto InkCollector o InkOverlay.
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: Evento InkOverlay. DoubleClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4baddc89e309b7d64ba2294827b58956b3e6c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278486"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="16472-103">Evento InkOverlay. DoubleClick</span><span class="sxs-lookup"><span data-stu-id="16472-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="16472-104">Se produce cuando se hace doble clic en el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="16472-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="16472-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16472-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="16472-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16472-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16472-107">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="16472-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16472-108">Indica si se debe cancelar el evento para el control primario.</span><span class="sxs-lookup"><span data-stu-id="16472-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16472-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16472-109">Return value</span></span>

<span data-ttu-id="16472-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="16472-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16472-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16472-111">Remarks</span></span>

<span data-ttu-id="16472-112">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ IPEDblClick.</span><span class="sxs-lookup"><span data-stu-id="16472-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="16472-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16472-113">Requirements</span></span>



| <span data-ttu-id="16472-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="16472-114">Requirement</span></span> | <span data-ttu-id="16472-115">Value</span><span class="sxs-lookup"><span data-stu-id="16472-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16472-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16472-116">Minimum supported client</span></span><br/> | <span data-ttu-id="16472-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="16472-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="16472-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16472-118">Minimum supported server</span></span><br/> | <span data-ttu-id="16472-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="16472-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="16472-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16472-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="16472-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="16472-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="16472-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16472-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="16472-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16472-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="16472-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="16472-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16472-125">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="16472-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




