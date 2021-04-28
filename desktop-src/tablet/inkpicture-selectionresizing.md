---
description: 'Evento InkPicture.SelectionResizing: se produce cuando el tamaño de la selección actual está a punto de cambiar, como a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad Selection.'
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: Evento InkPicture.SelectionResizing (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8f70b0b502fe426cfd94ce9002e8bbfc5260a88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086423"
---
# <a name="inkpictureselectionresizing-event"></a><span data-ttu-id="9765f-103">Evento InkPicture.SelectionResizing</span><span class="sxs-lookup"><span data-stu-id="9765f-103">InkPicture.SelectionResizing event</span></span>

<span data-ttu-id="9765f-104">Se produce cuando el tamaño de la selección actual está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="9765f-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9765f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9765f-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="9765f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9765f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9765f-107">*CurSelectionRect* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9765f-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9765f-108">Rectángulo delimitador de la selección después del **evento SelectionResizing.**</span><span class="sxs-lookup"><span data-stu-id="9765f-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="9765f-109">Este rectángulo se especifica en coordenadas de ventana de cliente, lo que permite escenarios como mantener la relación de aspecto al cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="9765f-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9765f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9765f-110">Return value</span></span>

<span data-ttu-id="9765f-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="9765f-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9765f-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9765f-112">Remarks</span></span>

<span data-ttu-id="9765f-113">Este método de evento se define en las interfaces de solo envío (dispinterfaces) de **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador de DISPID \_ IOESelectionResizing.</span><span class="sxs-lookup"><span data-stu-id="9765f-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="9765f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9765f-114">Requirements</span></span>



| <span data-ttu-id="9765f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9765f-115">Requirement</span></span> | <span data-ttu-id="9765f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9765f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9765f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9765f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9765f-118">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="9765f-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9765f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9765f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9765f-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9765f-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9765f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9765f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9765f-122"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="9765f-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9765f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9765f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9765f-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9765f-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9765f-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9765f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9765f-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="9765f-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="9765f-127">[**Propiedad Selection \[ InkPicture (control)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="9765f-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="9765f-128">**InkRectangle (clase)**</span><span class="sxs-lookup"><span data-stu-id="9765f-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




