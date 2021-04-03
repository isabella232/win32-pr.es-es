---
description: Se produce cuando se presiona una tecla y en la posición hacia abajo mientras el control InkPicture tiene el foco.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: Evento InkPicture. KeyDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5d6bd3555aeec98ac28555c1674dfef32ecc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083452"
---
# <a name="inkpicturekeydown-event"></a><span data-ttu-id="54a56-103">Evento InkPicture. KeyDown</span><span class="sxs-lookup"><span data-stu-id="54a56-103">InkPicture.KeyDown event</span></span>

<span data-ttu-id="54a56-104">Se produce cuando se presiona una tecla y en la posición hacia abajo mientras el control [InkPicture](inkpicture-control-reference.md) tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="54a56-104">Occurs when a key is pressed and in the down position while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="54a56-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54a56-105">Syntax</span></span>


```C++
void KeyDown(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a><span data-ttu-id="54a56-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54a56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54a56-107">*KeyCode* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="54a56-107">*KeyCode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54a56-108">Valor ASCII de la tecla que se va a presionar.</span><span class="sxs-lookup"><span data-stu-id="54a56-108">The ASCII value of the key that is being pressed.</span></span>

</dd> <dt>

<span data-ttu-id="54a56-109">*Desplazamiento* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="54a56-109">*Shift* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54a56-110">Estado de la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="54a56-110">The state of the SHIFT key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54a56-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54a56-111">Return value</span></span>

<span data-ttu-id="54a56-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="54a56-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54a56-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54a56-113">Remarks</span></span>

<span data-ttu-id="54a56-114">Este método de evento se define en la interfaz **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="54a56-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="54a56-115">La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEKeyDown.</span><span class="sxs-lookup"><span data-stu-id="54a56-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="54a56-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54a56-116">Requirements</span></span>



| <span data-ttu-id="54a56-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="54a56-117">Requirement</span></span> | <span data-ttu-id="54a56-118">Value</span><span class="sxs-lookup"><span data-stu-id="54a56-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54a56-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54a56-119">Minimum supported client</span></span><br/> | <span data-ttu-id="54a56-120">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="54a56-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="54a56-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54a56-121">Minimum supported server</span></span><br/> | <span data-ttu-id="54a56-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="54a56-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="54a56-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54a56-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="54a56-124"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="54a56-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="54a56-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54a56-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="54a56-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54a56-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="54a56-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="54a56-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a56-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="54a56-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

