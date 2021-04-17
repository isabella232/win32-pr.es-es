---
description: Se produce cuando el control InkPicture ha terminado de volver a dibujarse.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: Evento InkPicture. pintado (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716304"
---
# <a name="inkpicturepainted-event"></a><span data-ttu-id="7af20-103">InkPicture. pintado (evento)</span><span class="sxs-lookup"><span data-stu-id="7af20-103">InkPicture.Painted event</span></span>

<span data-ttu-id="7af20-104">Se produce cuando el control [InkPicture](inkpicture-control-reference.md) ha terminado de volver a dibujarse.</span><span class="sxs-lookup"><span data-stu-id="7af20-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="7af20-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7af20-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="7af20-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7af20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af20-107">*HDC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7af20-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7af20-108">Contexto de dispositivo en el que se produjo el evento.</span><span class="sxs-lookup"><span data-stu-id="7af20-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="7af20-109">*Rectángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7af20-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7af20-110">[**InkRectangle**](inkrectangle-class.md) que se ha repintado.</span><span class="sxs-lookup"><span data-stu-id="7af20-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af20-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7af20-111">Return value</span></span>

<span data-ttu-id="7af20-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="7af20-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af20-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7af20-113">Remarks</span></span>

<span data-ttu-id="7af20-114">Este método de evento se define en las interfaces dispinterface **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** con un identificador de DISPID \_ IOEPainted.</span><span class="sxs-lookup"><span data-stu-id="7af20-114">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af20-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7af20-115">Requirements</span></span>



| <span data-ttu-id="7af20-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7af20-116">Requirement</span></span> | <span data-ttu-id="7af20-117">Value</span><span class="sxs-lookup"><span data-stu-id="7af20-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7af20-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7af20-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7af20-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7af20-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7af20-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7af20-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7af20-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7af20-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7af20-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7af20-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7af20-123"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7af20-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7af20-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7af20-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="7af20-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7af20-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7af20-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7af20-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af20-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="7af20-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




