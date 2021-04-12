---
description: Se produce cuando se mueve la rueda del mouse mientras el control InkPicture tiene el foco.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: Evento InkPicture. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cab870f3a00b2aa0cea3c003993e2b35cd2abbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360821"
---
# <a name="inkpicturemousewheel-event"></a><span data-ttu-id="2708c-103">InkPicture. MouseWheel (evento)</span><span class="sxs-lookup"><span data-stu-id="2708c-103">InkPicture.MouseWheel event</span></span>

<span data-ttu-id="2708c-104">Se produce cuando se mueve la rueda del mouse mientras el control [InkPicture](inkpicture-control-reference.md) tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="2708c-104">Occurs when the mouse wheel moves while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="2708c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2708c-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="2708c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2708c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2708c-107">*Botón* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2708c-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2708c-108">Botón que se presionó.</span><span class="sxs-lookup"><span data-stu-id="2708c-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="2708c-109">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2708c-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2708c-110">Estado de la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="2708c-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="2708c-111">*Delta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2708c-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2708c-112">Distancia que ha girado la rueda del mouse.</span><span class="sxs-lookup"><span data-stu-id="2708c-112">The distance that the mouse wheel turned.</span></span>

</dd> <dt>

<span data-ttu-id="2708c-113">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2708c-113">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2708c-114">La coordenada x, en píxeles, del objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="2708c-114">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="2708c-115">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2708c-115">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2708c-116">La coordenada y, en píxeles, del objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="2708c-116">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="2708c-117">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2708c-117">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2708c-118">VARIANT \_ true para cancelar el evento **MouseWheel** del control primario; de lo contrario, Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="2708c-118">VARIANT\_TRUE to cancel the **MouseWheel** event for the parent control; otherwise, VARIANT\_FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2708c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2708c-119">Return value</span></span>

<span data-ttu-id="2708c-120">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="2708c-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2708c-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2708c-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2708c-122">Los parámetros *x* e y se encuentran en píxeles *, y no* las unidades HIMETRIC asociadas con el sistema de coordenadas de espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="2708c-122">The parameters *x* and *y* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="2708c-123">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no es compatible con el lápiz y ese tipo de aplicación solo hace referencia a píxeles.</span><span class="sxs-lookup"><span data-stu-id="2708c-123">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

<span data-ttu-id="2708c-124">Este método de evento se define en la interfaz **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="2708c-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="2708c-125">La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEMouseWheel.</span><span class="sxs-lookup"><span data-stu-id="2708c-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="2708c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2708c-126">Requirements</span></span>



| <span data-ttu-id="2708c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2708c-127">Requirement</span></span> | <span data-ttu-id="2708c-128">Value</span><span class="sxs-lookup"><span data-stu-id="2708c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2708c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2708c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2708c-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2708c-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2708c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2708c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2708c-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2708c-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2708c-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2708c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2708c-134"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2708c-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2708c-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2708c-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="2708c-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2708c-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2708c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="2708c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2708c-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="2708c-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

