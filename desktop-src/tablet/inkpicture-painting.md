---
description: Se produce antes de que el control InkPicture se vuelva a dibujar.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: Evento InkPicture. Painting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc76bbf3079d61c84ac14d1b22690d645a7cce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277394"
---
# <a name="inkpicturepainting-event"></a><span data-ttu-id="904d9-103">Evento InkPicture. Painting</span><span class="sxs-lookup"><span data-stu-id="904d9-103">InkPicture.Painting event</span></span>

<span data-ttu-id="904d9-104">Se produce antes de que el control [InkPicture](inkpicture-control-reference.md) se vuelva a dibujar.</span><span class="sxs-lookup"><span data-stu-id="904d9-104">Occurs before the [InkPicture](inkpicture-control-reference.md) control redraws itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="904d9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="904d9-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="904d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="904d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="904d9-107">*HDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="904d9-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904d9-108">Contexto de dispositivo en el que se producirá el dibujo.</span><span class="sxs-lookup"><span data-stu-id="904d9-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="904d9-109">*Rectángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="904d9-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904d9-110">Rectángulo de entrada manuscrita que se va a volver a dibujar.</span><span class="sxs-lookup"><span data-stu-id="904d9-110">The ink rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="904d9-111">*Permitir* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="904d9-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="904d9-112">Indica si se debe volver a dibujar.</span><span class="sxs-lookup"><span data-stu-id="904d9-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="904d9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="904d9-113">Return value</span></span>

<span data-ttu-id="904d9-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="904d9-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="904d9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="904d9-115">Remarks</span></span>

<span data-ttu-id="904d9-116">Este método de evento se define en las interfaces de solo envío **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** (dispinterfaces) con un identificador de DISPID \_ IOEPainting.</span><span class="sxs-lookup"><span data-stu-id="904d9-116">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="904d9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="904d9-117">Requirements</span></span>



| <span data-ttu-id="904d9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="904d9-118">Requirement</span></span> | <span data-ttu-id="904d9-119">Value</span><span class="sxs-lookup"><span data-stu-id="904d9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="904d9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="904d9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="904d9-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="904d9-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="904d9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="904d9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="904d9-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="904d9-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="904d9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="904d9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="904d9-125"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="904d9-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="904d9-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="904d9-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="904d9-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="904d9-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="904d9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="904d9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904d9-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="904d9-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




