---
description: Se produce cuando la selección de tinta dentro del control InkPicture está a punto de cambiar, por ejemplo, a través de las modificaciones a la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad de selección.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: Evento InkPicture. SelectionChanging (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b8a35d57aeb9367bb9d30647cb074a7e0e6fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912906"
---
# <a name="inkpictureselectionchanging-event"></a><span data-ttu-id="b3c01-103">Evento InkPicture. SelectionChanging</span><span class="sxs-lookup"><span data-stu-id="b3c01-103">InkPicture.SelectionChanging event</span></span>

<span data-ttu-id="b3c01-104">Se produce cuando la selección de tinta dentro del control [InkPicture](inkpicture-control-reference.md) está a punto de cambiar, por ejemplo, a través de las modificaciones a la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="b3c01-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c01-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3c01-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="b3c01-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3c01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c01-107">*NewSelection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3c01-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c01-108">Nueva colección de [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="b3c01-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c01-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3c01-109">Return value</span></span>

<span data-ttu-id="b3c01-110">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="b3c01-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c01-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3c01-111">Remarks</span></span>

<span data-ttu-id="b3c01-112">Este método de evento se define en las interfaces de solo envío **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** (dispinterfaces) con un identificador de DISPID \_ IOESelectionChanging.</span><span class="sxs-lookup"><span data-stu-id="b3c01-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c01-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3c01-113">Requirements</span></span>



| <span data-ttu-id="b3c01-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c01-114">Requirement</span></span> | <span data-ttu-id="b3c01-115">Value</span><span class="sxs-lookup"><span data-stu-id="b3c01-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c01-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3c01-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c01-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b3c01-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b3c01-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3c01-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c01-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b3c01-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b3c01-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3c01-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3c01-121"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b3c01-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b3c01-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3c01-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3c01-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3c01-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b3c01-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3c01-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c01-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="b3c01-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="b3c01-126">[**Propiedad de selección \[ InkPicture (control)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="b3c01-126">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

