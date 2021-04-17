---
description: Se produce cuando el puntero del mouse se mueve sobre el control InkPicture y se suelta un botón del mouse.
ms.assetid: 5e49acc8-1ce1-45ff-b87c-04bdc653156a
title: Evento InkPicture. MouseUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf652e1ad4110afb4819e5326a5a19a894a310a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716309"
---
# <a name="inkpicturemouseup-event"></a><span data-ttu-id="da786-103">Evento InkPicture. MouseUp</span><span class="sxs-lookup"><span data-stu-id="da786-103">InkPicture.MouseUp event</span></span>

<span data-ttu-id="da786-104">Se produce cuando el puntero del mouse se mueve sobre el control [InkPicture](inkpicture-control-reference.md) y se suelta un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="da786-104">Occurs when the mouse pointer is moved over the [InkPicture](inkpicture-control-reference.md) control and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="da786-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da786-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="da786-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da786-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da786-107">*Botón* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="da786-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da786-108">Botón que se presionó.</span><span class="sxs-lookup"><span data-stu-id="da786-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="da786-109">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da786-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da786-110">Estado de la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="da786-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="da786-111">*PX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da786-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da786-112">La coordenada x, en píxeles, del objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="da786-112">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="da786-113">*py* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da786-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da786-114">La coordenada y, en píxeles, del objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="da786-114">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="da786-115">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="da786-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="da786-116">**Variante \_ TRUE** para cancelar el evento MouseUp del control primario; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="da786-116">**VARIANT\_TRUE** to cancel the MouseUp event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da786-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da786-117">Return value</span></span>

<span data-ttu-id="da786-118">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="da786-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da786-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da786-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="da786-120">Los parámetros *PX* y *py* se encuentran en píxeles, y no las unidades HIMETRIC asociadas con el sistema de coordenadas de espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="da786-120">The parameters *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="da786-121">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no es compatible con el lápiz y ese tipo de aplicación solo hace referencia a píxeles.</span><span class="sxs-lookup"><span data-stu-id="da786-121">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

> [!Caution]  
> <span data-ttu-id="da786-122">Algunos controles dependen de una relación específica entre los eventos [**MouseDown**](inkpicture-mousedown.md), [**MouseMove**](inkpicture-mousemove.md)y **MouseUp** .</span><span class="sxs-lookup"><span data-stu-id="da786-122">Some controls rely on a specific relationship between [**MouseDown**](inkpicture-mousedown.md), [**MouseMove**](inkpicture-mousemove.md), and **MouseUp** events.</span></span> <span data-ttu-id="da786-123">La cancelación de algunos de estos eventos puede tener resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="da786-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="da786-124">Este método de evento se define en la interfaz **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="da786-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="da786-125">La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEMouseDown.</span><span class="sxs-lookup"><span data-stu-id="da786-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="da786-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da786-126">Requirements</span></span>



| <span data-ttu-id="da786-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="da786-127">Requirement</span></span> | <span data-ttu-id="da786-128">Value</span><span class="sxs-lookup"><span data-stu-id="da786-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da786-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da786-129">Minimum supported client</span></span><br/> | <span data-ttu-id="da786-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="da786-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="da786-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da786-131">Minimum supported server</span></span><br/> | <span data-ttu-id="da786-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="da786-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="da786-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da786-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="da786-134"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="da786-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="da786-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="da786-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="da786-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da786-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="da786-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="da786-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da786-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="da786-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

