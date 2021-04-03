---
description: Se produce cuando se cambia el tamaño del control InkPicture (cuando cambian los valores de la propiedad width o height).
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: Evento InkPicture. Resize (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083110"
---
# <a name="inkpictureresize-event"></a><span data-ttu-id="2e276-103">InkPicture. Resize (evento)</span><span class="sxs-lookup"><span data-stu-id="2e276-103">InkPicture.Resize event</span></span>

<span data-ttu-id="2e276-104">Se produce cuando se cambia el tamaño del control [InkPicture](inkpicture-control-reference.md) (cuando cambian los valores de la propiedad width o height).</span><span class="sxs-lookup"><span data-stu-id="2e276-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is resized (when the Width and/or Height property values change).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e276-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e276-105">Syntax</span></span>


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="2e276-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e276-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e276-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="2e276-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="2e276-108">Número de píxeles desde el lado izquierdo de la ventana que contiene el control en el lado izquierdo del control.</span><span class="sxs-lookup"><span data-stu-id="2e276-108">The number of pixels from the left side of the window that contains the control to the left side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2e276-109">*Top* (Principales)</span><span class="sxs-lookup"><span data-stu-id="2e276-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="2e276-110">Número de píxeles desde la parte superior de la ventana que contiene el control hasta la parte superior del control.</span><span class="sxs-lookup"><span data-stu-id="2e276-110">The number of pixels from the top of the window that contains the control to the top of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2e276-111">*Right*</span><span class="sxs-lookup"><span data-stu-id="2e276-111">*Right*</span></span> 
</dt> <dd>

<span data-ttu-id="2e276-112">Número de píxeles desde el lado izquierdo de la ventana que contiene el control que se encuentra a la derecha del control.</span><span class="sxs-lookup"><span data-stu-id="2e276-112">The number of pixels from the left side of the window that contains the control to the right side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2e276-113">*Bottom*</span><span class="sxs-lookup"><span data-stu-id="2e276-113">*Bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="2e276-114">Número de píxeles desde la parte superior de la ventana que contiene el control hasta la parte inferior del control.</span><span class="sxs-lookup"><span data-stu-id="2e276-114">The number of pixels from the top of the window that contains the control to the bottom of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e276-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e276-115">Return value</span></span>

<span data-ttu-id="2e276-116">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="2e276-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e276-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e276-117">Remarks</span></span>

<span data-ttu-id="2e276-118">El nuevo ancho del control en píxeles será igual a la diferencia entre los parámetros *derecho* e *izquierdo* .</span><span class="sxs-lookup"><span data-stu-id="2e276-118">The new width of the control in pixels will be equal to the difference between the *Right* and *Left* parameters.</span></span> <span data-ttu-id="2e276-119">Del mismo modo, el nuevo alto será igual a la diferencia entre la *parte inferior* y *superior*.</span><span class="sxs-lookup"><span data-stu-id="2e276-119">Likewise, the new height will be equal to the difference between *Bottom* and *Top*.</span></span>

<span data-ttu-id="2e276-120">Este método de evento se define en la interfaz **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="2e276-120">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="2e276-121">La interfaz **\_ IInkPictureEvents** implementa la interfaz IDispatch con un identificador de **DISPID \_ IPEResize**.</span><span class="sxs-lookup"><span data-stu-id="2e276-121">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEResize**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e276-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e276-122">Requirements</span></span>



| <span data-ttu-id="2e276-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e276-123">Requirement</span></span> | <span data-ttu-id="2e276-124">Value</span><span class="sxs-lookup"><span data-stu-id="2e276-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e276-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e276-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2e276-126">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2e276-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2e276-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e276-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2e276-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2e276-128">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2e276-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e276-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e276-130"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2e276-130"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2e276-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e276-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e276-132"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e276-132"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2e276-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e276-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e276-134">InkPicture</span><span class="sxs-lookup"><span data-stu-id="2e276-134">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




