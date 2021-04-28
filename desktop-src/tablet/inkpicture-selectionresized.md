---
description: 'Evento InkPicture.SelectionResized: se produce cuando el tamaño de la selección actual ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad Selection.'
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: Evento InkPicture.SelectionResized (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dcad4b84cd21ee9b4d385f24033c56913765810
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086473"
---
# <a name="inkpictureselectionresized-event"></a><span data-ttu-id="623b5-103">Evento InkPicture.SelectionResized</span><span class="sxs-lookup"><span data-stu-id="623b5-103">InkPicture.SelectionResized event</span></span>

<span data-ttu-id="623b5-104">Se produce cuando el tamaño de la selección actual ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="623b5-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="623b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="623b5-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="623b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="623b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="623b5-107">*OldSelectionRect* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="623b5-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="623b5-108">Rectángulo delimitador de la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) seleccionada tal como existía antes de que se desencadenase el evento **SelectionResized.**</span><span class="sxs-lookup"><span data-stu-id="623b5-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="623b5-109">Este rectángulo se especifica en coordenadas de espacio de entrada manuscrita, lo que permite escenarios de deshacer.</span><span class="sxs-lookup"><span data-stu-id="623b5-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="623b5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="623b5-110">Return value</span></span>

<span data-ttu-id="623b5-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="623b5-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="623b5-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="623b5-112">Remarks</span></span>

<span data-ttu-id="623b5-113">Este método de evento se define en las interfaces de solo distribución (dispinterfaces) de **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador de DISPID \_ IOESelectionResized.</span><span class="sxs-lookup"><span data-stu-id="623b5-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="623b5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="623b5-114">Requirements</span></span>



| <span data-ttu-id="623b5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="623b5-115">Requirement</span></span> | <span data-ttu-id="623b5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="623b5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="623b5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="623b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="623b5-118">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="623b5-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="623b5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="623b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="623b5-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="623b5-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="623b5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="623b5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="623b5-122"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="623b5-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="623b5-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="623b5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="623b5-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="623b5-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="623b5-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="623b5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="623b5-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="623b5-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="623b5-127">[**Propiedad Selection \[ InkPicture (Control)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="623b5-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="623b5-128">**InkRectangle (clase)**</span><span class="sxs-lookup"><span data-stu-id="623b5-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

