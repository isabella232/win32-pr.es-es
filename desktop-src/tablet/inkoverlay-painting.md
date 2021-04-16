---
description: Se produce antes de que el objeto InkOverlay o el InkPicture hayan terminado de volver a dibujarse.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: Evento InkOverlay. Painting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546563"
---
# <a name="inkoverlaypainting-event"></a><span data-ttu-id="64d48-103">Evento InkOverlay. Painting</span><span class="sxs-lookup"><span data-stu-id="64d48-103">InkOverlay.Painting event</span></span>

<span data-ttu-id="64d48-104">Se produce antes de que el objeto [**InkOverlay**](inkoverlay-class.md) o el [InkPicture](inkpicture-control-reference.md) hayan terminado de volver a dibujarse.</span><span class="sxs-lookup"><span data-stu-id="64d48-104">Occurs before the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d48-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64d48-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="64d48-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64d48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d48-107">*HDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64d48-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d48-108">Contexto de dispositivo en el que se producirá el dibujo.</span><span class="sxs-lookup"><span data-stu-id="64d48-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="64d48-109">*Rectángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64d48-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d48-110">Rectángulo que se va a volver a dibujar.</span><span class="sxs-lookup"><span data-stu-id="64d48-110">The rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="64d48-111">*Permitir* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="64d48-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="64d48-112">Indica si se debe volver a dibujar.</span><span class="sxs-lookup"><span data-stu-id="64d48-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d48-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64d48-113">Return value</span></span>

<span data-ttu-id="64d48-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="64d48-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64d48-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64d48-115">Remarks</span></span>

<span data-ttu-id="64d48-116">Este método de evento se define en las \_ \_ interfaces de solo envío IInkOverlayEvents y IInkPictureEvents (dispinterfaces) con un identificador de DISPID \_ IOEPainting.</span><span class="sxs-lookup"><span data-stu-id="64d48-116">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d48-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64d48-117">Requirements</span></span>



| <span data-ttu-id="64d48-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="64d48-118">Requirement</span></span> | <span data-ttu-id="64d48-119">Value</span><span class="sxs-lookup"><span data-stu-id="64d48-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d48-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64d48-120">Minimum supported client</span></span><br/> | <span data-ttu-id="64d48-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="64d48-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="64d48-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64d48-122">Minimum supported server</span></span><br/> | <span data-ttu-id="64d48-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="64d48-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="64d48-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64d48-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="64d48-125"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="64d48-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="64d48-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="64d48-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="64d48-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64d48-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="64d48-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="64d48-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d48-129">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="64d48-129">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




