---
description: Se produce después de cambiar el tamaño del control InkPicture, en concreto, después de que cambie el valor de la propiedad width o height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Evento InkPicture. SizeChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002882"
---
# <a name="inkpicturesizechanged-event"></a><span data-ttu-id="0aa30-103">Evento InkPicture. SizeChanged</span><span class="sxs-lookup"><span data-stu-id="0aa30-103">InkPicture.SizeChanged event</span></span>

<span data-ttu-id="0aa30-104">Se produce después de cambiar el tamaño del control [InkPicture](inkpicture-control-reference.md) , en concreto, después de que cambie el valor de la propiedad [**width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) o [**height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .</span><span class="sxs-lookup"><span data-stu-id="0aa30-104">Occurs after the [InkPicture](inkpicture-control-reference.md) control has been resized, specifically, after the [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) or [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) property value changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa30-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0aa30-105">Syntax</span></span>


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="0aa30-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0aa30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa30-107">*Izquierda* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aa30-107">*Left* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa30-108">Coordenada x del lado izquierdo del control [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="0aa30-108">The x-coordinate of the left side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="0aa30-109">*Parte superior* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aa30-109">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa30-110">Coordenada y de la parte superior del control [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="0aa30-110">The y-coordinate of the top of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="0aa30-111">*Derecha* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aa30-111">*Right* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa30-112">Coordenada x del lado derecho del control [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="0aa30-112">The x-coordinate of the right side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="0aa30-113">*Inferior* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aa30-113">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa30-114">Coordenada y de la parte inferior del control [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="0aa30-114">The y-coordinate of the bottom of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa30-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0aa30-115">Return value</span></span>

<span data-ttu-id="0aa30-116">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="0aa30-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aa30-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0aa30-117">Remarks</span></span>

<span data-ttu-id="0aa30-118">Este método de evento se define en la interfaz **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="0aa30-118">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="0aa30-119">La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPESizeChanged.</span><span class="sxs-lookup"><span data-stu-id="0aa30-119">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa30-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aa30-120">Requirements</span></span>



| <span data-ttu-id="0aa30-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa30-121">Requirement</span></span> | <span data-ttu-id="0aa30-122">Value</span><span class="sxs-lookup"><span data-stu-id="0aa30-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa30-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0aa30-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa30-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0aa30-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0aa30-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0aa30-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa30-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0aa30-126">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0aa30-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0aa30-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa30-128"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0aa30-128"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0aa30-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0aa30-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0aa30-130"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aa30-130"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0aa30-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0aa30-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa30-132">InkPicture</span><span class="sxs-lookup"><span data-stu-id="0aa30-132">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

